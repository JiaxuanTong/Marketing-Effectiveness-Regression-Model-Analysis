# Marketing Effectiveness Regression Model Analysis

## Overview

The main purpose is to explore the relationship between the Sales performance and advertising budgets access to TV, Radio, and Social Media.

In this project, linear regression models for each of the marketing types should be chosen and built, and deeper exploration includes combining the three types of expenditure into a multiple linear regression model.


## Dataset

The dataset used for this project is the Dummy Marketing and Sales Data. The dataset contains 5 columns consisting of TV promotion budget (in million), Social Media promotion budget (in million), Radio promotion budget (in million), Influencer: whether the promotion collaborates with Mega, Macro, Nano, Micro influencer, and Sales (in million), where the data type of the influencer column is categorical and others are numerical data type.

The dataset used in this project is the **Dummy Marketing and Sales Data** from Kaggle.

Dataset source:  
https://www.kaggle.com/datasets/harrimansaragih/dummy-advertising-and-sales-data

The original dataset contains 4,572 records and five variables:

- TV advertising expenditure
- Radio advertising expenditure
- Social Media advertising expenditure
- Influencer category
- Sales

For the regression analysis, TV, Radio, Social Media, and Sales were selected as numerical variables.

## Exploratory Data and Rgression Analysis

DATA 555 Project 1 Marketing Outcome Prediction
Summative Report

In this project, there are two types of linear regression models being built, the first type consists of three simple linear regression models aimed at predicting the sales performance of three independent marketing types, the second type is a multiple regression model that aims at predicting the sales performance by combining three marketing types.

In order to explore the correlation and determine the regression model type, the scatter plots were used to help to visualize the patterns of the paired values for each of the advertising types and Sales. From the scatter plots, the data points are almost arranged along a straight line from the lower left to the upper right corner for all three of them, indicating that there is a positive linear relationship between marketing type and Sales. However, they all showed different degrees of scatter, revealing that they may have different strengths of linear relationship with sales. 

Pearson's correlation scores were 0.9995 for TV, 0.8686 for Radio, and 0.5274 for Social Media, which indicates that TV appears to be the strongest individual linear predictor of Sales; the R-squared values were 0.999 for TV,  0.755 for Radio, and 0.278 for Social Media, this indicates that the TV model can explain the most variation in the Sales performance; the RMSE values were 2.949 for TV, 46.081 for Radio, and 79.020 for Social Media, which indicates that the TV model produces the smallest prediction error within approximately 2.949 million.

Since TV, Radio, and Social Media in the original dataset exist simultaneously in the same record, a multiple linear regression model was built to explore the relationship between Sales and all three advertising expenditures together.

The multiple linear regression model has an R-squared value of 0.999, TV has the coefficient value of 3.5626, Radio has -0.0040, and Social Media has 0.0050, RMSE is approximately 2.9485 million. Meanwhile, the residual plot in the notebook has shown that residuals are randomly scattered around zero which means there are no obvious error patterns, it suggests that the model chosen for this dataset is appropriate.

Overall, the multiple regression equation is shown as figure 1. This means although Radio and Social Media are positively correlated with Sales in a simple linear regression model, TV itself captured almost all the linear information related to Sales within this dataset in the multiple linear regression model. The RMSE for multiple linear regression model is similar to the TV in simple regression model, this also proves that adding Radio and Social Media, the model does not improve the goodness of fit much.

## Key Findings

The regression models indicate that TV appears to be the most effective platform in prediction of Sales in this dataset, however, since the dataset author states that it is dummy data for data science learning purpose, the result should be validated with real business dataset when making the advertising budget decision in a real business environment.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- SciPy
- Statsmodels
- Jupyter Notebook

## Project Structure

```text
.
├── Analysis.ipynb
├── README.md
├── requirements.txt
├── data/
    └── Dummy Data HSS.csv
