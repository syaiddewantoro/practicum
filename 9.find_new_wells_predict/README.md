<p align="center">
  <a href="https://practicum.com/id-idn/">
    <img src="https://eco-cdn.iqpc.com/eco/images/channel_content/images/biggest_oil_and_gas_companies.webp" alt="drawing" width="600" height="300">
  </a>
</p>

# Find the Best Place for a New Well

## OilyGiant

We work for the OilyGiant mining company. Our task is to find the best place for a new well.

Steps to choose the location:

- Collecting the oil well parameters in the selected region: oil quality and volume of reserves;
- Build a model for predicting the volume of reserves in the new wells;
- Pick the oil wells with the highest estimated values;
- Pick the region with the highest profit for the selected oil wells.

We have data on oil samples from three regions. The parameters of each oil well in the region are already known. We will build a model that will help choose the region with the highest profit margin. Analyze potential profit and risks using the *Bootstrapping* technique.

#### Goals:

- Collect the oil well parameters for each region: oil quality and volume of reserves.
- Build a model for predicting the volume of reserves in the new wells.
- Pick the oil wells with the highest estimated values.
- Pick the region with the highest profit for the selected oil wells.

## Results and Conclusions

1. Data Preparation

- We start by loading 3 datasets consisting of **5** columns and **100,000** rows each.
The three datasets contain no *missing value*; the data types in the columns are correctly defined; the **id** column is defined as an **object,** while **f0,** **f1,** **f2,** and **product** are defined as **floats.**
- In **Region 2**, the `f0`, `f1` and `f2` columns have a multimodal distribution, and the `product` column has a normal distribution.

### 2. EDA and Data Visualization

- In **Region 0**, the columns `f0`, `f1`, and `product` have a multimodal form, meaning that these columns have 2 or more *modes*, the `f2` column has a normal distribution..
- In **Region 1** column `f0` in dataset df1 has a bimodal distribution, column `f1` in dataset df1 has normal distribution, column `f2` and `product` in dataset df1 has abnormal distribution.

### 3. Split the Data

We will divide the data into two sets, the **train set** and the **validation set,** in a 75:25 ratio.
- We use the `f0`, `f1`, and `f2` fields as *features set* and the `product` field as *target set*, we also drop the `id` fields, which are not needed to create the model.

### 4. Model

- We can obtain RMSE values from a training and validation set with similar scores, indicating that neither **underfitting** nor **overfitting** occurs in the two data sets.
**Region 2** will be considered for development because it has the highest average reserve value, but keep in mind that it also has the highest error rate.

### 5. Determine the Profit

- The results of the **boostrapping** technique, which we used to calculate the average profit, confidence interval, and risk of losses, yielded the best area in Region 2 for the location of a new well.
- In these areas, the highest average profit is **4,525,765**, the lowest loss risk is **0.90%** and below the specified threshold value.
- In addition, the region has the narrowest confidence interval, with no negative values in the lower quantile.


## Main Conclusion

We found the best area to develop new wells in **Region 1**. In this area, we get the highest average profit and the lowest risk of loss.
