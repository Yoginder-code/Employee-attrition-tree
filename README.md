# IBM Employee Attrition

## Context

The IBM Data Science team built a dataset with fictional information about IBM employees and wether they left the company or not. The dataset can be found [here](https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset).

## Objective

This project aims to train different classifcation models and predict wether an employee might leave the company or not. In the end, the projects are compared based on their recall score, where the best model is the one with highest score.

## Data Preprocessing

For this project, several steps in data preprocessing were followed in order to have a dataset ready for the classification models, some of which were:

### Removing columns with high correlation

  Columns with high correlation between each other need to be remove so that we can remove bias from our models. The heatmap helps identify those columns.
  
  ![image 1](https://raw.githubusercontent.com/tmcdonald92/IBM-Employee-Attrition/main/heatmap.png)
  
  Thanks to the heatmap, we can see that the columns JobLevel and MonthlyIncome have high correlation. Since MonthlyIncome could still have importance to explain our results, the column JobLevel was dropped.
  
### Standardizing values
  
  Another good approach is to standardize the variables to reduce the weight and influence that variables with bigger ranges of values might have on the models' results.
  This was the distribution of each variable after standardization was applied:
  ![image 2](https://raw.githubusercontent.com/tmcdonald92/IBM-Employee-Attrition/main/Hist_standardizsed.png)
  
## Training the data

The models that were used to train the dataset were the following:

* Logistic Regression;
* Logistic Regression with Feature Selection (SFS, SBS and RFE),
* Decision Tree;
* Random Forest;
* KNN;
* AdaBoost;
* XGBoost;
* CatBoost

## Results

After training and testing the models, the one with highest recall score was the **Logistic Regression with SFS**, with a score of **99.35%**
