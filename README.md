# Hypothesis Testing — Is Job Training Worth It?

## Objective

I examined whether participation in the LaLonde NSW job training program was associated with higher earnings in 1978.

## Methodology

- Loaded the LaLonde NSW experimental sample with 445 participants: 185 trainees and 260 controls.
- Ran a one-sample t-test and a two-sample Welch's t-test on 1978 earnings.
- Wrote my own `welch_t()` function and checked its results against scipy for the full sample and five demographic subgroups.
- Computed Cohen's d to measure the size of the treatment effect.
- Conducted a power analysis for the observed effect and for an effect size of d = 0.3.
- Tested treatment effects across five overlapping demographic subgroups.
- Applied Bonferroni and Benjamini-Hochberg corrections for multiple testing.
- Simulated p-value distributions when the null hypothesis was true and when it was false.

## Key Findings

Trainees earned $1,794.34 more on average in 1978 than controls. The Welch's t-test gave t = 2.6741 and p = 0.0079, so the difference was statistically significant at the 5% level.

The estimated Cohen's d was 0.2727, indicating a small effect size.

Before correcting for multiple comparisons, 2 of the 5 subgroup effects were statistically significant. After the Bonferroni correction, 1 subgroup effect remained significant.
