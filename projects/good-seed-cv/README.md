# Good Seed (Computer Vision)

The full project can be found [here](good-seed.ipynb)

## Introduction

The supermarket chain Good Seed would like to explore whether Data Science can help them adhere to alcohol laws by making sure they do not sell alcohol to people underage.

# Good Seed - Computer Vision

The supermarket chain Good Seed would like to explore whether Data Science can help them adhere to alcohol laws by making sure they do not sell alcohol to people underage. The shops are equipped with cameras in the checkout area which are triggered when a person is buying alcohol.

## Goal

Develop a model that identifies the age of a person based on an image. Return a model that predicts age with a mean absolute average of below 8. 

## Process

1. Prepare Data
    - Initialize packages
    - Load data
    
2. Exploratory Data Analysis
    - Assess distribution

3. Run Model
    - Python script is created that performs training
    - Note that the model requires a GPU platform to run Tensorflow, resulting output is shared as markdown

4. Draw Conclusion


## Data

7.5k photos with accompanying ages are saved in an external folder.


## Key Findings

The model returns a mean absolute error of 6.37 on the validation set. This indicates that on average, predictions are 6.37 years off a person's actual age. This may seem like a large range, but becomes more useful when considering all provided ages range from 1 to 100.

Applying this model to the current needs of Good Seed to identify underage alcohol purchasing would be helpful. If the legal alcohol purchasing age is 21, those identified as 29 would likely be legally viable to do so. This works as even if the model is wrong, a person would on average be atleast over 22 years old (predicted age - mae). As the median age is 29, this would cut out the need to identify a large number of customers manually.

## Alternative Uses

This model could also help Good Seed financially by determining product demographics.

### Product Placement

 Firstly, Good Seed could identify what products are being bought by each age group. For instance, Good Seed could identify certain products that are bought more by elderly people. As elderly people may require more help accessing products, the store could place these items closer to the front, making it easier for them to purchase items and incentivising shopping at Good Seed over other stores. 

### Supplier Marketing
Secondly, this information could also be useful for suppliers who might want to identify their target audiences. Good Seed could sell this information and charge for specific shelf spacing based on customer preferences.