Great follow-up — Mutual Information (MI) is one of those concepts that clicks everything else into place.

**Mutual Information (MI)** measures how much knowing one variable tells you about another. It's entropy's answer to the question: _"Are these two things related?"_

Here's the core idea: if two variables are completely independent, knowing one gives you zero information about the other. If they're perfectly correlated, knowing one tells you everything. MI quantifies exactly how much information is shared.

**The formula** builds directly on entropy:

```
MI(X; Y) = H(X) + H(Y) - H(X, Y)
```

Where H(X) is the entropy of X alone, H(Y) is entropy of Y alone, and H(X,Y) is the _joint_ entropy of both together. If knowing Y reduces your uncertainty about X, that reduction _is_ the mutual information.

Think of it with a Venn diagram — MI is the overlap between two entropy circles.

V

visualize

V

visualize show_widget

Here's where MI shows up practically in ML:

**Feature selection** — before training a model, you can score every input feature by its MI with the target variable. Features with high MI are genuinely informative; features with near-zero MI are noise and can be dropped. This is far more powerful than correlation because MI captures _non-linear_ relationships too — correlation only catches linear ones.

**Information gain in decision trees** — this is literally MI under another name. When an ID3/C4.5 tree asks "which feature should I split on?", it's asking "which feature has the highest MI with the labels?" The split that reduces uncertainty the most wins.

**VAEs and representation learning** — the KL divergence term in a VAE's loss is closely related to MI. It penalizes the model for encoding too much information from the input into the latent space, which forces the model to learn compressed, meaningful representations.

**Clustering and ICA** — mutual information between clusters and features tells you whether a clustering is actually capturing meaningful structure in the data versus just grouping arbitrarily.

**Key advantage over correlation:** correlation assumes linearity. MI doesn't. If Y = X² (a perfectly predictable but nonlinear relationship), Pearson correlation gives ~0. Mutual information correctly identifies this as a perfect dependency. This makes it especially useful in finance and biology where relationships are rarely linear.

The main downside is that estimating MI from real data is tricky — it requires either binning continuous data (which introduces bias) or using more sophisticated density estimators. Given your trading work, MI-based feature selection is genuinely useful for finding which indicators are actually informative about price movements. 

[[Machine Learning/Entropy]]