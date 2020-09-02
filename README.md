# ToyotaCorolla-Project

Project Overview
In this project, I complete a data analysis process, beginning with posing an objective of the analysis, and ending with reporting my findings and conclusions. 

Project Table of Contents: 
•	Objective
•	Data Set
•	Column Descriptions
•	Accessing the Data
•	Cleaning the Data
•	Analyzing and Visualizing the Data 
•	Model Evaluation and Validation
•	Findings and Conclusions

Objective
Develop a model for predicting the price of a Toyota Corolla for sale. Determine what factors influence the price. 

Data Set:
The dataset contains 37 specifications of 1436 used Toyota Corolla cars for sale, including price, and was downloaded from Kaggle. 

Column Descriptions:
•	ID: ID number
•	Model: Car model
•	Price: Offer price in Euros
•	Age: Age in months
•	Mfg_Month: Manufacturing month (1-12)
•	Mfg_Year: Manufacturing year
•	KM: Accumulated kilometers on odometer
•	Fuel_Type: Fuel Type (Petrol, Diesel, CNG)
•	HP: Horsepower
•	Met_Color: Metallic Color? (Yes=1, No=0)
•	Automatic: Automatic? (Yes=1, No=0)
•	cc: Cylinder Volume in cubic centimeters
•	Doors: Number of doors
•	Cylinders: Number of cylinders
•	Gears: Number of gear positions
•	Quarterly_Tax: Quarterly road tax in Euros
•	Weight: Weight in Kilograms
•	Mfr_Guarantee: Within manufacturer’s guarantee period (Yes=1, No=0)
•	BOVAG_Guarantee: BOVAG (Dutch dealer network) guarantee (Yes=1, No=0)
•	Guartantee_Period: Guarantee period in months
•	ABS: Anti-lock brake system (Yes=1, No=0)
•	Airbag_1: Driver airbag (Yes=1, No=0)
•	Airbag_2: Passenger airbag (Yes=1, No=0)
•	Airco: Airconditioning (Yes=1, No=0)
•	Automatic_airco: Automatic airconditioning (Yes=1, No=0)
•	Boardcomputer: Boardcomputer (Yes=1, No=0)
•	CD_Player: CD player (Yes=1, No=0)
•	Central_Lock: Central lock (Yes=1, No=0)
•	Powered_Windows: Powered Windows (Yes=1, No=0)
•	Power_Steering: Power Steering (Yes=1, No=0)
•	Radio: Radio (Yes=1, No=0)
•	Mistlamps: Mistlamps (Yes=1, No=0)
•	Sport_Model: Sport model (Yes=1, No=0)
•	Backseat_Divider: Backseat Divider (Yes=1, No=0)
•	Metallic_Rim: Metallic Rim (Yes=1, No=0)
•	Radio_cassette: Radio Cassette (Yes=1, No=0)
•	Tow_Bar: Tow Bar (Yes=1, No=0)

Accessing the Data
Downloaded the csv file from Kaggle. I began by importing the data into a Jupyter notebook and exploring the data by checking the data types. This allowed me to determine that two of the variables (Model ID and Fuel_type) contain text strings, while all other variables were integer numbers. 

Cleaning the Data
Used the count function to assess whether there is any missing data. Found that all columns had the same number of observations, meaning there was no missing data. Verified this by checking for missing values by using the .isnull() method and found no missing values.

Next, I removed the variable Id as this assigned a number to each observation and would not influence the dependent variable, Price. I also removed Model because this variable overlaps with some of the other variables (e.g. the car model depends on other specifications or variables such as number of doors).

I also created a histogram to understand the distribution of the data.  

From previously exploring the data by checking data types, I was able to see that there was a categorical variable present. I created n - 1 dummy variables for the categorical variable of Fuel_type and removed the original categorical variable. 

Data Analysis and Visualization
After cleaning and preparing the data, I analyzed the correlation matrix to check for multicollinearity, ensuring to remove variables that were highly correlated (>0.4 or <-0.4) as leaving them in may double-count their influence on Price. I also removed any variables that had a weak correlation (<0.01) with Price, meaning that it has little to no relationship with Price. I created a heatmap version of the correlation matrix to help visually determine where multicollinearity was occurring. 

I also removed the variable Cylinders because every observation had the same number of cylinders, but different prices, meaning it does not have any effect on the price of the car. To confirm this, I found that this variable has no correlation with Price. 

Next, I split the data into a training testing set to later give me an idea of how well my model would perform in the real world. I used an 80% training, 20% testing split to assess the performance of the predictive model. 

Using the training data, I created a linear regression model. I used the summary of model results to determine which variables significantly predicted Price and which variables were insignificant. One-by-one, I removed insignificant variables and ran the regression again each time. 

In regression 6, after removing Airbag 1, Mfg_Year became slightly insignificant with a p-value of 0.09, however I chose to leave this in as all other variables related to year or age of the car were already removed and I believe year often does have an influence on car price, typically due to depreciation over time and increased KMs driven. 

Model Evaluation and Validation 
I evaluated and validated the model in 3 ways:
•	Splitting data into training and testing set to compare predicted and actual values
•	Checking R-squared
•	Checking root mean square error (RMSE)

In the final model, the R squared is high at 0.83, meaning that 83% of the variation of Price (dependent variable) is explained by the model. 

After training the model using the 80% training data, I used the model to predict the y values of the test data and compared those predicted values to the actual y values from the test data. I was able to visualize this data using a distribution plot to compare the predicted versus actual price values. It appears the model’s predicted values tracks the pattern of the actual values well, other than a few areas that are slightly off. 

The root mean square error (RMSE) is 1,680.46. Relative to the car prices, this is not a huge amount. The data ranges from 4,350 to 32,500 in terms of price in Euros. Relative to this range, the RMSE is small at 1,680.46.

Given the RMSE value and the R-squared value, I would conclude that the model can predict Toyota Corolla prices with a decent level of accuracy. 

Findings and Conclusions
Overall, I developed a model for predicting the price of Toyota Corolla cars. The variables or features of Toyota Corolla cars that significantly contributed to their prices included Mfg_Year, HP, Met_Color, cc, Doors, Mfr_Guarantee, Guarantee_Period, Airco, Sport_Model, and Tow_Bar. 

The coefficients of all the variables were positive, except for Tow_Bar. This means that the more recent the manufacturing year, the greater the horsepower, cylinder volume, number of doors, and guarantee period, as well as if the car was a metallic colour, was within the manufacturing guarantee period, had air conditioning, was a sports model and had no tow bar all would lead to a higher price. 

Testing the model using the remaining 20% of the data resulted an RMSE value of 1,680.46, which, relative to the range of prices in the data, is small. This value, in addition to a high R-squared at 83% leads me to conclude that the model is valid and would be useful for predicting future Toyota Corolla prices. 

What can be done now with this model is someone who is looking to sell a Toyota Corolla can determine a fair sale price of the car. Alternatively, for a person looking to buy a used Toyota Corolla, by checking the car specifications, they can determine an approximate price that the car will sell for which may help them budget for buying a car or simply estimate the amount of money they will have to set aside. 

However, there are a few limitations of the model:

One possible reason why the actual and predicted y doesn’t track more closely could be because of the values included in the training and testing sets. If I tested and trained the data multiple times, each time it may be tested and trained with different part of the data and I would likely have received a different result each time. In the future it may be worthwhile to look into cross validation methods so that each observation is used for both training and testing, allowing for a more accurate model. 

Additionally, this model was only based on 1436 data points taken in 2004, which may limit the accuracy of the model if someone were to use the same model by 2015. To improve this model in the future, I would recommend adding new observations to the data over time as adding more data to the model can help the model become more accurate at predicting Toyota Corolla prices. 
