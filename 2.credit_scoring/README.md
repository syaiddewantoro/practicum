<p align="center">
  <a href="https://practicum.com/id-idn/">
    <img src="https://github.com/syaiddewantoro/resources/blob/main/project%20image/bank%20credit.png" alt="drawing" width="600" height="370">
  </a>
</p>

# Analyze the Risk of the Borrower Failing to Pay¶

## Pre-processing Data

As a credit analyst, our project is to prepare reports for the bank's credit department. We find out the effect of a customer's marital status and the number of children on the probability of being on time in repaying the loan. Banks already have some data regarding customer creditworthiness.

Our report will be considered when making a **credit assessment** for prospective customers. **Credit scoring** is used to evaluate the ability of potential borrowers to repay their loans.

The main purpose of this project is to determine a client's eligibility to get credit based on their status and circumstances stored in our data. We also test the capacity of customers based on their characteristics which we summarize based on categories so that *patterns* are obtained to give yellow lights to customers who fall into certain categories.

Project hypothesis:
1. Is there a correlation between the number of children and the ability to repay loans on time?
2. Is there a correlation between family status and the ability to repay loans on time?
3. Is there a correlation between economic class and the ability to repay loans on time?
4. Is there a correlation between credit goals and the ability to repay loans on time?

## General Conclusion

- We have done a *cleansing data* process to fix problematic data in our dataset. The cleaning that we do includes filling in missing values, removing duplicate values, correcting irregular registers and values that are too large, and replacing unreasonable values so that we get a dataset we can process for the credit analysis process.

- The findings that we get after exploring are that there is a correlation between the number of children and marital status in the risk of credit payments. Clients who do not have children will find it easier to pay off their debts than clients with children. Clients who are married or have had a partner have a lower risk of default than clients who are single or live together.
Clients with lower incomes will be more likely to have loan debt, and clients who use the money for home purposes will have a higher percentage of them being able to pay off their debts.

- But can we use all the data manipulation we do in the **decision-making** process to minimize the risks that will occur in the future?
