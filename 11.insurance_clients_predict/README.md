# Obfuscating Client Data without Reducing Machine Learning Quality

## Linear Algebra

An insurance company called "Sure Tomorrow" wants to solve some problems with the help of machine learning. You are asked to evaluate the possibility.

**Goals:**

- Task 1: Find clients who are similar to specific client criteria. This task will make it easier for the company to do marketing.
- Task 2: Predict whether new clients will likely get insurance benefits. Is the model's prediction better than the *dummy* model?
- Task 3: Predict the amount of insurance benefits a new client will likely receive using a linear regression model.
- Task 4: Protect the client's data without breaking the model from the previous task. It is essential to develop data transformation algorithms that can prevent the misuse of personal information if the data falls into the wrong hands. It is called data hiding or data obfuscation. However, the data protection procedure also needs to be considered so that the quality of the machine learning model does not decrease. You don't need to choose the best model. Just prove that the algorithm works accurately.

## Conclusions

**1. Data Preparation**
- We start by loading a dataset with a total of **5000** rows and **5** columns.
- We rename the columns to lowercase to make it easier to analyze.
- No *missing value* is found, but there are some duplicates, and we decided to remove the duplicates.

**2. EDA and Data Visualization**
- The number of male and female *customers* is equal, and the income distribution is normal, with the average income at **40,000**.
- All insurance *customers* are aged between **18** years old and **65** years old. There are no young *customers* who receive insurance benefits. All *customers* who receive insurance benefits are above the age of **40** years.

**3. Model**
- In *objective* 1, we look for clients with similar characteristics and find that the scaled data has a smaller *distance* than the original data.
- In *objective* 2, we look for a comparison between the number of clients who receive insurance benefits and those who do not. The data shows that the number of insurance beneficiaries is much less than the number of clients who receive insurance benefits. The results of the *evaluation metric* on the model also show that the model with scaling has much better results than the model without *scaling*.
- The result of regression test on *objective* 3 shows that the result of **RMSE** on the model with *scaling* is better by **10%** than the model without *scaling*.
- We successfully performed data blurring on *objective* 4, by multiplying the numerical features. We also managed to restore the data to its original state.

**Main Conclusion**
- In the blurred data, we can see that the data has a different distribution from the original data through the results shown by some diagrams. Even though the data has a different distribution, it still shows the same results when we *train* the model.
