The data was collected from scraping from Zillow's api.

This project looked at Zillow's estimated home value (Zestimate). 525 samples (homes) in and around Boston were collected through the api.

The Zestimate was labeled as estimateValue.

The dependent variables are:
- City
- State
- Latitude
- Longitude
- Use Code
- Tax Assessment
- Year Built
- Lot Size
- Finished Size
- Bathrooms
- Total Rooms
- Last Sold Price

Engineered variables include:
- Years Since Sold
- Latitude From Boston
- Longitude From Boston
- Distance From Boston


40 data points did not have the zestimate and the values were dropped.

There were 97 missing values in the dependnet variables. These values were imputed with [random forests](https://www.rdocumentation.org/packages/randomForest/versions/4.7-1.1/topics/rfImpute). 

80 % (322 samples) of the data was used for training. The other 20 % was used for testing.

The box cox transformation revealed an optimal value of 0.22.

Models were created by estimating estimateValue, estimateValue$^{0.2}$, and log(estimateValue).

linear models and random forests were used to model the regression. The stepwise process was used to add and remove variables when creating the linear models for estimateValue^0.2 and log(estimateValue). Each linear model obtained an $R^2 > 0.8$.

The test data was used to check to see which model produced the best predictions. Overall the random forest with the dependent variable transformation of $y = estimateValue^{0.2}$ produced the model with the least error.



