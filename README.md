# Homelessness

# Purpose of Project: 
The purpose of this project is to identify market factors that have established effects on homelessness and to construct/evaluate empirical models of community-level homelessness

# Requirements: 
The Software used was google colab

# Data Used: 
The first data set used was 05b_analysis_file_update.csv which is a CSV file of factors believed to influence homelessness across communities from 2010 - 2017. The data dictionary HUD TO3 - 05b Analysis File - Data - Dictionary.csv is a centralized repository of information about data such as meaning, relationships to other data, origin, usage, and format. 

Both data sets can be found in the repository 
1. "05b_analysis_file_update.csv" 
2. "HUD TO3 - 05b Analysis File - Data - Dictionary.csv" 

# Data Preparation: 
The file preparing the data is called: 
Bayan_Farag_DATA_3320_Homelessness_Data_Preparation.ipynb. The output file is called df(4).csv 

The standard data cleaning process involves several important steps. Firstly, the source of the data must be identified and all necessary links to data sources provided. The contents of each data set should be inspected for issues such as duplicates, missing values, outliers, and data type inconsistencies. We have improved the data by renaming the original data names to make them more understandable. Additionally, due to substantial missing data for certain years, we have chosen to focus on the year 2017 as it contains all the necessary data. In the dataframe we have introduced three new variables: rate_homeless, rate_sheltered, and rate_unsheltered. These variables represent the counts per 10,000 people in the population. To calculate these rates, we divided the total count by the population size for each respective category. Furthermore, we have transformed the variables race, gender, and age into percentages rather than absolute totals. This change provides a more meaningful representation of the data by showing the proportions within each category. Finally we created df(1).csv. This file will be used in the analysis in the project & can be found the the repository. 

# Data Analysis: 
The file analyzing the data is called: Bayan Farag DATA 3320 Homelessness Analysis .ipynb

To begin the analysis, the dataset was divided into test and train splits for model evaluation. The predictor data was scaled to ensure consistent ranges across variables. Next, an ordinary least squares (OLS) model was created to establish a baseline. Additionally, k-fold cross-validation testing was performed on Ridge, Lasso, and XGBoost models. The root mean square error (RMSE) was used as an evaluation metric to assess the effectiveness of each model. The lower the RMSE value, the better the model's predictive performance. While on the other hand the higher value of the RSMSE values means less effective prediction. For our additonal step I decided to investigating whether the density of different areas (such as major cities, suburban regions, and rural areas) has an impact on their respective rates of homelessness and plotted it using the Lasso model. 

# License: 
The materials in this repository are available for reuse, with proper credit attribution to the original author. Feel free to utilize the content in your own projects, research, or any other endeavors.


