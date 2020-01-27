# Data_Analysis_for_Disaster_Mitigation_in_Australia

Please find the results here: 

https://docs.google.com/presentation/d/1batbCkVbhj-jlbZusftEJlaCyMZV3OKqPwo2XqPVta8/edit?usp=sharing

## Target:

- Prediction 1: Will there be rain tomorrow? (Binary Classification/Binary Clustering)

- Prediction 2: What is the probable amount of rain in mm to predict drought? (Regression)

## Data:

- 10 years’ of weather data (2007-2017) from 49 weather centers from 7 climate zones
source: https://www.kaggle.com/jsphyg/weather-dataset-rattle-package

- climate zone data
source: https://www.abcb.gov.au/Resources/Tools-Calculators/Climate-Zone-Map-Australia-Wide

-------------------------------------------------------------------------------------------
## Missing data imputation

Little’s test in R (I could not find anything in Python!) – identification of (MCAR/MCR/MCNR).
This is just a formal step before choosing any imputation method.

The possible choices for imputations:

- Delete the rows with NaN
- Median imputation for numerical data & mode imputation for categorical data
- Random imputation for numerical data & random imputation for categorical data
- Fast KNN data imputation for numerical data & mode imputation for categorical data ( $ pip install impyute)

## Identification and imputation of Outliers

The possible choices for detection of outliers:

- Z score (Z>3). If we use this we also need to perform Shapiro Wilk Test to validate the normality of the dataframe columns
- IQR score (3xIQR).

The possible choices for imputations

- min max capping

I am not very sure whether we can increase the accuracy of prediction by imputing the outliers. So far what I have done (with and without outliers), I did not observe any significant change - DB

## Dealing with the Data Imbalance

The possible choices:

- Random over sampling
- Synthetic Minority Over-Sampling Technique (SMOTE)
- Adaptive Synthetic (ADASYN)

## Feature Selection and Dimensionality Reduction

The possible choices:

- Correlation heat map
- Extra Tree Classifier
- SelectKBest and Chi2 test
- PCA for numerical data (feature scaling important)

Feature scaling(?)

## Training/Test Data Splitting

The possible choices:

- Random splitting (WY)
- Temporal splitting (DB)

## Binary Classification

The possible choices:

- Logistic Regreesion
- QDA
- LDA
- Random Forest
- AdaBoost
- SVM
  1. linear
  2. nonlinear
- NN - MLP
