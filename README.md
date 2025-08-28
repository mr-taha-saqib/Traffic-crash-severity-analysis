# 🚦 Traffic Crash Injury Prediction – Chicago Dataset  

## 📌 Objective  
This project aims to predict whether a traffic crash results in injury using a historical dataset from **Chicago traffic crashes**.  
By analyzing environmental, vehicular, and situational attributes (e.g., weather, lighting, control devices), we build machine learning models to forecast injury outcomes and support proactive safety measures.  

## 📊 Dataset Introduction  
The dataset contains **235,978 records** with **48 features**, including:  
- Crash details (date, hour, day of week, month)  
- Environmental conditions (weather, lighting, roadway surface)  
- Vehicular factors (posted speed limit, traffic control device, road alignment)  
- Injury outcomes (fatal, incapacitating, non-incapacitating, reported/not evident, unknown)  

The target variable is engineered as a **binary classification label (`HAS_INJURY`)**:  
- `1` → At least one injury reported  
- `0` → No injury  

## 🛠️ Project Workflow  

### 1. Data Loading & Inspection  
- Load CSV dataset with `pandas`  
- Inspect shape, data types, missing values, and descriptive statistics  

### 2. Data Cleaning & Preprocessing  
- Handle missing values (mode for categorical, median for numeric)  
- Remove duplicates and invalid entries (e.g., unrealistic speed limits)  
- Handle outliers using **IQR method**  
- Drop irrelevant or leakage columns (detailed injury breakdowns, crash IDs)  

### 3. Exploratory Data Analysis (EDA)  
- Distribution of crashes under different weather & lighting conditions  
- Correlation analysis between numeric features  
- Visualization with **matplotlib** & **seaborn**  

### 4. Feature Engineering  
- One-hot encode categorical features (`WEATHER_CONDITION`, `LIGHTING_CONDITION`, `TRAFFIC_CONTROL_DEVICE`)  
- Extract crash year from `CRASH_DATE`  
- Create binary target variable: `HAS_INJURY`  

### 5. Modeling  
Implemented models include:  
- **Logistic Regression**  
- **Ridge Regression**  
- **Random Forest Classifier**  

Metrics used:  
- Accuracy  
- Confusion Matrix  
- Classification Report  
