
This data origionated from [Kaggle](https://www.kaggle.com/datasets/vetrirah/ml-iot).

The data set consists of hourly traffic data collected at 4 junctions. The data at the 4th junction was incomplete so only the first 3 junctions were used. There was too much data for my computer to handle model fitting so the data was regrouped into daily traffic.


Most of the model fitting was performed with the [auto.arima](https://www.rdocumentation.org/packages/forecast/versions/8.18/topics/auto.arima) function. 
After creating initial time series functions correlations were looked at between the junctions and models were created that used data from the other junctions.

The presentation of the data and models can be fund in [final ts pjt.ppts](https://github.com/manatee-mike/Masters-Final-Projects/blob/main/Time%20Series%20Traffic/final%20ts%20pjt.pptx)
