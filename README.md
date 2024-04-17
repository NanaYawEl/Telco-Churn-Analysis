# TELCO-CHURN-ANALYSIS

## Business Problem Overview
In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.

For many incumbent operators, retaining high profitable customers is the number one business goal.

To reduce customer churn, telecom companies need to predict which customers are at high risk of churn.

In this project, you will analyse customer-level data of a leading telecom firm, build predictive models to identify customers at high risk of churn and identify the main indicators of churn.

## Data cleaning
Convert 'TotalCharges' column which is of object type to float type.
Eight missing values were found in the 'TotalCharges' column.
Data has no duplicates.

## Exploratory Data Analysis
1. Count plot shows the distribution of the churn rate in the data which showed an imbalance in the data.
2. Categorical features count plot insights:
- Data is evenly distributed between the two genders; males and females, which       might be useful in further analysis.
- No information added by 'No Internet Service' or 'No Phone Service' and 'No'       categories. --> Replacing 'No Internet Service' and 'No Phone Service' entries     with 'No'.
3. Histogram and box plot of continous features implies that:
  - No outliers exists.
  - 'TotalCharges' feature is right skewed.
4. Scatter plot of 'MonthlyCharges' vs. 'TotalCharges' shows a positive correlation between both and also it affects the Churn rate positively.

## Feature encoding
Several encoding techniques were tested on each categorical feature separately and One-Hot encoding all the categorical features gave the best results.

## Data imbalance
Data imbalance affects machine learning models by tending only to predict the majority class and ignoting the minority class, hence, having major misclassification of the minority class in comparison with the majority class. Hence, we use techniques to balance class distribution in the data.
