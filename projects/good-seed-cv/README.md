# Good Seed (Computer Vision)

The full project can be found [here](good-seed.ipynb)

## Introduction

The supermarket chain Good Seed would like to explore whether Data Science can help them adhere to alcohol laws by making sure they do not sell alcohol to people underage.

## Goal

Develop a model that identifies the age of a person based on an image. Return a model that predicts age with the lowest mean absolute average. 

## Key Findings

- Eliminates the need to manually identify the age of one-third of all customers that purchase alcohol.
- Predictions fall within 6.78 years off person's actual age on average.
- F1 score is better than constant at .89 with precision at 0.82
- Flaws: the model believes I am two years older than I am.



## Assumptions: 
- The distribution of the age of customers who purchase alcohol is similar to the distribition of the age of customers generally.
- 35% of all customers are aged 53 and above (according to statistica).

## Process

1. Prepare Data
    - Initialize packages
    - Load data
    
2. Exploratory Data Analysis
    - Assess distribution

3. Run Model
    - Load train
    - Load test
    - Create model
    - Train model

4. Draw Conclusions
    - How effective is the model?
    - How can it be used to save resources?
    - For fun: how old do I, my fiance, and my dogs look? 


## Data

7.5k photos with accompanying ages are saved in the `datasets/faces/` folder.


## Alternative Uses

This model could also help Good Seed financially by determining product demographics.

### Product Placement

Firstly, Good Seed could identify what products are being bought by each age group. For instance, Good Seed could identify certain products that are bought more by elderly people. As elderly people may require more help accessing products, the store could place these items closer to the front, making it easier for them to purchase items and incentivising shopping at Good Seed over other stores. 

### Supplier Marketing
Secondly, this information could also be useful for suppliers who might want to identify their target audiences. Good Seed could sell this information and charge for specific shelf spacing based on customer preferences.