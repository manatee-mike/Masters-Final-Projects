
This data origionated from [Kaggle](https://www.kaggle.com/datasets/vetrirah/ml-iot).

The data set consists of hourly traffic data collected at 4 junctions. The data at the 4th junction was incomplete so only the first 3 junctions were used. There was too much data for my computer to handle model fitting so the data was regrouped into daily traffic.


Most of the model fitting was performed with the [auto.arima](https://www.rdocumentation.org/packages/forecast/versions/8.18/topics/auto.arima) function. 
After creating initial time series functions correlations were looked at between the junctions and models were created that used data  from the other junctions.
