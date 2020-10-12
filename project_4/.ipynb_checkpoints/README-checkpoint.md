# Project 4: Predicting Income Bracket of Citizens with their Demographic Backgrounds

# Problem Statement
​
In this project we seek to identify individuals who have an income above $50,000 per year using information about their education, family, age, occupation and nationality. We will use a limited dataset to train classification models and determine the best predictors and models.
​
# Data Description
​
Data was gathered by the U.S. Census Bureau in 1994. A limited sample of this data was used for this analysis.
​
#### Data Dictionary:
​
|Feature|Type|Description|
|---|---|---|
|age|int|Age, in years|
|workclass|string|The type of entity for which a person works|
|fnlwgt|int|The total number of U.S. residents estimated to fall into this category|
|education|string|The highest level of education a person has achieved|
|education-num|int|'education' feature mapped to integers|
|marital-status|string|Marital status|
|occupation|string|Occupation|
|relationship|string|A person's position within their family|
|sex|int|Binarized values for sex; 0 for Female, 1 for Male|
|capital-gain|int|capital gains|
|capital-loss|int|capital losses|
|hours-per-week|int|Number of hours worked per week|
|native-country|int|Binzarized native country values; 0 for immigrant, 1 for native-born|
|wage|int|Binarized values indicating wage; 0 for <=50K, 1 for > 50K|
​
​
# Executive Summary
​
Data was cleaned and dummified. Native country data was binarized to 1 for US native and 0 for otherwise. Engineered features were tested but none were used in the final models. Models fit were Decision Tree, Random Forest, Extra Trees, Logistic Regression, K-Nearest Neighbors, SVC, GradientBoost, and AdaBoost. All models were tested with bagging classifiers for bootstrapping after optimizing individually on non-bootstrapped train/test splits. Bootstrapping was weighted using the 'fnlwgt' column of the data in order to get a sample that is better representative of the population.
​
|                    | Decision Tree      | Random Forest      | Extra Trees        | Logistic Regression | KNN                | SVC                | AdaBoost           | Gradient Boost     | Naive-Bayes        |
|--------------------|--------------------|--------------------|--------------------|---------------------|--------------------|--------------------|--------------------|--------------------|--------------------|
| Train Score        | 0.8673218673218673 | 0.9232186732186732 | 0.895986895986896  | 0.855036855036855   | 0.8368140868140869 | 0.8693693693693694 | 0.8560606060606061 | 0.8931203931203932 | 0.7811220311220312 |
| Test Score         | 0.8551258440761204 | 0.8655616942909761 | 0.8354818907305095 | 0.8471454880294659  | 0.8170656844689994 | 0.8440761203192142 | 0.8557397176181707 | 0.8686310620012277 | 0.7833026396562308 |
| Bagged Train Score | 0.8734643734643734 | 0.9037674037674037 | 0.8705978705978706 | 0.8533988533988534  | 0.842956592956593  |                    |                    |                    |                    |
| Bagged Test Score  | 0.856353591160221  | 0.8465316144874155 | 0.8268876611418048 | 0.8428483732351135  | 0.8084714548802947 |                    |                    |                    |                    |
​
# Visualizations
​
1. Decision Tree Confusion Matrix
​
<img src='images/dt_conf.png'>
​
2. Gradient Boost Confusion Matrix 
​
<img src='images/gboost_conf.png'>
​
3. Gradient Boost ROC Curve 
​
<img src='images/gboost_roc.png'>
​
# Conclusions
​
The best models for this data were GradientBoost and Random Forest. GradientBoost was preferred for its low variance and high rate of true positive predictions. Education, Profession, and Marital Status were important features of prediction, while age and nationality were of less importance. One particularly good predictor was capital gains, as those with capital gains were signficantly more likely to make the 50,000 threshold, especially as capital gains rose over 5000. Using the provided weighting column to weight bootstrapped samples slightly improved the accuracy of our predictions.
Collapse
