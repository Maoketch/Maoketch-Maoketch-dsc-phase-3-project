# 1. Business Problem
Maintaining customer retention holds immense value for businesses, particularly within the competitive telecommunications industry. Research indicates that the costs associated with acquiring new customers can significantly outweigh those of retaining current ones. This project aims to create a predictive model for SyriaTel, enabling the identification of customers prone to churning. By analyzing diverse customer data encompassing demographics, usage patterns, complaints, and billing records, we seek to unveil correlations and factors influencing churn.

Through comprehensive exploratory data analysis and meticulous feature selection, we aim to pinpoint the primary drivers of churn and construct a robust machine learning model. The model's performance will undergo evaluation using pertinent metrics before its deployment into operational use.

This initiative will empower SyriaTel to actively retain customers at risk of leaving, thereby mitigating financial losses attributed to customer attrition. Continuous monitoring and refinement of the model will be undertaken to ensure its efficacy in predicting churn and facilitating targeted retention strategies.

## 1.1 Problem Statement
SyriaTel has faced significant losses due to a notable churn rate. The goal of this project is to construct a precise predictive model that pinpoints customers at risk of churning within SyriaTel, a telecommunications company.

Through proactive identification of potential service discontinuations, the aim is to diminish customer attrition and uphold a larger customer base. Ultimately, this endeavor strives to assist SyriaTel in mitigating financial losses attributed to churn, elevating overall customer retention rates, and refining business strategies to bolster profitability.

## 1.2 Business Objectives
The primary business objectives of this project for SyriaTel are;

1.To understand the factors that contribute to customer churn.'
2.To understand factors boosting customer loyalty,
3.To enhance overall customer retention.

## The Data
The data used for the project can be found here(https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset).

During the data cleaning, and exploratory data analysis:
* We found that the data had 3333 rows and 20 columns
* The data did not contain any missing data, duplicates, or placeholders for missing data.
* we noted the data had a number of outliers and we opted to keep them as they may carry valuable information or insights that could be relevant to our analysis.


## Data Preprocessing and Modelling
During the exploratory data analysis, we realised that these columns had a high correlation:

* **Total day minutes & Total day charge** - correlation 1 

* **Total eve minutes & Total eve charge** - correlation 1 

* **Total night minutes & Total night charge** - correlation 1

* **Total intl minutes & Total intl charge** - correlation 1 

We choose to drop these columns since they had the least to contribute to our project objective:

1. Total day minutes 
2. Total eve minutes 
3. Total night minutes 
4. Total intl minutes 

We then used the train_test_split method to divide our data into the training and testing data we need to perform our modeling.
After performing our logistic regression we realised that our data was imbalanced so we set about using the **SMOTE** method to create synthetic data that mirrored our data and helped balance it thus allowing us to model our data better.

We used four different models:
* Logistic Regression.
* Decision trees
* KNearest Neighbour(KNN)
  
## Model of Choice: Decision Trees
We then choose the **Decision trees** for the following reasons:

* the model achieved a high recall score of 0.75. Recall, also known as sensitivity or true positive rate, measures the proportion of actual churn cases correctly identified by the model. In our case, a recall score of 0.75 implies that the decision tree model can capture a significant number of churn cases, correctly identifying 75% of the actual instances of customers who are likely to churn. This high recall score is crucial because it aligns with our objective of identifying and mitigating churn effectively.

* the model demonstrated an accuracy score of 0.91. Accuracy represents the overall correctness of the model's predictions. This indicates that the model performs well in accurately predicting churn, which is essential for making informed business decisions.

 * The model's substantial ability to balance precision and recall is reflected in its F1 score of 0.72. The F1 score combines precision and recall into a single metric, providing a balanced measure of a model's performance. A higher F1 score indicates that the model effectively identifies true positives while minimizing false positives and false negatives. In our case, the Decision tree model achieves an F1 score of 0.72, suggesting that it strikes a good balance between precision and recall, resulting in accurate identification of churn cases.
  


 ## Recommendations and Future Investigations
 
### Customer Service Calls Investigation:
Dig deeper to understand why some customers need to contact customer service frequently and if there is a relationship between customers who call and their churn rate. This will help in finding ways to better assist them.

### International Plan Churn Investigation:
Since some of the customers with international plans are leaving, it's essential to explore bundled plan for them in oreder to retain these customers.

### High Churn States Analysis:
Look into the states where many customers are leaving to identify any patterns or reasons for the high churn rates.

### Incentives for High Bill Customers:
Find ways to reward customers with high daily charges (over $55) for them to stay with SyriaTel. This might involve offering extra benefits and perks. Currently, all of these high bill customers are leaving, which is a concern.

### Incentives for Customers who stay more than 6 months:
Find ways to encouragte customers to stay with the company even longer, eg giving them loyalty points offers etc, as this will help in creating a form of loyalty.

# Conclusion

It is important to monitor the effectiveness of these measures through ongoing analysis of churn rates, customer feedback, and market trends. Regularly evaluating and adapting these strategies based on customer needs and preferences will help optimize retention efforts and reduce churn effectively. Additionally, providing personalized offers, loyalty programs, and targeted marketing campaigns can further contribute to improving customer satisfaction and loyalty.