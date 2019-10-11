# Ames_Housing
A model to predict housing prices in Ames

Problem Statement
For this project, I have two goals:

    1) Determine the best model for predicting Sale Price for houses in Ames using up to 25 features from the data set
    2) Determine what the most important features are for said prediction
    
Specifically, we want a model that has high predictive power (R2 > 0.8), but generalizes well to new data. Furthermore, we want to select a reasonable (<25) number of features to ensure that the model does not become too complicated or overfitted


Project Contents
- 1. Executive Summary
    - Problem_Statement
- 2. Data Dictionary
- 3. Data Import and Cleaning
    - 3.1 Library Imports
    - 3.2 Data Imports
    - 3.3 Overview of Imported Data
    - 3.4 Functions and Pipelines for Cleaning 
    - 3.5 Data Cleaning
- 4. Exploratory Data Analysis
    - 4.1 Distribution Visualizations  
        - 4.1.1 Histograms
        - 4.1.2 Bar Plots
        - 4.1.3 Box Plots
    - 4.2 Correlation Visualizations
        - 4.2.1 Scatter Plots
        - 4.2.2 Heatmaps
- 5. Encoding and Preprocessing 
    - 5.1 Removing Outliers
    - 5.2 Encoding Dichotomous Variables
    - 5.3 Get Dummies
- 6. Data Export  
- 7. Model Benchmarks
- 8. Feature Selection
    - 8.1 Filter Method
    - 8.2 Embedded Method
    - 8.3 Wrapper Method
    - 8.4 Analysis of Features
    - 8.5 Assessing Multicollinearity
 - 9. Modelling and Tuning
    - 9.1 Ridge
    - 9.2 Lasso
    - 9.3 ElasticNet
    - 9.4 Polynomial ElasticNet
    - 9.5 Analysis of Model
 -10. Conclusion
 
 Summary of Findings

RSquared
Filter	Embedded	Wrapper	Combined
Ridge	0.87	0.89	0.89	0.86
Lasso	0.87	0.90	0.89	0.86
Enet	0.87	0.90	0.89	0.86
Poly Enet	-	0.93	-	0.90

MSE
Filter	Embedded	Wrapper	Combined
Ridge	7.65264e+08	6.121902e+08	6.43408e+08	8.357110e+08
Lasso	7.62479e+08	6.164244e+08	6.36612e+08	8.315334e+08
Enet	7.67292e+08	6.170996e+08	6.33163e+08	8.611059e+08
Poly Enet	-	6.694659e+08	-	5.929756e+08

Conclusion
There are three main findings:

    1) For feature selection, the intersection between the three feature selection methods yielded the features with the 
       highest predictive power.
       
    2) Polynomials were needed to factor in correlations between the independent variables, and this led to a problem of 
       over dimensionality. Using a smaller list yielded as much predictive power as using 25! features.
    
    3) The ElasticNet model was the best performing in terms of both R2 and MSE.
