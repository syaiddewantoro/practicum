<p align="center">
  <a href="https://practicum.com/id-idn/">
    <img src="https://appscrip.com/blog/wp-content/uploads/2022/07/444555.webp" alt="drawing" width="600" height="350">
  </a>
</p>

# Ride-Sharing Analysis

## Zuber

We work as analysts for Zuber, a new ride-sharing company launching in Chicago. Our job is to find patterns in the available information. We want to understand passenger preferences and the impact of external factors on the trip.

Using the database, we will look at data from competitors and test our ideas about how the weather affects the number of trips.

#### Goals:
- Determine the top ten regions to be served.
- Shows a chart of companies with the most deliveries.
- Shows a graph of the top ten passenger-destination regions.

#### Hypothesis testing:

- On rainy Saturdays, the average journey time from the Loop to O'Hare International Airport changes. 

## Results and Conclusion

### 1. Data Collection and Preprocessing Stage

- This project starts with collecting external data through the website, studying the database, and analyzing data from competitors.
- We have **3** datasets to analyze, the first contains information about taxi companies, the second contains information on delivery locations, and the third contains information about the time needed for delivery when the weather is rainy or not.We begin by loading the **2** datasets, "company" and "drop-off location," and inspecting the contents to ensure that the data types match.

### 2. Explanatory Data Analysis and Hypothesis Test

- Next, we analyze the companies that have the most trips, and the most popular destinations, and then we display the graphs.
- In the next step, we load weather data and use the **t-test** method to see if the weather affects delivery time.

### 3. Result and Recommendation

- The **Flash Cab** company has significantly more deliveries than its competitors, with a difference of more than 40% compared to second place; additional data shows that **Loop** and **River North** are the most popular destinations from other locations.- The results of the hypothesis test show that `The average trip duration from the Loop to O'Hare International Airport changes on rainy Saturdays`, so we can conclude that weather conditions can affect the time passengers arrive at their destination, with the difference in the average travel time being an average of 7 minutes longer in rainy weather.
- We need to understand why Flash Cab has the most trips; we also know that Loop and River North are the most popular destinations, so drivers can choose to wait for passengers in the area. That said, during rainy weather, we can notify *customers* that there may be delays in pickup and delivery times so that passengers can order taxis earlier.
