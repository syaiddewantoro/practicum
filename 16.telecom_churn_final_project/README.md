<p align="center">
  <a href="https://practicum.com/id-idn/">
    <img src="https://www.precisely.com/app/uploads/2021/09/Creating-an-Omnichannel-Customer-Experience-in-the-Telco-Industry-768x512.jpg" alt="drawing" width="600" height="350">
  </a>
</p>

# Churn Rate Forecasting for Telecom Operator: Leveraging Client Data for Promotional Strategies

## 1. Final Project Description <a class="anchor" id="Project_Description"></a>

A telecom operator called Interconnect wants to forecast their clients' *churn* rate.󠀲󠀡󠀠󠀥󠀨󠀣󠀤󠀡󠀳󠀰 If it is known that a client is planning to quit, the client will be offered promotional codes and special plan options.󠀲󠀡󠀠󠀥󠀨󠀣󠀤󠀢󠀳󠀰 Interconnect's marketing team has collected some of the client's data, including information about the chosen data plan and their contract.

## 2. Interconnect Service <a class="anchor" id="Layanan_Interconnet"></a>

󠀰Interconnect provides two main types of services:

1. Home telephone network.󠀲󠀡󠀠󠀥󠀨󠀣󠀤󠀦󠀳󠀰 A telephone can be connected to multiple lines simultaneously.
2. Internet.󠀲󠀡󠀠󠀥󠀨󠀣󠀤󠀨󠀳󠀰 Internet networks can be set up through a telephone line (DSL, *digital subscriber line*) or fiber optic cables.

󠀰Some other services that Interconnect provides include:

- Internet security: antivirus software (*DeviceProtection*) and malicious website blocker (*OnlineSecurity*)
- Dedicated technical support line (*TechSupport*)
- *cloud* storage for *files* and data *backup* (*OnlineBackup*)
- TV *streaming* (*StreamingTV*) and movie directory (*StreamingMovies*)

Clients can make monthly payments or sign a contract for a 1 or 2-year subscription.󠀲󠀡󠀠󠀥󠀨󠀣󠀥󠀥󠀳󠀰 They can use various payment methods and receive electronic bills after making transactions.

## 3. Data Description <a class="anchor" id="Deskripsi Data"></a>

󠀰The available data consists of several *files* obtained from different sources:

- `contract.csv` - 󠀰contract information
- `personal.csv` - 󠀰client's personal data
- `internet.csv` - information about Internet services
- `phone.csv` - information about phone service

In each *file*, we can find the `customerID` field with a unique code assigned to each client.

Contract information is valid as of February 1, 2020.

## 4. Work Plans <a class="anchor" id="Work_Plans"></a>

- Defining the problem: Identifying the problem to be solved and answering questions such as predicting the customer churn rate, what factors make clients stop using the service, and what options or customized packages suit the customer's needs.

- Data collection: Collecting relevant data from various sources, such as data on what services were used, customer personal information, and contract information.

- Data cleaning and preprocessing: Clean the data and prepare it for analysis, such as handling missing values, merging data, scaling data, and converting data into appropriate formats.

- Exploratory data analysis (EDA): Perform EDA to gain insights from the data, such as visualizing patterns and relationships, identifying outliers, and detecting correlations.

- Feature engineering: Creating new features from existing data to improve model performance, such as calculating usage trends, customer lifetime value, and segmenting customers based on their behavior.

- Model selection and training: Select an appropriate model based on the problem and data, such as logistic regression, random forest, xgboost, neural network or the model used as a baseline. Train the model on the training data and validate its performance on the validation data.

- Model evaluation and tuning: Evaluate the model's performance and fine-tune its hyperparameters to improve its performance.

- Interpreting results: Interpreting the analysis results, such as identifying the most important features, the most predictive model, and potential causes of identified problems.

- Communication and reporting: Communicating results and insights to stakeholders in the project times a team leader clearly and understandably, such as creating visualizations, presentations, or reports.

## 5. Report

### 5.1. Report on Telco Customer Churn Project

#### Introduction:

This project aims to forecast customer turnover for a telecom firm. It is known as customer churn when a consumer discontinues using a company's products or services. The dataset used for this project includes the client demographics, account details, and usage trends. The objective is to create a predictive model that can correctly identify consumers likely to leave and offer insights that will aid the business in keeping those clients.

#### Data Preprocessing:

This project's first step was to preprocess the data. Combining contract, personal, and service data was necessary for this. Missing values had to be handled, extraneous variables had to be eliminated, and categorical variables had to be coded to nominal. Eighty percent of the data were used for training and twenty percent for testing after being split into training and testing sets.

#### Exploratory Data Analysis: 

To learn more about the data, we conducted exploratory data analysis after preprocessing it. In search of patterns and correlations, we investigated the relationship between different variables and churn. The following are some insights acquired by EDA:

- Shorter-term contract customers are more likely to leave the company.
- Compared to clients with long-term contracts, those with monthly contracts are more likely to churn.
- Customers who use data security services but do not have internet access are more likely to leave.
- Low monthly charge customers are more likely to leave.
- Senior customers are more inclined to leave the company.
- Long-term contracts are more prevalent among customers who have children and partners.


#### Model Construction and Evaluation: 

We trained some machine learning models, such as Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, and Artificial Neural Network (ANN), to forecast customer turnover. All of the models were evaluated using the ROC-AUC score. The ANN model performed the best, with a ROC-AUC score of 85% on the test set. The ROC-AUC values for the other models ranged from 70% to 80%.

#### Difficulties:

The difficulty in completing this project was choosing a suitable model to train the data because, as we can see from the algorithms we chose, some of them were overfitting. 

#### Importance of Features:

We also looked into the value of various features in forecasting churn. The top five essential factors are the contract length, monthly fees and total charges, nb_months, payment method, and internet service. The business can concentrate on these aspects to lower churn.

#### Results: 

The following table displays the ROC-AUC scores for each model on the train and test sets:

- Logistic Regression: 78% on the test set and 87% on the train set when cross-validation is used.
- Random Forest: 78% in the test set and 87% in the train set utilizing cross-validation.
- Cross-validation CatBoost: 90% on the train set, 76% on the test set.
- Cross-validation XGBoost: 92% on the train set, 76% on the test set.
- KNN: 72% on the test set and 88% on the train set when cross-validation is used.
- ANN: 85% on the test set and 84% on the train set using cross-validation.

The Artificial Neural Network model received the highest ROC-AUC score of 85% on the test set. Cross-validation yielded a good ROC-AUC score of 84% for the model on the train set. The ROC-AUC values for the Logistic Regression and Random Forest models on the test set were both 78%.

#### Discussion:

The findings indicate that, to varied degrees, machine learning models might accurately forecast customer churn. A ROC-AUC score of 85% on the test set was attained by the Artificial Neural Network model, which performed better than the other models. It was much easier to train this model quickly, which has several advantages in real-world scenarios. The ROC-AUC values for the Logistic Regression and Random Forest models on the test set were 78%.

#### Conclusion:

The findings of several experiment show that machine learning models can be employed to forecast customer churn for a telecoms business. With the highest ROC-AUC score on the test set, the Artificial Neural Network model is the most effective for this task. The logistic regression and random forest models both had good results and might be used as alternatives. The organization can utilize the predictive model created in this project to spot clients likely to leave and take proactive steps to keep them.

### 5.2. Conclusion

The findings of this project demonstrate the feasibility of using machine learning models to forecast customer churn in the telecom sector. With a ROC-AUC score of 85%, the Artificial Neural Network model had the best performance. By analyzing feature importance, a business can learn which characteristics are most crucial for predicting churn and take proactive steps to keep clients. Overall, this research shows how data science and machine learning can be used to solve business problems like customer turnover.

### 5.3. Recommendation

Based on the influencing characteristics in the prediction model, some of the following suggestions can assist telecom business Interconnect in lowering customer attrition rates:

- Provide Personalised Discounts and Promotions: Based on consumer usage and preference data, offer customized discounts and promotions to customers. Customers will feel appreciated and become more devoted to the Interconnect business.

- Improving client Service: By responding to client complaints and issues immediately, Interconnect can concentrate on offering exceptional customer service. As a result, there will be a rise in customer satisfaction and a decline in customer churn.

- Simplify the invoicing and payment processes by making them more user-friendly and offering more flexible payment alternatives. Customers will spend less time and effort, strengthening their loyalty to the business.

- Track client Satisfaction: Utilise surveys and other feedback channels to track client satisfaction regularly. It will give insight into the demands and preferences of the customer as well as areas that need improvement.

- Provide a Loyalty Programme: A loyalty program honors patrons for their steadfast allegiance. They will be encouraged to stick with the telecom service, which will lower customer churn.

- Analyse Customer Churn Data: Just as we did in this project, examine customer churn data to find trends and causes of churn. Companies can utilize this data to address customer issues, enhance the customer experience, and create strategies for client retention.

- Effective Communication: Engage your audience frequently through newsletters, emails, and SMS. Inform clients about new products and services, and respond to complaints immediately.

Interconnect, a telecommunications firm, can lower customer churn and boost customer loyalty by implementing these suggestions, which will ultimately boost sales and profitability.
