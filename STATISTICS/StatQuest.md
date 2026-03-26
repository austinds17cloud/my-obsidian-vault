
![[Pasted image 20260325173910.png]]

P value <0.05 is against null hypotheses which means it is true . Means are very close

## Comparing Multiple Tests with P-Values

### The Setup: Which ad drives the most clicks?

A company tests **3 different ad designs** on their website over 1 week:

| Ad | Clicks | Views | Click Rate |
|---|---|---|---|
| Ad A (Red button) | 300 | 1000 | 30% |
| Ad B (Blue button) | 280 | 1000 | 28% |
| Ad C (Green button) | 250 | 1000 | 25% |

The baseline (no special ad) averages **25% click rate.**

---

### Running a test on each ad

| Ad | Difference from baseline | P-Value | Significant? |
|---|---|---|---|
| Ad A (Red) | +5% | **0.01** | ✅ Yes |
| Ad B (Blue) | +3% | **0.08** | ❌ No |
| Ad C (Green) | 0% | **0.95** | ❌ No |

---

### Reading the results

- **Ad A (p = 0.01):** Only 1% chance this 5% boost is random → Red button genuinely works
- **Ad B (p = 0.08):** 8% chance it's random → Slightly above the 0.05 cutoff → Not convincing enough, could be a fluke
- **Ad C (p = 0.95):** 95% chance it's random → Green button does absolutely nothing

---

### The key takeaway here

> Comparing p-values across tests tells you **which results you can trust** and which might just be noise.

But watch out — when you run **many tests at once**, you naturally increase the chance of *accidentally* getting a p < 0.05 somewhere. This is called the **multiple testing problem.** With 20 tests, you'd expect one false positive just by chance, even if nothing is real. Researchers fix this using corrections like **Bonferroni correction**, which raises the bar for significance when running multiple comparisons.



![[attachments/Pasted image 20260326195852.png]]

![[attachments/Pasted image 20260326200349.png]]

