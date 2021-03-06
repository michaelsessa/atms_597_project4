# ATMS 597 Project 4 Group F
ATMS 597: Weather and Climate Data Science
Project 4 Group F
Group Members: Max Grover, Michael Sessa, Rose Miller

The following class project utilizes regression methods for weather prediction and validation for the Champaign-Urbana region from 2010-2019.
Multiple linear regression using past Global Forecast System (GFS) forecast data was used to predict a WxChallenge-like forecast. This was also repeated using a random forest regression analysis as well.

The weather predictions for this model used the following:
Using the 12 UTC GFS forecast and observations up to 00 UTC to predict the following variables for the 6 UTC to 6 UTC period of the following day:

Maximum Temperature (°C)
Minimum Temperature (°C)
Maximum Wind Speed (m/s)
Total Precipitation accumulation (mm)

The training data for the model were the years of 2010-2018 and 2019 was the validation dataset.
The following datasets were used in this project:

Hourly and Daily observations from KCMI that were used for both training and validation.
Daily GFS 12 UTC initialization forecasts, three hourly GFS surface forecast parameters, three hourly upper air forecast parameters.

A large portion of this project included data manipulation. NAN values and missing data were removed from the observed data as well as the GFS model data. The hourly observed precipitation data was used to calculate daily precipitation data and negative precipitation data was removed. The individual datasets were then organized into pandas dataframes, merged into master dataframes, and separated into training and test data.

For the regressions, the observation and model forecast were combined into one dataframe. Days with missing data of NAN values were not used as discussed above. RMSEs were calculated to determine regression performance for the desired variables.
