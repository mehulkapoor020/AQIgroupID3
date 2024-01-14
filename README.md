# AQI Data Mining Project

**Team members:** Mehul And Abhishek

**Code:** [Data Mining Python Code](Random_forest_SVR_And_LSTM_AQIDataMining.ipynb)

**Project Report:** [Project Report](AQI_Report_MehulKapoor.pdf)

The Air Quality Monitoring Data, which offers a helpful insight into the air we breathe, is accessible through the [data.act.gov.au](https://www.data.act.gov.au/Environment/Air-Quality-Monitoring-Data/94a5-zqnn) platform. This programme demonstrates the value of using data to inform decision-making while addressing environmental problems and fostering healthier communities.

## Abstract

The Air Quality Index (AQI) is a vital indicator of environmental health, reflecting air pollution levels and their impact on public health. Accurate AQI evaluation/prediction is essential for mitigating health risks and formulating environmental policies, especially in urban areas like the City of Monash, New Zealand. This project employs four machine learning models – Random Forest, Support Vector Machine (SVM), an ensemble of Random Forest and SVM, and a Long Short-Term Memory (LSTM) model – to forecast AQI accurately. These models were chosen for their diverse strengths in handling complex environmental data. Our study reveals that the Random Forest model outperforms the others in evaluating AQI with higher accuracy and reliability. It efficiently captures the intricate relationships between pollutants and atmospheric conditions, making it a robust tool for air quality evaluation. The insights gained from this study are crucial for public health advisories and urban environmental management, demonstrating the potential of machine learning in tackling environmental challenges.

**Original Data source:** [Air Quality Monitoring Data](https://www.data.act.gov.au/Environment/Air-Quality-Monitoring-Data/94a5-zqnn)

**Cleaned Data:** [Cleaned Air Quality Monitoring Data](Cleaned_AQI_Data.csv)

## Data Preprocessing

1. The dataset was sorted chronologically before the following preprocessing steps were performed.

2. **Data Cleaning (Missing Values):** Since our dataset is organized chronologically in an hourly manner, the missing values were replaced with the previous hour’s values because the particle concentration (NO2, O3, etc.) has minimum variation from one hour to the next, meaning they tend to have similar values in both hours.

3. **Data Cleaning (Outliers):** The Outliers were identified using the IQR algorithm and dropped, which were then replaced by the previous hour’s values.

4. **Data Reduction:** Of the initial 3 regions Civic, Monash, and Florey, Civic and Florey were dropped as Civic had null values for NO2 and CO attributes, whereas no data was available for Florey from 2011 to 2014. Also GPS, Date, and Time attributes were also dropped.

5. **Data Transformation:** The attributes ‘Date’ and ‘Time’ of datatype ‘object’ were combined to form ‘DateTime’ attribute with the datatype as same, i.e., datatype ‘DateTime’.

## Data Training and Testing with Machine Learning Models

1. Random Forest Regressor
2. Support Vector Regression
3. Ensemble Model (Random Forest and SVR)
4. Long Short-Term Memory

## Model Evaluation

1. MAE
2. MSE
3. RMSE
