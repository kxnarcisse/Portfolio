# Predicting Housing Market
![what-is-my-home-worth-1](https://user-images.githubusercontent.com/77252878/141031939-d4ab10ad-fafe-4dc2-b069-aac5a25b4270.jpg)




## Problem Definition:
The purpose of this project is to make a predictive pricing model based on given known features and square footage. The low inventory and high competition in the Seattle housing market make it difficult for homebuyers to find a place to call home. Increasing single-family home prices have resulted from a widespread housing boom fueled by historically low-interest rates and a scarcity of available properties, making homeownership out of reach for more people. As more millennials enter the market, the demand crunch will intensify. From the supply and demand standpoint, Seattle's housing market is currently one of the most inequitably balanced in the United States. Many homes get multiple offers, some with waived contingencies.

There's not enough supply to keep up. Growing demand is expected to continue due to a lack of new construction entering the market in suburban areas following years of underdevelopment. With interest rates remaining at historically low levels and a supply of homes available for sale in the region of less than one month, the perfect storm for rising house prices will continue, albeit perhaps not quite as ferociously as previously.

What you get to see are record-breaking housing prices and record-breaking low inventory. Seattle's housing market is driven by employees of local tech businesses like Amazon and Microsoft and corporations with significant operations in the vicinity like Google and Facebook. Many of them didn't want to work remotely in small apartments during the epidemic, so they sought spacious homes with office areas. Most of them have the financial means to compete with other buyers and raise home selling prices.


## Dataset:
This dataset contains house sale prices for King County, which includes Seattle. 
** https://www.kaggle.com/harlfoxem/housesalesprediction

## Features Description:

  •    id: unique identifier    
  •    date: Date house was sold    
  •    price: Price is (Target variable)    
  •    bedrooms: Number of Bedrooms/House   
  •    bathrooms: Number of bathrooms/bedrooms    
  •    sqft_living: square footage of the home    
  •    sqft_lot: square footage of the lot    
  •    floors :Total floors in the home   
  •    waterfront :Home with a view to a waterfront   
  •    view: Has been viewed by buyers    
  •    condition: Home condition    
  •    grade: overall grade given to the housing unit, based on King County grading system    
  •    sqft_above: square footage of home apart from basement   
  •    sqft_basement: square footage of the basement    
  •    yr_built: Year home was built    
  •    yr_renovated: Year when home was renovated   
  •    zipcode: zip code    
  •    lat: Latitude coordinate   
  •    long: Longitude coordinate   
  •    sqft_living15: Living room area in 2015 (implies-- with some renovations)    
  •    sqft_lot15: lot-size area in 2015 (implies-- with some renovations)


## Data Wrangling

### Cleaning
![image](https://user-images.githubusercontent.com/77252878/141161570-90e9971c-e94d-40a2-83a7-4dd4c65ffaf8.png)

![image](https://user-images.githubusercontent.com/77252878/141162081-a146976c-d95d-4018-82a8-8ff2fd954405.png)

## Explanatory Data Analysis:
**[EDA Notebook](https://github.com/kxnarcisse/Springboard/blob/master/Git/Notebooks//housing_market/Housing%20Market%20_%20Data%20Wrangling%20and%20EDA%20Work.ipynb)**

Check for outliers. Calculated the quantile value for 75% and 25%, the value above 75% tend to be outliers. 

![image](https://user-images.githubusercontent.com/77252878/141163491-6bec37fb-6b1b-4dd9-97ed-814a3a26fe81.png)
### Fig 1.2 Price – target variable

![image](https://user-images.githubusercontent.com/77252878/141164117-ba571faf-252b-4983-8b4c-196860e6d33d.png)

![image](https://user-images.githubusercontent.com/77252878/141164453-d76b5f12-7d51-4f7a-b60e-5a5c9ae33c3a.png)

![image](https://user-images.githubusercontent.com/77252878/141164641-970e30c9-f5f8-4445-a58f-8fee17ed60f6.png)

## Checked for correlation:
![image](https://user-images.githubusercontent.com/77252878/141165275-ca95655d-ab33-4ce6-8676-ba82efe9d36d.png)

## Algorithms & Machine Learning:

### Feature Engineering - Machine Learning - Classification

**[Classification Machine Learning Notebook](https://github.com/kxnarcisse/Portfolio/blob/master/Git/Notebooks/housing_market/modeling_housing_market_classification_model.ipynb)**

### Predictive models
Random Forest   
K nearest neighbors

### Split the X and y into 70/30 training and testing data subsets
![image](https://user-images.githubusercontent.com/77252878/141166368-a0a532a9-02e7-4221-b68c-cc804e0bca52.png)

![image](https://user-images.githubusercontent.com/77252878/141166543-4e6b8c57-fc39-4cb3-ab87-e1dc8ae2005c.png)

## K Nearest Neighbors
![image](https://user-images.githubusercontent.com/77252878/141166954-0f77f4bd-f316-4357-84d2-2e0f1765ff7f.png)

![image](https://user-images.githubusercontent.com/77252878/141167261-d6a0594f-268d-4f7f-97d1-c03b2a2ecff6.png)

### NOTE: Confusion Matrix Break down
N = 6431

TN & FN is the Predicted NO

FP & TP is the Predicted YES

Accuracy: (TN+TP)/N (4537 + 719)/6431 = 82%

Misclassification Rate: (FP +FN)/N (937 + 238)/6431 = 0.18%



### Feature Engineering - Machine Learning - Regression

**[Regression Machine Learning Notebook](https://github.com/kxnarcisse/Portfolio/blob/master/Git/Notebooks/housing_market/modeling_housing_market_regression_model.ipynb)**


### Predictive models

Linear Regression
Random Forest   


### Linear Regression
![image](https://user-images.githubusercontent.com/77252878/141168726-51687b69-2d24-4f9c-994d-48ce347ded67.png)

### Random Forest
![image](https://user-images.githubusercontent.com/77252878/141168931-6a25a019-8272-43d7-9306-bcaa2498ab2b.png)

## Predicted Result:
![image](https://user-images.githubusercontent.com/77252878/141169174-993bf832-9975-4ab2-b6c8-d3c8c67572eb.png)

## Feature importance:
![image](https://user-images.githubusercontent.com/77252878/141169396-49f18c35-c144-4550-b1a0-0df1012770e0.png)

### Summary:
Scaling the features, generating new features with KNN model with hyperparameter tuning led to the most accurate predictions with the least missclassification. The result was a score of 82% accuracy. This model can be used as a guide when determining house price estimates for Seattle since it leads to reasonable predictions.




