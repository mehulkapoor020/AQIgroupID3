AQI Data Maining Project
Team members: Mehul And Abhishek

The Air Quality Monitoring Data, which offers a helpful insight into the air we breathe, is accessible through the data.act.gov.au platform. This programme demonstrates the value of using data to inform decision-making while addressing environmental problems and fostering healthier communities.

Original Data source: https://www.data.act.gov.au/Environment/Air-Quality-Monitoring-Data/94a5-zqnn


Data preprocessing:

1. The dataset was sorted chronologically before the following preprocessing steps were performed

2. Data Cleaning (Missing Values) :  Since our dataset is organized chronologically in an hourly manner, the missing values were replaced with previous hour’s values because the particle concentration (NO2,O3,etc) has minimum variation from one hour to the next, meaning they tend to have similar values in both hours.

3. Data Cleaning (Outliers) :  The Outliers were identified using the IQR algorithm and dropped, which were then replaced by the previous hour’s values.
Data Reduction :  Of the initial 3 regions Civic, Monash and Florey,  Civic and Florey were dropped as Civic had null values for NO2 and CO attributes, whereas no data was available for Florey from 2011 to 2014.  Also GPS, Date and Time attributes were also dropped.

4. Data Transformation :  The attributes ‘Date’ and ‘Time’ of datatype ‘object’, were combined to form ‘DateTime’ attribute with the datatype as same, i.e, datatype ‘DateTime’.

Data Training and Testing with Machine Learning models:

1. Random Forest Regressor
2. Support Vector Regression
3. Ensemble Model (Random Forest and SVR) 
4. Long Short-Term Memory

Model Evaluation:
1. MAE
2. MSE
3. RMSE
