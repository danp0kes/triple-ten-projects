# Film Junky (Machine Learning with Texts)

The full project can be found [here](film-junky.ipynb)

## Project Statement

The Film Junky Union, a new edgy community for classic movie enthusiasts, is developing a system for filtering and categorizing movie reviews. The goal is to train a model to automatically detect negative reviews. IMDB movie reviews with polarity labelling will be used to build a model for classifying positive and negative reviews.

## Purpose 

Predict negative reviews from the IMDB with a model that is atleast 85% accurate.

## Findings

- Performed exploratory data analysis to find determine best model would be a text based interpreter
- Created a model that was 88% accurate on 23,000 text entries
- Determined best lemmatization process, increasing accuracy by 2% across models

## Process

### 1. Preparation
- Load the data.
- Preprocess data.
- Conduct an EDA and make conclusions on class imbalances.

### 2. Modelling
- Preprocess the data for modeling.
- Train three different models for the given train dataset.
    1. NLTK and Linear Regression
    2. spaCy and Linear Regression
    3. spaCy and Gradient Boosting (XGB)
- Test the models for the given test dataset.

### 3. Testing
- Compose own reviews and classify them with all the models.
- Check for differences between the testing results of models.
- Present findings.


## Data

Data has been provided by TripleTen and can be found in the Data folder. It contains 47k rows about IMDB reviews.