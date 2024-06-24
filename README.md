# Project 4: What’s Cooking? Cuisine Classification Model Based On Ingredients.
### By: Haziel Andrade Ayala, Valentin Baltazar, An Nguyen

### Question: What’s Cooking?
Our goal as data scientists for this project was to find out what types of cuisines are cooking by using recipe ingredients to categorize the cuisine. To answer this, we are looking to find the best cuisine classification model based on ingredients.
---
### Datasets ###
Background on data: The following data was used in the analysis and was obtained from [Kaggle](https://www.kaggle.com/c/whats-cooking) which is a data science competition platform.

---

### Data Dictionary ###

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**id**|*int*|Kaggle data|ID assigned to Cuisine| 
|**cuisine**|*object*|Kaggle data|Type of Cuisine|
|**ingredients**|*object*|Kaggle data|Food Ingredients|
|**ingredients_count**|*int*|Kaggle data|Feature Engineered: Count of unique ingredients|
|**ingredients_string**|*str*|Kaggle data|Feature Engineered: Ingredients coverted to string|

---

### Executive Summary:
In conclusion, our best classification model was the Logistic Regression with CountVectorizer default settings (unigram) with a train accuracy score of 0.86 and a test accuracy score of 0.78. Our Logistic Regression model correctly classified with ~80% accuracy. We also found that many of the false predictions have to do with similar recipe ingredients.

We also created other models such as K-Nearest Neighbors, Random Forest Classifier, AdaBoost Classifier, Support Vector Classification (SVC) with paramters unigram, bigram and both unigram and bigram. 

| Classifier Model (with CountVectorizer) | Test Accuracy Score |
| --- | --- |
| Logistic Regression | |
| - unigram | 0.78 |
| - unigram and bigram | 0.77 |
| - bigrams | 0.74 |
| K-Nearest Neighbors | |
| - unigram | 0.63 |
| - unigram and bigram | 0.51 |
| - bigrams | 0.26 |
| Random Forest Classifier | |
| - unigram | 0.75 |
| - unigram and bigram | 0.73 |
| - bigrams | 0.68 |
| AdaBoost Classifier | |
| - unigram | 0.55 |
| - unigram and bigram | 0.55 |
| - bigrams | 0.51 |
| Support Vector Classification (SVC) | |
| - unigram | 0.77 |
| - unigram and bigram | 0.77 |
| - bigrams | 0.70 |

Based on our findings, our recommendation is that the Logistic Regression model would be best to use for finding cuisine based on ingredients. 

To improve this model, there are a few things that we would consider such as implementing gridsearchCV to optimize model parameters, feature engineering with countvectorizer vs. tfidfvectorizer and potetially looking at other possibilities such as making ingredients into individual features.