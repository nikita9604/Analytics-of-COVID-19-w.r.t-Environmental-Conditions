## Analytics of COVID-19 w.r.t Environmental Conditions

To perform Descriptive and Predictive Analytics of COVID-19 with respect to different Weather parameters such as temperature, humidity, dew point, wind speed, pressure and precipitation intensity.

### Datasets Used 
  1. [Covid-19 dataset](Datasets/covid_19_data.csv)
  2. [Weather dataset](Datasets/daily_weather_2020.csv)

### Steps Involved as per the Data Analytics Life Cycle 
  1. Objective
  2. Understanding the Data
  3. Data Cleaning and Data Transformation
  4. Data Enhancement
  5. Data Analytics
  6. Data Visualization

### Objective
To analyse the spread of COVID-19 disease with respect to environmental conditions of a particular region and check whether using the data of weather conditions of a particular place, can we predict the total number of Confirmed Cases on that particular day.

### Descriptive Analytics
The datasets containing the COVID-19 data and weather data were first cleaned, imputed and then merged. The merged dataset was used to find out the trend of the spread with respect to the date. Observing the plot of total confirmed cases per day vs Days, it was decided to split the dataset into 2 sets - one before March 15 and the other After March 15. March 15 was an elbow point in the graph plotted. 

After splitting up based on this point the results improved as this reduced a lot of hidden factors that might have skewed the model. Plots between Confirmed cases grouped by only pressure or only precipitation Intensity was not fruitful as the graph showed no trend in this manner. Using the correlation values obtained, pairs of variables that had good correlation with each other and with the Confirmed Cases were taken and plotted. For this, plotly.express graphs were used. Each graph had one weather parameter each in the x-axis and y axis, and the intensity of colour of the data circles and their size corresponded to the Confirmed Cases count. All these plots did not follow any specific trend. Very minute trends were observed when graphs were plotted only for a particular month, that too for months till March as till then the virus was concentrated in China alone.     

### Predictive Analytics
Correlation matrix is shown and observed for the 2 split datasets and also for the whole dataset.
Then different Machine Learning models were used to try and fit the data to it. The following models were performed:
1. Linear regression:
     - With combination of max correlated features.
     - Simple Linear regression with a weather parameter.
     - With all the weather parameters.
2. XGboost:
     - Simple and Multiple
3. SVM
     - Radical basis function and Linear Kernel
4. Decision Tree based
5. Considering only China (more number of cases):
     - Linear regression
     - Xgboost

### Conclusion

In this work, we are motivated to study and analyze the impact of different weather parameters in relation to the number of infected cases due to COVID-19. We have presented descriptive and predictive analytics for the spread of COVID-19 on different features taken from climatic conditions such as temperature, humidity, dew point, wind speed, pressure and precipitation intensity. To validate the proposed result, we have used publicly available datasets which were trained on the specified climatic conditions.

In our fight against coronavirus, it is possible to note here that this project can be used as an input to create general awareness and bust the myth on weather stimulating coronavirus spread that emerged during the past couple of months. Moreover, as we are limping through this period, it is advisable to continue with the lockdown and ensure social distancing until the vaccine is created irrespective of the change in climate.

### Reference
Dataset are taken from the following links:
- https://www.kaggle.com/sudalairajkumar/novel-corona-virus-2019-dataset?select=covid_19_data.csv
- https://www.kaggle.com/vishalvjoseph/weather-dataset-for-covid19-predictions
