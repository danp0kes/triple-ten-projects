# Megaline (Introduction to Machine Learning)
The loom overview can be found here and full python notebook project [here.](megaline-ml.ipynb)

## Introduction

Mobile carrier Megaline has found out that many of their subscribers use legacy plans. They want to develop a model that would analyze subscribers' behavior and recommend one of Megaline's newer plans: Smart or Ultra.

## Purpose

Develop the best model that recommends the more applicable phone plan with 75% accuracy on a test set.

## Data

Data was acquired from the previous megaline project found [here](./megaline-sda)

## Process

The following steps will be made:
- Read and Check Data
- Split Data
- Train Models:
    - Decision Trees
    - Random Forests
    - Logistic Regression
- Create Sanity Check
- Make Conclusions

## Key Findings

The random forest model (80.87%) performed better than both the decision tree (78.54%) and logistic regression (75.6%) models on the validation set. This was achieved by looping through hyperparameters that manipulated the number of estimators and depth of the forest.

On the test set, the random model achieved an accuracy of 79.9%. This was better than random chance as the sanity test saw a dummy model achieve an accuracy of 49.9%