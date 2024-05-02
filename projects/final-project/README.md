# Final Project

## Introduction

In an increasingly competitive telecommunications landscape, retaining customers is paramount for sustained growth and profitability. To address this challenge, Interconnect, a prominent telecom operator, seeks to implement a proactive churn management strategy. By leveraging advanced data analytics techniques, Interconnect aims to forecast customer churn and intervene with targeted retention efforts.

The full project can be found [here](final_project.ipynb).

## Goal

Create a model that utilizes Interconnect's rich repository of customer data, encompassing information about their plans, contracts, and demographic details. 

## Process

Through sophisticated predictive modeling, we aim to identify subtle patterns and indicators that precede customer churn. By detecting early signals of customer dissatisfaction, Interconnect can deploy timely interventions such as promotional codes and tailored plan options to mitigate churn risk and foster long-term customer loyalty. This project will do so by completing the following steps:

1. Load Data
2. Prepare Data
3. Perform Exploratory Data Analysis
4. Pre-process Data
5. Create Model
6. Draw conclusions


## Key Findings

- The target distribution was highly imbalanced, mitigated by sampling techniques (especially random oversampling)
- Feature engineering was key to obtaining high F1 scores, particularly by enriching data with member duration days.
- Gradient boosting models outperformed logistic regression and random forests models

## Final Model

The model that returned the highest AUC-ROC score was the CatBoost Model at 0.929 on the test set. This model used the random over sampler dataset with a learning rate of 0.05, iterated over 2000 times. 


