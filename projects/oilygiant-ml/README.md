# Oily Giant Mining Company (Machine Learning in Business)

Check out the full project [here](oilygiant.ipynb)

## Introduction

Oily Giant Mining Company is seeking the ideal place for a new oil well. A model will predict which of the three regions will produce the greatest profit that overcomes their `$100 million` budget. Oily Giant also wishes to eliminate risk of investing in wells that pose risks.

## Goals
- Profitabiltiy: Find the region that will produce the most profit
- Risk: Eliminate regions that have a loss probability above 2.5%

## Data Description

Three datasets from oil samples within three regions have been provided in the datasets folder. For each the following parameters are given:

`id:` unique oil well identifier

`f0, f1, f2:` three undisclosed features of significance

`product:` volume of reserves in the oil well (thousand barrels)

Potential profits and risks will be identified using the bootstrapping method.

## Process

The process will include five distinct steps:
1. Data Preparation
2. Model training and testing
3. Prepare data for profit calculation
4. Calculate profit from a set of selected oil wells and model predictions
5. Calculate risks and profit for each region

## Key Findings
- The breakeven point was determined to be 111,111 barrels of oil. This was much higher than the initial averages for all three regions.

- A profit function was created that found the actual volume of wells from the predicted model. Region 1 showed the most promise with a maximum potential profit of around `$33 million`.

- Bootstrapping produced results that suggested the risk of Region 3 was too high. Region 2 was chosen as the recommended region due to its high profit of `$6.7 million`.