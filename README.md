A small exploratory Python analysis of how bat body size and season relate to
prey richness and the average body mass of prey.

**Rendered notebook:** [https://holzmann33.github.io/Relation-of-Bats-and-Prey/]

## What the notebook does
- Loads and cleans a field dataset of 43 individual bats
  (body mass, forearm length, prey richness, mean prey mass, season)
- Standardizes bat body mass (z-score) and codes season as a categorical
  variable (Spring, Summer, Autumn)
- Models prey richness (a count variable) with Poisson and negative-binomial
  regressions, using a dispersion check and AIC to compare them
- Models mean prey mass with OLS, including bat size × season interaction terms

## Results
With only 43 observations, most coefficients are not statistically significant,
so the results should be read as exploratory. The Poisson model fit the count
data better than the negative binomial (lower AIC, Pearson dispersion of about 0.87).

**Tools:** Python, pandas, NumPy, statsmodels
