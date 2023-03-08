# **Regression NYC Taxi Trip Time Prediction**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1RjJpB2QjckFbld9v3hl7w6bs06uGti9c?usp=sharing)

![image](https://user-images.githubusercontent.com/107030716/198834150-38d3f6c7-5d43-4da6-b0f1-051162911ad0.png)


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Summary 
The dataset is based on the 2016 NYC Yellow Cab trip record data made available in Big Query on Google Cloud Platform. The data was originally published by the NYC Taxi and Limousine Commission (TLC). The complete dataset consist of 1458644 & 11 rows and columns, consisting of different features. The major purpose of doing this project will help in predicting the average trip duration of passengers which will help them in saving their time from future trips as well as money, as it is well known for everyone the heavy traffic problem in New York City (NYC). Taxi agencies will also try to improve their service further as they are also getting tough competitions from app-based companies like lyft and uber. </br> 


## Problem Statement
The task is to build a model that predicts the total ride duration of taxi trips in New York City. The primary dataset is one released by the NYC Taxi and Limousine Commission, which includes pickup time, geo-coordinates, number of passengers, and several other variables. </br>

## Data Summary
The dataset is based on the 2016 NYC Yellow Cab trip record data made available in Big Query on Google Cloud Platform. The data was originally published by the NYC Taxi and Limousine commission (TLC). ### The contents of NYC Taxi Time Prediction are:
* id - a unique identifier for each trip.
* vendor_id - a code indicating the provider associated with the trip record.
* pickup_datetime - date and time when the meter was engaged.
* dropoff_datetime - date and time when the meter was disengaged.
* passenger_count - the number of passengers in the vehicle (driver entered value).
* pickup_longitude - the longitude where the meter was engaged.
* pickup_latitude - the latitude where the meter was engaged.
* dropoff_longitude - the longitude where the meter was disengaged.
* dropoff_latitude - the latitude where the meter was disengaged.
* store_and_fwd_flag - This flag indicates whether the trip record was held in vehicle memory before sending to the vendor because the vehicle did not have a connection to the server - Y=store and forward; N=not a store and forward trip.
* trip_duration - duration of the trip in seconds. 

## Exploring solution of the problem
Having a deeper understanding of what problem we are trying to solve, what the users’ needs, and frustrations are, and what the goals are for achieving the best possible solution for both for the business as well as the user, I began by listing out the possible solutions that were arrived from the research.

## Steps Involved

1. Uploading Dataset from GitHub repository - We have loaded the data from the given csv files using a function from pandas library. Then we checked the general information about data. </br> 
2. Data Cleaning - No issue came up regarding cleaning of dataset, as it was clean. 
3. Expolatory Data Analysis (EDA) - Calculated the distance based on haversine formula from pickup and drop-off latitude and longitude. Then we plotted the box plot for the variable and observed there are many outlier so we segregate this variable and see that most of the trip are within 10km, some trip are within 50km while a very few trip crosses 100km. so we eliminate trip with 0 and above 100km distance. Similary for the average speed it was restricted to 60km/hr. We then checked for categorical variable store_and_fwd_flag and passenger_count. We observed the store and fwd. flag contain majority of one category. So we drop this feature. Passenger count variable has entries from 0 to 9. Since there is no trips with 0 passenger either this a miss entry or the driver forgot to enter passenger count of that trip. Also in a taxi maximum six person are allowed to sit including minor. So we eliminate 0 and 7-9 records from our dataset. </br> 
4. Feature Engineering - In feature engineering, feature encoding were performed of the some the variables which were found to be very improtant for our analysis. 
5. Model Building & Evaluation- For model building I selected different regression models were I further applied hyperparameter tuning for optimizing our models and provide good accuracy. After getting the result R^2, adjusted R^2, MSE, RMSE scores were checked and compared using these evaluation metrics with test data. 
6. Feature Importance - After evaluating our models, feature importance were also identified which showed "distance" to be the most important feature among all the given variables in dataset. 


## Model used in study 

1. Linear Regression
2. Lasso Regression
3. Ridge Regression
4. XGBoost Regression -  (Best score of test dataset for R^2 as well as adjusted R^2 value) </br> 
5. Decision Tree Regression
6. Random Forest Regression


## Conclusion 
The present analysis of NYC taxi trip time prediction using supervised regression method was quite challenging but it provided us lots of insights. As the dataset is huge, so I have use different regression models to get the better prediction.

* Firstly, their is not much difference between the train and test values of Linear Regression, Lasso Regression, Ridge Regression during the MSE, RMSE.
* But the model performance of the above mentioned regression models suddenly increases for R^2 and Adjusted R^2 value.
* The model performance for the Decision Tree Rregressor, XGBoost Regressor and Random Forest Regressor finally showed some good performance in both train and test data for MSE, RMSE.
* For R^2 and Adjusted R^2 all above mentioned regressors showed a better running model.
* But among all the used models for ML regression analysis, XGBoost Regressor showed the best performance with 80.72% in test R^2 value and 83.31% in train R^2.


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Acknowledgements 

##### © Copyright 
![image](https://user-images.githubusercontent.com/107030716/198835325-f3e1f465-d56d-4af2-9847-75ec15f1c311.png)

[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/sonica-sinha-25792b18b)
[![GitHub Badge](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Soni-Test)
