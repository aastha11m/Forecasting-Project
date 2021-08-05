# Forecasting Project

This project was part of the course Forecasting Methods in Summer semester 2021.

I worked on the Kaggle dataset: “Climate Change: Earth Surface Temperature Data,” which summarizes the average land temperature across states by country around the world. In this project, the goal is to analyze temperatures in different regions of the United States and make forecasts.

Source: https://www.kaggle.com/berkeleyearth/climate-change-earth-surface-temperature-data/code

**Description of the Dataset-** The dataset includes the following columns: - Date - Average Temperature - State - Country

**Data Cleaning-** It started with 645,675 observations. After filtering down to observations in the United States, it came down to 149,745 rows. Then created groups for each climate region. Then we filtered the dates to observations between 1913 and 2013. Next, created groups for each temperature region 
(source: https://www.ducksters.com/geography/us_states/us_geographical_regions.php).

**Regions:** - North East - West - South East - South West - Midwest. Each region has been analysed separately.

**Creating a Time Series Object-** Created a time-series object, filtered the data to include observations between January 1, 1913, and December 31, 2012 (focused on recent 100 years). Further dropped the State column from the dataframe and then took the average by region by month.

Further created dataframes for each region for ease of use.

I defined three functions for the codes being used repeatedly-

a.	Function for auto ETS

b.	Function to obtain AICc using auto Arima, other plausible ARIMA models and plausible ETS models–
This function loops through all plausible values of p, q, P, Q parameters used in ARIMA function with values ranging from 0 to 3. The 4 best ARIMA models with the lowest AICc values are then compared with auto.arima and two other ETS models (ANA and A,Ad,A).This function helps us in evaluating the best model based on AICc and if the best arima model selected is based on acf and pacf plots.

c.	Forecast function - generates accuracy scores and plots the forecast






