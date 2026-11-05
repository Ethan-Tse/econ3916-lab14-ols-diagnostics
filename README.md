# econ3916-lab14-ols-diagnostics
OLS Diagnostics: When the Standard Error Is Lying

Objective

I investigated how data violations affect ordinary least squares regressions and learned to diagnose and fix invalid standard errors and influential observations.

Methodology

Simulated heteroskedastic data to fit regressions using both classical and robust HC3 standard errors.

Ran 400 simulated samples to evaluate the true coverage rates of classical versus robust 95 confidence intervals.

Generated and analyzed residual plots alongside Breusch-Pagan and Jarque-Bera formal diagnostic tests.

Measured the impact of an extreme outlier by dropping a single row from a 600-observation dataset.

Fitted a multi-variable regression on the California Housing dataset and calculated standard error scaling ratios.

Built a custom Python function to compute HC3 robust standard errors on arbitrary data slices, both with and without censored ceiling values.

Key Findings

Fitting heteroskedastic data yielded a slope of 2.0147, with classical and robust standard errors of 0.0264 and 0.0290.

Across 400 simulated samples, the classical 95 interval covered the true slope in 91.8 of them (Monte Carlo SE 1.4) and the robust interval in 93.5 of them (Monte Carlo SE 1.2).

Deleting one row out of 600 caused the slope to move 0.58 of its own standard error, while the standard error fell 33.

In the California Housing regression, the HC3 standard error on AveRooms was 5.02 times the classical one.
