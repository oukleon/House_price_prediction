# House-price-prediction

## Overview
House price prediction
1.5k training set with 81 features (www.kaggle.com)
Dataset includes conditions & location information of the houses with the price.
The aim of this project produces accurate prediction of the price that helps for buyers to know the house price is overvalued, undervalued or fair.  
### Data Preprocessing
Dropped irrelavent features and features with over 90% of one value -> Followed up study showed that without feature selection brought better performance with some regressors. For example, linear regression or linear based regression gave horrible results without feature selections, but another regressors, like gradientboosting or random forest actually improved scores without selection

### Training regressors
```
Using linear regressor as a baseline model. 
ElasticNet
RandomForest(RF)
LGBM
XGB
GBR
VotingRegressor with RF,LGBM,XGB and GBR

XGB got the best in training data, but overfitting
GBR had the best score in validation set, but second best in testset.
Voting Regressor got the best one in testset.
```
