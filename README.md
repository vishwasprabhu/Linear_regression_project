# Final project for linear regression analysis to perform Used-Cars-Price-Prediction

The notebook contains complete linear regression analysis carried out on the kaggle cars dataset. The pdf file provides complete explanations for the analysis. 
Dataset link: https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho?select=Car+details+v3.csv

# Introduction
Consumer demand for used cars has returned to pre-COVID-19 levels [1], resulting in a recent surge in used car prices [2]. This leads to the question: what are the stable factors that have a nontrivial influence on used car prices? In this project, we seek to identify predictors that have a significant impact on a used car’s sales price, as well as understand the relative impact of these predictors on a used car’s sales price.
To this end, we analyzed a dataset [3] containing multiple such features for cars manufactured by the automotive manufacturer Hyundai Motor Company. Based on our analysis, the factors which have a significant impact on a used Hyundai car’s price are: (i) age, (ii) mileage, (iii) mpg, (iv) engine size, (v) transmission, and (vi) fuel type.

# Description of Data
The dataset has 4860 rows and 9 columns, with the following variables:
  - "model": Hyundai model of the car.
  - "year": Year of registration for the car.
  - "price": Price of the car (in Euros).
  - "transmission": Car’s gearbox type.
  - "mileage": Distance used up by the car.
  - "fuelType": Type of engine fuel used by the car.
  - "tax": Road tax of the car.
  - "mpg": Miles per gallon, i.e., the distance per gallon the car can travel up to.
  - "engineSize": Engine size (in litres) of the car.

# Overview of Methodology
Our regression analysis was conducted via the following broad sequence of steps:
1. Check for multicollinearity in the data using the variance inflation factor (VIF) score of each predictor.
2. Fit a multiple linear regression model on the full data.
3. Check for influential points in the data using the Cook’s distance and externally studentized residual for every observation.
4. Check for (possible) heteroscedasticity using the Breusch-Pagan test.
5. Check for (possible) violation of normality using the Jarque-Bera test.
6. Select our most preferred model via the Best Subsets approach using, primarily, Akaike’s
information criterion (AIC) and Bayesian information criterion (BIC).

