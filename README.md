# econ5200-lab05-risk-model
# Diagnosing a Flawed Risk Model — VaR, Expected Shortfall & Monte Carlo

## Objective
My goal was to identify problems in a Value at Risk (VaR) model and compare different methods for measuring portfolio risk.

## Methodology
- Reviewed a junior analyst's normal-distribution VaR model and compared its results with historical VaR.
- Calculated VaR and Expected Shortfall (ES) using historical simulation, normal distribution, and Student-t distribution methods.
- Fitted a Student-t distribution to the returns data.
- Used antithetic variates to reduce Monte Carlo simulation error.
- Worked with the `risk_metrics.py` module, including `calculate_var`, `calculate_es`, and `mc_var`, and ran its self-tests.
- Asked AI to write a VaR backtesting function, revised my prompt once, and checked the output against my own breach count.

## Key Findings
- The normal-distribution model underestimated historical VaR by **12.7%**, equivalent to **$40,393** for the portfolio at the 99% confidence level.
- The fitted Student-t distribution had **4.58 degrees of freedom**, allowing for heavier tails than the normal distribution.
- Antithetic variates reduced Monte Carlo standard error by a factor of **1.26**.
- The normal 99% VaR was exceeded on **1.71% of trading days**, higher than the expected 1%.
- The backtesting results showed that the normal model underestimated the frequency of large losses.
