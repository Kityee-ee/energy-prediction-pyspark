# Building Energy Prediction with PySpark

## Overview
This project implements an **end-to-end scalable machine learning pipeline** to predict
**6-hour aggregated building energy consumption** using large-scale sensor, building
metadata, and weather data.

The pipeline is built using **PySpark DataFrames and Spark MLlib**, with an emphasis on
data engineering, feature construction, and model optimisation for energy forecasting
use cases such as grid planning and demand management.

---

## Problem Statement
Energy operators often collect **high-frequency meter data**, which is noisy and costly
to process for operational decision-making.

This project addresses that challenge by:
- Aggregating hourly energy readings into **6-hour intervals**
- Engineering **building, temporal, and weather-level features**
- Training scalable machine learning models to predict energy demand

---

## Architecture & Workflow

### 1. Data Loading
- Load large CSV datasets using explicitly defined Spark schemas
- Control partitioning to optimise distributed processing

### 2. Data Transformation
- Aggregate hourly meter readings into 6-hour intervals
- Handle multiple meter types (electricity, heating, cooling, steam)
- Clean and impute missing weather observations

### 3. Feature Engineering
- Building features (size, construction year, usage type)
- Temporal features (time interval, seasonality)
- Weather features (temperature, pressure, wind speed)
- Peak vs off-peak season classification

### 4. Exploratory Data Analysis
- Multivariate analysis across building categories
- Energy usage patterns across time intervals and seasons

### 5. Machine Learning
- Feature vectorisation using Spark ML pipelines
- Model training and evaluation with Spark MLlib
- Hyperparameter tuning for performance optimisation

---

## Key Insights
- Larger buildings generally consume more energy, but **building type introduces strong variability**
- Education and office buildings exhibit the **widest consumption ranges**
- Time-of-day alone is insufficient; **weather and usage type are critical predictors**

---

## Tech Stack
- **Python**
- **PySpark** (DataFrames, Spark SQL, Spark MLlib)
- **Jupyter Notebook**
- **Matplotlib / Seaborn** for visualisation