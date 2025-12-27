# 🌧️ Precipitation Forecasting using XGBoost & Random Forest

This repository implements **machine learning models** for **precipitation forecasting** to support effective **water resource management**. The focus is on two robust tree-based ensemble models: **XGBoost** and **Random Forest**, both of which showed strong performance on time-series weather data.

---

## 📌 Project Overview
Accurate rainfall prediction is essential for irrigation planning, flood mitigation, and sustainable water usage. This project applies ensemble learning techniques on historical weather data to reduce forecasting error and improve reliability.

---

## 📊 Dataset
- **Time Period:** 2007 – 2020  
- **Data Type:** Historical weather and precipitation data  
- **Target Variable:** Precipitation (PCP)  
- **Features Include:**
  - Temperature
  - Humidity
  - Wind Speed
  - Calendar features (day, month, quarter, week of year)

---

## ⚙️ Data Preprocessing
- Handling missing values using imputation
- Feature scaling (where required)
- Creation of **lag features** to capture temporal dependency
- Time-based feature extraction for seasonality

---

## 🤖 Models Implemented

### 1️⃣ XGBoost
**XGBoost (Extreme Gradient Boosting)** is a powerful gradient-boosted tree algorithm known for speed and performance on structured data.

**Key Details:**
- Ensemble of decision trees with regularization
- Handles missing values automatically
- Supports parallel computation

**Training Strategy:**
- **Train/Test Split:** 80% / 20%
- **Cross-Validation:** TimeSeriesSplit
- **Evaluation Metric:** RMSE

**Hyperparameter Tuning:**
- Randomized Search
- Parameters tuned include:
  - `n_estimators`
  - `max_depth`
  - `learning_rate`
  - `min_child_weight`

**Advantages:**
- High predictive accuracy
- Captures non-linear patterns
- Provides feature importance

---

### 2️⃣ Random Forest
**Random Forest** uses bagging to train multiple decision trees on bootstrapped samples and averages their predictions.

**Key Details:**
- Reduces overfitting compared to single trees
- Uses random feature selection at each split

**Training Strategy:**
- **Train/Test Split:** 80% / 20%
- **Cross-Validation:** TimeSeriesSplit
- **Evaluation Metric:** RMSE

**Hyperparameter Tuning:**
- GridSearchCV
- Parameters tuned include:
  - `n_estimators`
  - `max_depth`
  - `min_samples_split`
  - `min_samples_leaf`

**Advantages:**
- Robust to noise and outliers
- Stable and interpretable
- Provides intrinsic feature importance

---

## 📈 Results Summary
- **XGBoost** achieved the **lowest RMSE**, making it the best-performing model
- **Random Forest** delivered consistent and reliable predictions
- Lag features and time-series validation significantly improved accuracy

---

## 🛠️ Tech Stack
- Python
- NumPy
- Pandas
- Scikit-learn
- XGBoost
- Matplotlib

---

## 👤 Author
**Sasidhar Reddy Navuluri**  
B.Tech, Electrical Engineering  
IIT Palakkad  

---

## 📄 License
This project is intended for academic and learning purposes.
