# House-price-prediction
## Overview
- House price prediction  
- 1.5k training set with 81 features (www.kaggle.com)  
- Dataset includes conditions & location information of the houses with the price (a target variable).  
- The aim of this project produces accurate prediction of the price that helps for buyers to know the house price is overvalued, undervalued or fair.  

## Data Preprocessing
- Analyze 81 features
- Dropped irrelavent features, duplicated features, and features with over 90% of one value -> Followed up study showed that without feature selection brought better performance with some regressors. For example, linear regression or linear based regression gave lower scores without feature selections, whereas another regressors, like gradientboosting or random forest, actually improved scores without selection
- Handling NA values
- Heatmap after preprocessing (2 heatmaps to better visualizing)
![heatmap](https://user-images.githubusercontent.com/54334941/144773608-b05661a1-a3ef-4942-88eb-1762454f10e5.png)

![heatmap2](https://user-images.githubusercontent.com/54334941/144773619-00c9e95d-bea3-4322-9ceb-0cc167e53a22.png)

- 0 Na values

![navalues](https://user-images.githubusercontent.com/54334941/144773755-f367c0d0-bffa-415b-b6a8-239c26e8dc01.png)


## Training regressors
```
Using linear regressor as a baseline model. 
ElasticNet
RandomForest(RF)
LGBM
XGB
GBR
VotingRegressor with RF,LGBM,XGB and GBR
```
- XGB got the best in training data, but overfitting

![xgb1](https://user-images.githubusercontent.com/54334941/144774043-8b1f5f9e-9539-4f89-942a-e097c3783fcb.png)

![xgb2](https://user-images.githubusercontent.com/54334941/144774047-ba75cea9-adfb-4dc9-b7b0-124f0f100462.png)

- GBR had the best score in validation set, but second best in an actual testset in kaggle server.

![gbr](https://user-images.githubusercontent.com/54334941/144774049-c7217e44-7dd4-44fc-9202-3016d5dce324.png)

- Voting Regressor got the best one in a testset.

![ensemble](https://user-images.githubusercontent.com/54334941/144774053-3f9188d7-61d1-4474-b6ad-7ff90c7cf260.png)
