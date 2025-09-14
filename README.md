# AirQualityInsight: A Predictive Analysis of Urban Air Pollution in India 

## 1. Project Overview

### Problem Statement
Air pollution is a critical environmental and health issue across India. While extensive data is collected from hundreds of monitoring stations, it remains fragmented and complex. This makes it challenging for researchers, policymakers, and the public to understand long-term pollution trends, identify the most critically affected areas, and anticipate future air quality levels.

### Solution: AirQualityInsight
This project addresses the challenge by creating a unified and insightful analysis of air quality in India. It involves a comprehensive data engineering pipeline, in-depth exploratory data analysis, and the development of a machine learning model to forecast future pollution levels.

**Dataset:** The project utilizes the Time Series Air Quality Data of India (2010-2023) dataset from Kaggle, which contains hourly data from 454 monitoring stations.

---

## 2. Methodology
This project followed a structured four-phase data science workflow:

### Data Collection & Cleaning
- Consolidated 454 individual station files into a single master dataset of over 14 million records.
- Cleaned the data by handling missing values, standardizing the date format, and creating essential time-based and lag features for modeling.

### Exploratory Data Analysis (EDA)
- Performed a deep dive to visualize long-term trends, seasonal patterns, and spatial hotspots.
- Conducted a specific case study on the impact of the 2020 COVID-19 lockdown.

### Predictive Modeling
- Developed three machine learning models (Linear Regression, Decision Tree, and Random Forest) to forecast next-day PM2.5 levels.
- A time-aware split was used, training on historical data (2010-2021) and testing on future data (2022-2023) to simulate a real-world forecasting scenario.

### Driver Analysis & Conclusion
- Evaluated the models based on Mean Absolute Error (MAE) and R² metrics and used the best model (Random Forest) to identify the most significant features driving air pollution.

---

## 3. Key Insights from Exploratory Data Analysis

### Insight 1: Strong Seasonal Pollution Cycle
- Analysis reveals a clear and recurring "U-shaped" seasonal pattern. 
- Pollution peaks during the dry, cold winter months (November-January) and is lowest during the monsoon season (July-August) when rain washes pollutants from the atmosphere.

### Insight 2: The Impact of the 2020 COVID-19 Lockdown
- The nationwide lockdown provided a unique natural experiment.
- Analysis of daily PM2.5 levels in Delhi shows a dramatic and immediate drop during the peak lockdown period compared to the previous year (2019) and a clear rebound in 2021 as economic activity resumed.

---

## 4. Predictive Model Performance

| Model             | Mean Absolute Error (MAE) | R² Score |
|------------------|--------------------------|-----------|
| Linear Regression | 22.57                    | 0.75      |
| Decision Tree     | 31.80                    | 0.48      |
| Random Forest     | 20.88                    | 0.77      |

- The Random Forest model closely tracks the actual PM2.5 values on the unseen test data.
- Key Drivers of Pollution: Analysis of the Random Forest model's feature importances reveals that the most powerful predictor of today's pollution is the pollution level of the previous day, highlighting the persistent nature of air quality conditions.

---

## 5. Conclusion
This project demonstrates a complete end-to-end approach to air quality analysis and prediction in India. The insights and predictive model can help policymakers, researchers, and the public to make informed decisions to mitigate pollution and protect public health.
