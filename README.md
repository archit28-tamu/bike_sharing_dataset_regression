# Regression on Bike Sharing Data

## Introduction
Bike-sharing rental process is highly correlated to the environmental and seasonal settings. For instance, weather conditions, precipitation, day of week, season, hour of the day, etc. can affect the rental behaviors. The core data set is related to the two-year historical log corresponding to years 2011 and 2012 from Capital Bikeshare system, Washington D.C., USA which is publicly available in http://capitalbikeshare.com/system-data. Data is aggregated on daily basis and then extracted and added the corresponding weather and seasonal information. Weather information are extracted from http://www.freemeteo.com.

Link to Dataset: https://www.kaggle.com/datasets/harbhajansingh21/bike-sharing-dataset?select=day.csv

**Goal of the Project:**
The goal of the project is to make the predictions of number of bike rentals based on various seasonal impacts and weather conditions. The motivation of the set goal is to give the business insights on what can they expect with the number of bike rentals for the following week so that they can better optimize their resources. For this problem, hypotheses would have to be tested and upon comparision of various hypotheses and models, the best results would be published.

**Objective of the Project:**
The objective of the research is to design 3 hypotheses and apply multiple regression models on the data based on the hypothesis. Then the various results would be comparied using mean squared error to choose the best proforming regression model among the ones used. Also, the results of the varous hypotheses would be compared to choose the best performing set of data attributes along with the model. Also, before fiting the model on the data, data preprocessing would be done to check for any null values in the data and drop the columns that are not required for regression. Also, to design hypotheses, Exploratory Data Analysis would be performed on the data to better understand its features.

## Data Description
The data has been collected and combined from various sources, like, the bike rental data has been collected from the publicly available dataset present at Capital Bikeshare system's website (http://capitalbikeshare.com/system-data), and the weather data is extracted from http://www.freemeteo.com/.

**Columns Details**

- instant: index
- dteday : date
- season : season (1:springer, 2:summer, 3:fall, 4:winter)
- yr : year (0: 2011, 1:2012)
- mnth : month ( 1 to 12)
- holiday : weather day is holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
- weekday : day of the week
- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
- weathersit :
  
  Clear, Few clouds, Partly cloudy, Partly cloudy
  
  Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
  
  Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
  
  Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
  
- temp : Normalized temperature in Celsius. The values are divided to 41 (max)
- atemp: Normalized feeling temperature in Celsius. The values are divided to 50 (max)
- hum: Normalized humidity. The values are divided to 100 (max)
- windspeed: Normalized wind speed. The values are divided to 67 (max)
- casual: count of casual users
- registered: count of registered users
- cnt: count of total rental bikes including both casual and registered
