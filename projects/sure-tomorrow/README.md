# Sure Tomorrow Insurance (Linear Algebra)

## Introduction

Sure Tomorrow, an insurance company wants to improve marketing to similar customers and predict how many claims a new customers will make. They wish to do so by keeping clients' interest in mind and protecting their personal data. 

## Goals
1. Find clients that are similar using kNN
2. Create a classification model that predicts if a client will claim a benefit or not
3. Create a regression model that predicts how many claims a client will claim
4. Hide client data using a mask and re-create above model

## Key Findings

### Scaling

Values in the scaled dataframe are more comparable. The closest value unscaled was one family member off, compared to someone with slightly more income in the scaled version. Overall, unscaled results are determined almost solely on income due to this features magnitude.

### Classification Model

The KNN classifier outperformed dummy models by an F1 differential of 0.70 suggesting the model is more effective than chance.

### Regression Model

Scaled and unscaled models yielded the same results with an RMSE and R2 score of 0.36 and 0.65 respectively. This indicates that a positive correlation exists between features and target, however, is not considered particularly strong.

### Data Masking

A random invertible matrix was created that was applied to client data to mask data. This ensured that gender, age, income and family members could be hidden in the modelling process. 

This was shown with an analytical proof that showed that predictions are the same with actual or obfuscated data:

The staring formula: $$w_P = [(XP)^T XP]^{-1} (XP)^T y$$
    
Simplify transposition with $(AB)^T = B^TA^T$:
    
$$w_P = [P^T X^T XP]^{-1} P^T X^T y $$
    
    
Apply inversion with $(AB)^{-1} = B^{-1} A^{-1}$):
    
$$w_P = P^{-1}[X^T X]^{-1} (P^T)^{-1} P^T X^T y $$
    
Apply identity matrix with $(P^T)^{-1} P^T = I$
   
$$w_P = P^{-1}[X^T X]^{-1} X^T y $$
    
Substitute $w = (X^T X)^{-1} X^T y$ $$w_P = P^{-1} w$$
    
Apply new weight to predictions of the new model:
    
$$\hat{y_P} = X'w_P = XPP^{-1}w = Xw = \hat{y}$$


Targets are kept constant allowing for no impact to RMSE measures and overall model quality.