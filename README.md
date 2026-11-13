# Regression Discontinuity: Bandwidths, Manipulation and Close Elections

## Objective

I used regression discontinuity (RD) designs to see how bandwidth choice affects estimates of a treatment effect at a cutoff, how to test whether the running variable was manipulated, and what a close-election RD says about the ideology of US House representation.

## Methodology

- I simulated a grant program with a true effect of 8 percentage points at the cutoff.
- I estimated the effect with a global quadratic fit and with a local linear fit at a data-driven bandwidth of 16.1.
- I repeated the simulation 300 times and compared root mean squared error (RMSE) across bandwidths.
- I ran a density test for manipulation of the running variable on data where units had moved across the cutoff.
- I ran a covariate continuity test at the cutoff.
- I used the close-election design from Lee, Moretti and Butler (2004) to estimate how much more liberally a US House district is represented when a Democrat barely wins, measured in ADA points.
- I wrote my own local linear RD estimator with a triangular kernel and checked it against the rdrobust package.

## Key Findings

- The global quadratic estimated +0.0357, well below the true effect of 0.08.
- The local linear fit at a bandwidth of 16.1 estimated +0.0789, close to the true effect.
- Across the 300 simulations, RMSE was smallest at a bandwidth of 20.
- The density test gave p = 0.0022 on the data where units moved across the cutoff, which is evidence of manipulation of the running variable.
- In the House data, a district is represented +46.491 ADA points more liberally when a Democrat barely wins (Lee, Moretti and Butler 2004).
- I wrote the local linear estimator with a triangular kernel myself and checked it against rdrobust.
