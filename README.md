# Projects
- Project 1: SAT & ACT Analysis
- Project 2: Predicting House Sale Prices with Machine Learning

# Project 1: SAT & ACT Analysis

## Problem Statement
Geographically, the United States remains divided by more than just geology. For each state, the participation rate of their high school students in the SAT vs ACT varies wildly. Yet, clear trends and correlations emerge. Why do some states remain loyal to only one test? Moreover, which specific factors influence the popularity of tests? Additionally, how do political and economic factors influence the layout of the test landscape? Finally, what can we suggest to raise participation rates.

## Executive Summary
The ACT dominates the SAT rate all three years in terms of participation. This results from State-Required Testing, Self-Selection, Economic Inequality, and Political Bias. To increase participation, we recommend that the SAT Board streamline the Fee Waiver Application Process, get rid of SAT Subject Tests, increase State-Required SAT Tests, add Science as its own Subject, and politically insist on the importance of SAT testing.

## Project 1 Contents:
2017 Data Import & Cleaning
2018 Data Import and Cleaning
Exploratory Data Analysis
Data Visualization
Descriptive and Inferential Statistics
Outside Research
Conclusions and Recommendations

Data Source
- General Assembly Data Science Immersive 2020

Outside Research Sources
- https://www.brookings.edu/research/race-gaps-in-sat-scores-highlight-inequality-and-hinder-upward-mobility/ impact of race, wealth, required testing on SAT/ACT
- https://www.vox.com/the-goods/2019/3/28/18282453/sat-act-college-admission-testing-cost-price impact of wealth on SAT/ACT
- https://www.cnbc.com/2019/10/03/rich-students-get-better-sat-scores-heres-why.html impact of wealth on SAT/ACT
- https://www.forbes.com/sites/prestoncooper2/2020/02/07/should-colleges-abandon-sat-score-requirements/#277e3736edd3 Abandoning score requirements on SAT/ACT
- https://www.insidehighered.com/admissions/article/2018/06/25/younger-people-and-democrats-more-likely-back-test-optional-admissions Abandoning college score requirement with politics on SAT/ACT
- https://www.census.gov/library/visualizations/2016/comm/cb16-158_median_hh_income_map.html #US MEDIAN INCOME BY STATE
- https://www.270towin.com/maps/2016-actual-electoral-map Democrat vs Republican 2016 Race
- https://www.statista.com/statistics/233301/median-household-income-in-the-united-states-by-education/ Income from college
- https://www.testive.com/state-sat-act/#:~:text=Each%20U.S.%20state%20has%20a,student%20achievement%20using%20standardized%20tests.&text=In%20addition%2C%20free%20 State-required SAT/ACT testing list of states

# Project 2: Predicting House Sale Prices with Machine Learning

## Problem Statement
The AMES Housing Data Set represents the amenities of over 2900 properties in Ames, Iowa priced and sold from 2006 to 2010. Over 75 distinct variables divide these amenities into categories. 

The four categories of amenities for each house are categorical, ordinal, discrete, and continuous. Categorical (or nominative) values, such as neighborhood or type of roofing, lack a hierarchy of quality and possess qualitative information. Ordinal values possess a clear hierarchy (like Kitchen Quality (Excellent, Good, Average, Poor)) but still represent qualitative information. Discrete variables are countable (like Number of Cars) and quantitative. Finally, continuous variables are quantitative, measurable, and can contain fractions of values (like Square Footage). 

How can this information be used by Real Estate developers and clients to predict or increase a property's value? Moreover, how can a data scientist use a model to process all of this data?

## Executive Summary
By using the form of Machine Learning called Linear Regression, this project processes through a database of AMES Housing training data. Then, linear regression predicts a house's sale price and value using the training data's trends and properties. Additionally, regression techniques (such as feature engineering and selection) enhance the quality of our predictions.

## Conclusions

One can use linear regression to greatly reduce errors and improve the performance of predicting sale price based on a variety of highly correlated factors. Although, it seems that knowing which factors influence a house's price (such as Kitchen Quality and Bathroom Space) can often be more valuable than the predictive model itself. As a result, even the basic method of Linear Regression can be incredibly useful for a firm's Real Estate pricing decisions.

The interpretability of linear regression (as opposed to more complex models) makes it one of the more easy models to make inferences with. We have the ability to note which features correlate with Sale Price to be able to improve the price. Additionally, we also have the relative correlations of Sale Price with other factors, giving us an actual quantitative idea of how to advise a Real Estate branch on how to recreate their properties.

## Project 2 Contents:

### Informative
- Problem Statement
- Executive Summary

### train_df
- Data Cleaning: Categorical (Nominal) Columns with Null Values - train_df
- Data Cleaning: Continuous Columns with Null Values - train_df
- Data Cleaning: Discrete Columns with Null Values - train_df
- Data Cleaning: Categorical Columns without Null Values (Making Dummies) - train_df
- Data Cleaning: Ordinal Column Mapping
- Data Cleaning: Correlation Heatmap
- Data Cleaning: Continuous Columns with Null Values - train_df
- Exploratory Data Analysis (Identifying/Possibly Dropping Outliers) - train_df
- Feature Engineering - train_df¶
- Model Definition - train_df
- Model and Fit - train_df

### test_df
- Data Cleaning: Categorical (Nominal) Columns with Null Values - test_df
- Data Cleaning: Continuous Columns with Null Values - test_df
- Data Cleaning: Discrete Columns with Null Values - test_df
- Data Cleaning: Categorical Columns without Null Values (Making Dummies) - test_df
- Data Cleaning: Ordinal Column Mapping
- Data Cleaning: Continuous Columns with Null Values - test_df
- Exploratory Data Analysis (Identifying/Possibly Dropping Outliers) - test_df
- Feature Engineering - test_df¶
- Model Definition - test_df
- Model and Fit - test_df

### Exporting Dataframes
- Exporting test_df Dataframes
- Ridge
- LASSO

Conclusions
- Descriptive and Inferential Statistics
- Outside Research
- Conclusions and Recommendations

Data Source
- General Assembly Data Science Immersive 2020
- Kaggle
- https://www.kaggle.com/c/dsir-720-project-2-regression-challenge/overview
- http://jse.amstat.org/v19n3/decock/DataDocumentation.txt