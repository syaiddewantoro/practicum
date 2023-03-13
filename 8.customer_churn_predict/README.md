<p align="center">
  <a href="https://practicum.com/id-idn/">
    <img src="https://cdn.dnaindia.com/sites/default/files/styles/full/public/2021/09/09/995364-payment-gateway-integration.jpg" alt="drawing" width="600" height="300">
  </a>
</p>

# Customers Churn Prediction

## Supervised Learning

Bank Beta's customers are leaving the company: little by little, their number is decreasing every month. Bank employees realized it was cheaper to retain their loyal old customers than to attract new ones.

In this case, our task is to predict whether a customer will leave the Bank soon or not. We have data regarding clients' past behavior and history of termination of their contracts with the Bank.

We will build a model with the highest possible F1 score. We need a minimum F1 score of 0.59 for the test dataset to pass the review. Check the F1 value for the test set.

In addition, we'll measure the AUC-ROC metric and compare it to the F1 score.

**Objective:**
- Predict whether a customer will soon leave the Bank or not.
- Train models without considering class imbalance.
- Improve data quality for running models.
- Find the best model to predict the Bank's customers.

# Conclusions

**1. Data Preparation**
- We start by loading a dataset consisting of **14** columns and **10,000** rows, the column types are defined correctly.
- There is a *missing value* of **909** rows or **9%** from the data in the 'tenure' column, and we have filled in the average age.
- We also changed the *register* column names to lowercase for easy analysis.

**2. EDA and Data Visualization**
- Of the two groups of customers who are *exited* and those who are not, the majority have an average credit score between **550 - 750**.
- Many customers have no remaining balance in their *account* there are around **500** people from the **exited** group and more than **3000** customers from the *stay* group. The other majority are from they also have an average *balance* between **100,000 - 150,000**
- *Estimated Salary* has an even distribution starting from **0 - 200,000**.
- The majority of the group that remained faithful had an age range of under **50** years, while the **exited** group had an age range of **40-60** years.
- The majority of Bank Beta's customers come from France
- Most Bank Beta customers use at least **1-2** products issued by the bank.
- The majority of Bank Beta's customers also have a card.

**3. Split the Data**
- Comparison of data in the `exited` column of **80** with **20** we divide the data into **3** types with the proportion **70%** *training set*, **15%** * validation set*, and **15%** for *test set*.

**4. Models without Class Adjustment**
1. In the **Decision Tree Classifier** model, the results obtained cannot reach the limit for the *fi score* on the `train set` and `validation set`. The best parameter is **max_dept = 7**.
2. **Logistic Regression** model results obtained are higher than **Decision Tree**, with values on *train* and *validation* set of **84%** and **82%** and have passed *threshold* value. The best model is obtained by setting the parameter **solver = lbfgs**.
3. In the **Random Forest** model, the best model is obtained by setting **n-estimators = 5**, having a very large difference between the *training set* and the *validation set*.
4. In the **K-Nearest Neighbors** model, we define **n-neighbors** in the range **1 - 20**, and the best model is obtained at the value **n-neighbors = 13** even though **f1** there is nothing that can exceed the specified threshold value.

**5. Improving Model Quality**
- We improve the quality of the model with the **upsampling** method by randomizing **3** times to adjust the class balance and using the **StandardScaller** method to adjust the scale.
- We also apply the `class_weight = balanced` parameter to some models.

**6. Models After Improved Quality**
1. In the **Decision Tree Classifier** model, **max_depth = 5** is the best parameter with an increase in *f1 score* in each dataset of around **19%** or to **80%** and **55%** for data *train* and *validation* sets.
2. The **Logistic Regression** model has decreased *f1 score* on datasets of around **15%** or becomes **78%** for *train* data, even *validation* sets do not reach the specified minimum threshold only get **46%**, this model is better before *balanced* data.
3. The **Random Forest** model with a value of **n-estimators = 9** is the best parameter and has an increase in *f1 score* in the *validation set* so that between the two *train* and *validation* data there is a significant difference or to **82%** and **50%** for data *train* and *validation* sets and do not reach threshold values.
4. The **K-Nearest Neighbors** model, with a value of **n-neighbors = 18**, is the best parameter and has an increase in *f1 score* in the *validation set* or becomes **69%** and **57%** for *train* and *validation* data sets even though they have not been able to reach the specified threshold value with several *tuning* parameters.

The value of **AUC-ROC Score** in all models is above **70 - 80%**, this shows that our model is better than the random model.

**Main Conclusion**

We found the best model after *balancing data* with the highest *f1 score* in **Random Forest** with the `max_depth` parameter set to **13**, obtaining *f1 score* **60%** on *test set*.
