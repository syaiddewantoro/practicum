<p align="center">
  <a href="https://practicum.com/id-idn/">
    <img src="https://www.letstalk.com/app/uploads/2019/11/reachmobile2-1.jpeg" alt="drawing" width="600" height="300">
  </a>
</p>

# Telecom Plans Analysis

## Statistical Data Analysis

As an analyst for the telecom operator Megaline, the company offers its clients two prepaid plans, Surf and Ultimate. The marketing department wants to discover which plans generate more revenue to adjust the advertising budget. We Will conduct a preliminary analysis of the plans based on a relatively small client selection.

We will have the data on 500 Megaline clients: who they are, where they're from, which plan their use, and the number of calls their made and text messages they sent in 2018. Our job is to analyze the clients' behavior and determine which prepaid plan generates more revenue.

The purpose of this project is:
1. Analyze users behavior
2. Calculate the mean, variance and standard deviation
3. Visualize the data and describe the distribution

Test the hypothesis:
- The average income of users of Ultimate and Surf phone plans is different.
- The average income of users in the NY-NJ area differs from that of users from other regions.

# Results and Conclusions

We have done several steps in processing the mobile plan data to get conclusions:

## 1. Preprocessing Data

- We have five datasets, each containing information about our service users. That 5 dataset includes the information of 500 users using the service, the minutes of call they spent, the number of messages they sent, the total data they used, and the information about the price of each plan.
- There are some missing values ​​in the data, but filling in the missing values ​​isn't always needed.
- We have to convert some columns, especially the column with the object type, to the timestamp format to make it easier for us to do the following analysis.

## 2. Transformation Data

- We created new columns like the month based on the date columns in the calls, messages, and internet dataset to calculate the amount of traffic from each user every month.
- We created the function to calculate the revenue from each user every month, applied the process, and created a new column called revenue.

## 3. Visualization and Analysis

- The calling behavior from users of each plan is very similar.
- The ultimate users sent more messages than surf plan users, but there is no significant difference between the two plans. Most users don't use their message quota at all. It may happen because they prefer to use an instant messaging application with the internet; we suggest changing the SMS quota to an instant messaging application quota.
- The internet usage for ultimate plan users is slightly higher than users of the surf plan, but the variance of the users from the ultimate plan is less than the surf plan users.
- The users from surf plans bring in more revenue than ultimate plans. It's because the number of ultimate users programs is more than the surf plans users.

## 4. Test the Hypothesis

- The results of the analysis that we have done determine that the average income of the surf plan and the ultimate plan is different, this is of course too surprising because we see that some users on the surf package pay extra for their bills for excess usage, with this result it will certainly be a consideration for the marketing department in adjusting the advertising budget for each package.
- The results of other analyses also determine that the average income of users in NY-NJ and other cities is similar. With these results, it will certainly be a consideration for the marketing department in adjusting the advertising budget in one city and another, which means we can recommend the advertising department so that there is no need to differentiate the advertising budget in each city.
- We recommend users who often experience overuse upgrade their packages, or if there are quite a number of them, we can consider adding a new package as an option between the surf package and the ultimate package.
