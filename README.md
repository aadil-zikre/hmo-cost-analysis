# hmo-cost-analysis
A comprehensive approach to predicting whether a customer is going to spend a significant amount on healthcare in the following year. This dataset is done on a fictional dataset that was provided by Syracuse University as part of Intro to DS Course. 

## Directory Structure 

```
- models                      # folder that contains all the exported trained models
- hmo_project_final.r         # EDA for the dataset and training several Binary Classifiers
- app.r                       # Source Code for a demo shiny app
```

## Contents
### hmo_project_final.r

Following things can be found in this notebook
1. Exploratory data analysis for all variables in the dataset. GGPlot is used for the visualization of the features
2. Conversion of a continuous variable, cost into a binary variable expensive based on a threshold which is derived from real life analysis of spends. 
3. Building and Rebuilding Models with different features and hyperparameters. Following Models were built:
    1. Logistic Classifier Model 
    2. Probit Classifier Model
    3. Support Vector Classifier Model
    4. Neural Network Classifier
    5. Decision Tree Classifier
    6. Random Forest Classifier
4. Models were compared on the basis of Sensitivity and Specificity. Best Model was Random Forest with a Sensitivity of 0.96 and Specificity of 0.64.

### app.r

This is a file for making a R Shiny Application. The Application is a simple page that lists all the features and user (Our Target User was Receptionist) can input all the details to get a prediction which would be a Yes or No for next year spend. With this prediction they can decide on the best plan for the customer. The app also gives an option to try several models but we recommend only the best model to be deployed in Production. 

## Conclusion 

The goal of the project was to build a binary classifier to predict whether a customer is going to spend a significant amount on healthcare on various factors such as smoker, location, location_type, education_level, yearly_physical, exercise, married, hypertension and gender. Various Predictive Models were built and Random Forest was the best of them on the basis of its specificity and sensitivity. The analysis also revealed smoking to be the most important factor at determing the healthcare spend. So, as an advice to HMO, we recommend that they pay more attention to their customers who are more prone to smoking addiction and just smoking in general.
