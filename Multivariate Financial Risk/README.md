
This data originated from https://archive.ics.uci.edu/ml/datasets/Stock+portfolio+performance

People entering the stock market have different philosophies, methods, and preferences when investing. One common area in which people differ is in their risk tolerance. Given this, portfolios can differ substantially. Many people purchase shares of ETFs and index funds for their own portfolios. These securities can be considered portfolios in and of themselves. The S&P 500 tracks the top 500 largest US companies; many ETFs and index funds track the S&P 500.

The data tracks the S&P 500 and the simulations were designed as a Simplex-Centroid Design. This means that for the 6 predictor variables, we obtain 2^6-1 combinations of weights. This allows us to measure the nonlinear effects of the variables.

The dependent variables are:
1. Annual Return
2. Excess Return
3. Systematic Risk
4. Total Risk

The independent variables are:
1. Book-to-market ratio
2. Return on Equity
3. Price to Sales Ratio
4. Last Quarter Rate of Return
5. Market Value
6. Small Systematic Risk


Power transformations were performed on the dependnet variables. Correlation analyis was performed between the dependent and independent variables.

Initially a multivariate linear model was created which incorperated all depend variables as well as the second and third oreder interaction terms.


