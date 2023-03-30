<p align="center">
  <a href="https://practicum.com/id-idn/">
    <img src="https://i.guim.co.uk/img/media/f621b0c91f06a597a5e86c86270e7b808f3a24dc/0_354_5256_3154/master/5256.jpg?width=620&quality=85&dpr=1&s=none" alt="drawing" width="600" height="350">
  </a>
</p>

# Customers Plan Behavior

## Megaline (Introduce to Machine Learning)

Mobile operator Megaline is dissatisfied because many of its customers are still using old packages. The company wants to develop a model that can analyze consumer behavior and recommend one of the two new Megaline packages: Smart or Ultra.

We have access to the behavioral data of customers who have switched to the latest package (from the Statistical Data Analysis course project). In this classification task, we need to develop a model that is able to choose the right package. Considering that we have completed the data pre-processing step, we can go directly to the model building stage.

We will develop a model that has the highest possible accuracy. In this project, the threshold for the accuracy level is 0.75. We will examine the model accuracy metrics using a test dataset.

#### Goals :

1. Separating the source data into training sets, validation sets, and test sets
2. Check the quality of different models by changing their hyperparameters. Briefly explain the findings obtained from this study.
3. Using a test set to evaluate the model's quality.
4. Conduct a sanity check on the model.

## Conclusions

### 1. Data Preparation

- We begin by loading a dataset with **4** columns and **3214** rows; there are four **float** columns, namely **calls,** **minutes,** **messages,** and **mb_used.**
- We change the **calls** and **messages** columns, which contain the number of calls and messages sent, to **int.**

### 2. EDA and Data Visualization

- According to the call volume graph, the average user makes **30-80** calls per month.
- The average user spends **250-500** minutes per month on calls.
- On average, users of both packages do not use their text message quota at all, this might be because they have switched to instant messaging or chatting applications that use internet data.
- Users on both plans use approximately **10,000-20,000 MB** of data per month.

### 3. Split the Data
- We directly divide the data into three types using the **fast_ml.model_development** library in the proportions of 70% for `training sets`, 15% for `validation sets`, and 15% for `test sets`. 

### 4. Models

We use several models with a number of settings in the parameters to get the best results:
1. The **Logistic Regression Model** results in an **accuracy** level of 75% for the **training test** and 74% for the **validation test** when Newton-CG is set on the **solver** parameter.The results of applying the model to the *test set* data were not able to increase the *accuracy* level, and the *accuracy* continued to decrease to **70.8%** which made this model ineligible to be used as a *machine learning* model.
2. Using several **looping** processes in the **Decision Tree Model,** we set the **max_dept** parameter with a **range** of **1** through **11** then set the value to **max_depth = 3**. In this model, the *accuracy* level in the training set is **80%**, in the validation set it is **79.2%**, and in the test set it is **76.6%**, indicating that the model has passed the *threshold* specified *accuracy* level.
3. The **Random Forest Model** results show *overfitting* in the *training set* with a value of **95%** versus the *validation set* with a value of **77%**, with the 'n-estimator' parameter set at a value of **3**.The *test set* also did not produce a significant difference, producing an *accuracy* level of **75%**. Thus, this model does exceed the specified *threshold* value, but *overfitting* occurs, so we cannot use it.
4. The K-Nearest Neighbors Classifier Model produces a fairly good accuracy level of **76.9%** on the training test and a rate of **75%** on the validation test. The results of the *test set* are unfavorable because the accuracy level drops significantly to below the *threshold* with the number **71.8%**, indicating that this model cannot be used for *machine learning*.


### Main Conclusion

With the `max_dept` parameter set to **3,** we find the best model with the highest *accuracy* value and lowest *margin* in the **Decision Tree Model**. 
