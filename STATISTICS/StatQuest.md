
![[Pasted image 20260325173910.png]]

P value <0.05 is against null hypotheses which means it is true . Means are very close

Comparing Multiple Tests with P-Values
The Setup: Which ad drives the most clicks?
A company tests 3 different ad designs on their website over 1 week:
AdClicksViewsClick RateAd A (Red button)300100030%Ad B (Blue button)280100028%Ad C (Green button)250100025%
The baseline (no special ad) averages 25% click rate.

Running a test on each ad
AdDifference from baselineP-ValueSignificant?Ad A (Red)+5%0.01✅ YesAd B (Blue)+3%0.08❌ NoAd C (Green)0%0.95❌ No

Reading the results

Ad A (p = 0.01): Only 1% chance this 5% boost is random → Red button genuinely works
Ad B (p = 0.08): 8% chance it's random → Slightly above the 0.05 cutoff → Not convincing enough, could be a fluke
Ad C (p = 0.95): 95% chance it's random → Green button does absolutely nothing
