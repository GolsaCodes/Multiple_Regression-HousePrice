# Boston Housing Price Prediction with Ridge Regression

## Overview

This project focuses on predicting house prices using the Boston Housing dataset. 
Ridge Regression model was developed with complete preprocessing and feature 
engineering pipeline, including scaling, polynomial feature generation, categorical 
encoding, and feature selection.

## Dataset

The project uses the Boston Housing dataset, which contains information about 
different properties and their surrounding areas. The target variable is `MEDV`, 
representing the median value of owner-occupied homes. Here is the link to the dataset: [Boston Housing Dataset](https://www.kaggle.com/code/prasadperera/the-boston-housing-dataset) from Kaggle.

### Preprocessing

Different preprocessing strategies were applied based on the characteristics of the features:

- Standardization using `StandardScaler`
- Polynomial feature generation (`degree=2`) for selected nonlinear features
- One-hot encoding of the `RAD` categorical feature
- Keep the binary `CHAS` feature unchanged
- Feature selection using `SelectKBest` with `f_regression`

## Model

Ridge Regression was used as the final regression model to reduce the risk of 
overfitting, particularly after polynomial feature expansion.

All preprocessing and modeling steps were combined into a Scikit-learn `Pipeline` 
to ensure that transformations were learned only from the training data and 
consistently applied to unseen data.

## Evaluation

The final model was evaluated on the held-out test set using:

- **R² Score**: 0.830701966633179
- **RMSE**: 3.5235302281081076

## Technologies

- Python
- NumPy
- Pandas
- Scikit-learn
- Ridge Regression
- Polynomial Features
- Feature Selection
