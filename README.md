# BikeSharing Case Study
> Problem Statement : A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic.So to accelerate its revenue as soon as the ongoing lockdown comes to an end, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market.

Company wants to know :
 - Which variables are significant in predicting the demand for shared bikes.
 - How well those variables describe the bike demands

> Business Goal : Business requirement is to develop a model that demands for shared bikes with avialable independent variables. Management will use this model to understand how demands vary with different features, so that they can control the business strategy to meet customer's expectations and demand levels. Further , this model will also help management to understand demand dynamics of new market.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
- Bike Sharing System is a shared micromobility service for short term bike rental in which all processes are automatic like rental, return and subscription.This system provides facility that user can rent bike from one station using their app and can return bike any of the docking station, which makes bike sharing a convenient alternative to both public transportation and private cars. Nowadays in many cities, renting a bike has become an everyday digital service.So there is a possiblity of huge data due to this bike-sharing system which can be usable for analysis and bring out some insight for this business.

- Attribute's Characteristics
    - instant: record index
    - dteday : date
    - season : season (1:spring, 2:summer, 3:fall, 4:winter)
    - yr : year (0: 2018, 1:2019)
    - mnth : month ( 1 to 12)
    - holiday : weather day is a holiday or not 
    - weekday : day of the week
    - workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
    - weathersit : 
        - 1: Clear, Few clouds, Partly cloudy, Partly cloudy
        - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
        - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
        - 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
    - temp : temperature in Celsius
    - atemp: feeling temperature in Celsius
    - hum: humidity
    - windspeed: wind speed
    - casual: count of casual users
    - registered: count of registered users
    - cnt: count of total rental bikes including both casual and registered

- Bike Sharing is an innovative transportation program, which is ideal for short distance point-to-point trips providing users the ability to pick up a bike or bicycle at any self-serve bike station and return it to any other bike station located within the system's service area. Its overall goal is providing fun , healthy and low-cost transportation for locals and visitors alike.

- Business Problem : During the Corona pandemic there is a considerable dip in bike sharing demand so in revenues. So the goal to solve this problem is to find out the independent features which might be significant to up the demand of bike sharing, later management can follow that solution and those features to understand and manipulate the business strategy and meet the customer expectation and demands.

- Task Performed
    - Reading, Understanding and Visualizing the data
        - Total number of records in the dataset
        - Checking for null values or missing values
        - Dropping unnecessry columns
        - Determine categorical and numerical columns
        - Calculation Correlation matrix using Heatmap
        - Outlier Analysis using Boxplot
        - Change Categorical variable according to data dictionary
        - Bi-variate Analysis using Pair plot
    - Preparing data for Modelling
        - Split the dataset into train and test data
        - Scaling the train data set
    - Training the model
        - fit-transform the training data set
        - find out the best fit linear model
    - Residual analysis
        - Check the error distribution, it should be normal
    - Predictions and evaluation on the test set
        - transform and evaluate the test data set with best fit linear model


## Conclusions
- Season : There is high demand for bike sharing in Fall/Raining season and Very Low demand in Spring season as compare to others.
- Year(yr) : In year 2019 demand is high as compare to year 2018.
- Month(mnth) : August and September are pretty significant than other.
- WeatherSit : When weather situation is clear demand rises, When weather situation is LightSnow demand falls.
- Top 3 features contribution towards explaining demand of bike sharing
    - temp (temperature) : Due to positive correlation with cnt (Target variable)
    - yr (year) : Positive Correlation
    - weathersit (LightSnow + Mist) : Negative Correlation

## Technologies Used
- Python - version 3.9.12
- numpy library - version 1.21.5
- pandas library - version 1.4.2
- seaborn library - version 0.11.2
- matplotlib.pyplot library - version 3.5.1
- sklearn.model_selection - train_test_split
- sklearn.preprocessing - MinMaxScaler
- sklearn.feature_selection - RFE
- sklearn.linear_model - LinearRegression
- statsmodels.api
- statsmodels.stats.outliers_influence - variance_inflation_factor
- jupyter notebook - version 6.4.8


## Acknowledgements
Give credit here.
- This project was inspired by Upgrad.
- Referenced from Google, Case Study live session and Stack-Overflow (the famous one)


## Contact
Created by Pallavi Gupta : (https://github.com/pallavi-17763)  - feel free to contact me!
