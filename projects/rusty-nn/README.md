# Rusty Bargains (Neural Networks)

The full project can be found [here](rusty-nn.ipynb)

## Introduction

Rusty Bargain, a used car company, is developing an app to help customers predict the market value of their own car. By giving historical data of technical specifications and prices, they hope we can find a model that is accurate and time efficient.


## Data

The data was provided by TripleTen

## Process

The modelling process includes the following three steps:

1. Data Preparation
2. Model Training
3. Model Analysis

## Preparation

The data will first be prepared. This will include:
- Importing packages
- Reading the dataframe
- Inspecting the dataframe
- Converting datatypes
- Dropping unnecessary columns
- Handling missing data
- Encoding data

## Training

Training will be done on four different models:

- Linear regression (1 model)
- Random forest (1 model)
- Gradient descent (2 models)

Each will require splitting data and training according to their specific hyperparameters.

## Analysis

Model efficiency will be compared. This can be broken down to how accurate and how quick the model is. Accuracy will be measured with reference to the root of the mean square error (RMSE). The lower the number, the better. Each model will also be evaluated by how long each model takes along with how long the best model takes whilst iterating through hyperparameters.

## Key Findings

### Accuracy

A gradient boosting model (LGBM) performed best among other models, achieving an RMSE of 1586.68. This indicates that, on average, the predicted car values deviate from the true values by approximately `$1,586`. This compares to RMSE values of 1660, 1781.69, and 2665.65 of the CatBoost, Random Forest, and Linear Regression models.

### Speed

To train the LGBM model, training time was minimal at 8.03 seconds which is faster than the CatBoost (10.31 seconds) and Random Forest (21.86 seconds) models. The Linear Regression model was faster, however, much more inaccurate.

### Test Set

When applying the LGBM model to the test set, RMSE decreased slightly to 1623.92 but retained a faster training time at 8.6 seconds. 