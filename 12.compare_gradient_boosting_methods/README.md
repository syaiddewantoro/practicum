# Comparing Gradient Boosting Methods with Random Forest, Decision Tree, and Linear Regression

## Numerical Method
 
Rusty Bargain is a used car buying and selling company developing an app to attract new buyers. In the app, we can find the market price of a car. We have access to historical data: specifications, version, and price of the vehicle. We need to build a model to determine its value. 

Goals:
- Prediction quality;
- Speed of the model in predicting;
- Time required to train the model

## Consclusions

**1. Data Preparation**
- Our data contains a collection of specifications and prices of a car.
- Quite a lot of missing values were found in around 20% of the data.
- Some columns have abnormal values, such as the power and year columns.

**2. EDA and Data Visualization**
- Most of the cars we sell start from a price of 0.
- The majority of cars we advertise have mileage above 140,000 miles.
- Most of the cars posted on the app have registration years between 1990 and 2016.
- The majority of cars have an engine power rating below 400 hp.
- The most popular car types are sedan, small, and wagon. Most consumers prefer a compact car type for use or an urban type.
- Almost all cars are fueled by petrol and gasoline.
- The majority of cars have never been repaired before.
- Most cars have manual transmissions, four times more than automatic transmissions.


**3. Train, Test Split**
- We split the data into two groups of train set and test set with a ratio of 70:30 because the available data is quite large.
- We create OHE features because models such as Linear Regression, Random Forest, and XGBoost require categorical data in OHE form.
- We also do Ordinal Encoding conversion on categorical data for the LightGBM model, while the CatBoost model can read data in object form.

**4. Model Analysis**
- In the Random Forest model, the time needed to train the model is relatively short by setting the depth parameter of 10 levels. The best result of this model increases by about 33% from the baseline model by setting the max_depth = 10.
- The XGBoost model takes the longest to train the train data even though we only set the depth parameter at five levels. The results obtained are also slightly better than the Random Forest model.
- The LightGBM model has the shortest training time than some previous models. Although the results are not better than XGBoost, we can still set some parameters to optimize the results considering the short training time.
- The CatBoost model is the model with the best results. Although it takes a little longer, it is still in the excellent category because training a model with depth parameters below up to 10 levels takes about 4 minutes. This model is the most balanced among all existing models.


**Main Conclusion**
- We get the best model in this project in the CatBoos model, the model takes little time to train the model, and the results obtained also have the slightest error among all models. In addition, this model also does not require categorical data to be converted into numerical form or dummies.
