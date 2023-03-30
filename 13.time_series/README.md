# Predict the Number of Taxi Orders for the Next Hour

## Time Series

A taxi company called Sweet Lift has collected historical data on taxi orders at the airport. It needs to predict the number of taxi orders for the next hour to attract more drivers at peak hours. We will model such a prediction.

The RMSE metric on the *test set* should be at most 48.

### Objective

1. Download the data and perform *resampling* within one hour.
2. Analyze the data.
3. Train different models with different hyperparameters. The test sample should be 10% of the initial *dataset*.
4. Test the data using the test samples and provide conclusions.

## Conclusions

**1. Data Preparation**
- Our data contains a collection of time and number of taxi bookings from the airport.
- No missing values and duplicates were found.

**2. EDA and Data Visualization**
- The trend of taxi bookings increases every month, although not significantly in the early months.
- We resampled the first week of March and the first two days of August to see the distribution of data based on seasonality, showing the number of taxi bookings from the airport peaks at 00:00 or 12pm, this could be because at midnight taxis are the only mode of transportation available at the airport so customers do not have other alternatives.
- 6am is the least taxi booking time, this could be because at that time most airlines are just about to take-off and not many planes have landed at the airport.

**3. Features Engineering**
- We perform feature engineering by adding 5 lag columns, and setting a rolling window of 10 with an average value.

**4. Model Analysis**
- From several training models that we did, we found the best model in the CatBoost model with a max_dept parameter of 5.
- This model has the lowest rmse value in the test results, although it has a considerable difference with the rmse results from the train data.

**Recommendation**

Following these guidelines will help a taxi business run smoothly during rush hour:

- Recruit more drivers: During peak hours, the company can hire more drivers based on estimates of the number of taxi orders for the following hour. It will make it more likely that there will be enough drivers to satisfy customer demand.

- Optimize the locations of the drivers who are accessible in order to decrease customer wait periods. Each driver's location can be tracked using GPS information, and they can be assigned to pickups that are near to where they are right now.

- Provide incentives to drivers: By providing drivers with increased pay rates, bonuses, or other rewards, the company can encourage them to work during peak hours. Thus, it can be made clear that

- Provide incentives to drivers: By providing drivers with increased pay rates, bonuses, or other rewards, taxi companies can encourage them to work during peak hours. This may guarantee that there are sufficient drivers on hand during rush hour.

- Enhance dispatching: To manage driver availability and satisfy customer demand, a dispatching system that works well is essential. The software can be used to automatically allocate pickups to drivers based on their availability and location as well as to optimize routes to shorten wait times for customers.

- Customers should be given real-time information about potential wait periods during peak hours. Real-time updates on expected wait times and the status of taxi requests are crucial for reducing frustration. It can lower client complaints and raise satisfaction levels generally.

A taxi business can efficiently manage driver availability and satisfy customer demand during peak hours by adhering to these suggestions. This can raise sales for the business and increase customer happiness.
