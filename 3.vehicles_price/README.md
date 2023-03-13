<p align="center">
  <a href="https://practicum.com/id-idn/">
    <img src="https://github.com/syaiddewantoro/resources/blob/main/project%20image/car%20sales.jpg" alt="drawing" width="600" height="350">
  </a>
</p>

# What Factors Sell a Car?

## Exploratory Data Analysis

As an analyst at Crankshaft List, hundreds of free vehicle advertisements are displayed on the Company's website daily. Our team needed to study datasets over the last few years and determine the factors that influence the price of a vehicle.

**Goals**

In this project, we will focus on Exploratory Data Analysis and Data Visualization, which will help us identify outliers in the data, find patterns and provide new insights. Data visualization also helps tell a story by depicting data in an easier-to-understand visual form and highlighting trends.

This study is to answer 5 hypotheses:
1. Is there a correlation between the price and the age of the vehicle
2. Is there a correlation between price and vehicle mileage
3. Is there a correlation between the price and the condition of the vehicle
4. Is there a correlation between the price and the color of the vehicle
5. Is there a correlation between the price and the type of vehicle transmission

## General Conclusion

We have carried out several stages in processing car data to draw conclusions.

**A. Preprocessing Stage**

From our exploration, we get some conclusions:
1. We start with a dataset size of **51525** rows and **13** columns, there are 5 columns that have *missing values* namely model_year, cylinders, odometer, paint_color, and is_4wd.
2. The following steps are to fill in the values from the columns that have *missing values*, fix the data type, improve the data quality, and add a few columns.

The cause of missing value can be caused by *human error* or simply not having enough data access with the vehicle, considering that some cars are ancient and can be more than one hundred years.

**B. Exploration Stage**

After the preprocessing data stage, we do some exploration:
1. Set *outliers* limits from the price, age, and odometer columns, and create a new dataset with **46169** rows.
2. We also filter to get ad time within the range **1 - 150 days**.
3. We find that sedans and SUVs are the most popular types of cars.

**C. Conclusion**

From our exploration, we get some conclusions:
1. Car price versus age has a negative connection even if the value is not very high, meaning that a newer car will have a higher price.
2. The price of a car and the average distance have a very weak correlation.
3. Price and conditions show a low correlation.
4. Cars in black and white have a higher price than other colors.
5. The transmission type does not always indicate that an automatic car will be more expensive than a manual one.
