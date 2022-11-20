
This data originated from https://archive.ics.uci.edu/ml/datasets/Stock+portfolio+performance

People entering the stock market have different philosophies, methods, and preferences when investing. One common area in which people differ is in their risk tolerance. Given this, portfolios can differ substantially. Many people purchase shares of ETFs and index funds for their own portfolios. These securities can be considered portfolios in and of themselves. The S&P 500 tracks the top 500 largest US companies; many ETFs and index funds track the S&P 500.

The data tracks the S&P 500 and the simulations were designed as a Simplex-Centroid Design. This means that for the 6 predictor variables, we obtain 2^6-1 combinations of weights. This allows us to measure the nonlinear effects of the variables.

The dependent variables (y) are:
1. Annual Return
2. Excess Return
3. Systematic Risk
4. Total Risk

The independent variables (x) are:
1. Book-to-market ratio
2. Return on Equity
3. Price to Sales Ratio
4. Last Quarter Rate of Return
5. Market Value
6. Small Systematic Risk


Power transformations were performed on the dependnet variables. These transformed letters were denoted with the letter z. Correlation analyis was performed between the dependent and independent variables.

Initially a multivariate linear model was created which incorperated all depend variables as well as the 2nd and 3rd oreder interaction terms.
The likelihood ratio test for regression parameters was used to check to see if the 3rd order parameters could be removed. The corresponding p-value for both the chi-squared and F-statistic was approximately 1. Additionally, we performed a bootstrap analysis to check whether or not the chi-squared and F-statistic were appropriate to use on this data. 

Next we look at whether the 2nd order terms involving x3 as well as X4*X5, X4*X6, and X5*X6 could be removed. A p-value of 0.0542 was obtained by likelihood ratio test again. Thus, we determined that it was appropriate to remove those interactions from the model.

The final model becomes Z ~ X1 + X2 + X3 + X4 + X5 + X6 + X1*X2 + X1*X4 + X1*X5 + X1*X6 + X2*X4 + X2*X6. The coefficients and their p-values are shown below. The model does a good job of estimating all of the response variables as shown with adjusted R-squared values between 0.96 and 0.987. This means that at least 96% of the variance in Z can be explained with this model. Overall someone could use this model to determine what kind of portfolio they should have so that they can invest according to their goals for returns and risks.

