#  Train a Model to Automatically Detect Negative Reviews

## Machine Learning for Text

Film Junky Union, a new community for classic movie fans is developing a system to filter and categorize movie reviews. The goal is to train a model to automatically detect negative reviews. We will use the IMBD movie review dataset with polarity labeling to build a model that can classify positive and negative reviews. This model should have an F1 score of at least 0.85.

**Goal**
- Train the model to automatically detect negative reviews

## Conclusion

**1. Data Preparing**
- We start with data totaling 47331 rows and 17 columns.
- The train set and test set have a 50:50 ratio.

**2. EDA**
- We know that every year the number of movies reviewed increases. It can happen because the number of members is getting bigger, and people find it difficult to access previous movies, especially if they still need to be in digital form.
- The number of positive and negative reviews also has a 50:50 ratio.

**3. Model**
- The **logistic regression** model with NLTK, TF-IDF produces a much better F1 value than the dummy classifier model and passes the threshold value.
- Although the F1 score results of NLTK, TF-IDF with XGBoost are not better than the vectorization results with Logistic Regression, this model is less prone to overfitting.
- The **logistic regression** model with Spacy, TF-IDF produces F1 values that are almost the same as NLTK, TF-IDF but with slightly better results.
- **The LGBM model with Spacy, TF-IDF** produces F1 values that are not better than the **logistic regression** model with Spacy, TF-IDF.
- **BERT** model with **logistic regression** gives results that are not too significantly different from the previous models, but this model has better performance to be free from overfitting.

**Main Conclusion**
- The BERT model does produce the best performance and is free from overfitting, but it does take a very long time to transform. We can consider this model if our main goal is to get the best F1 results.
- But if our main focus is on the transformation time, we should use NLTK, TF-IDF and XGBoost, which have similar results to the BERT model.
