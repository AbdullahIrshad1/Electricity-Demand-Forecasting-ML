# Electricity-Demand-Forecasting-ML

End-to-end electric load forecasting system using clustering, anomaly detection, and machine learning models with a front-end dashboard for visualization and control.

---

## 🌟 Features

- **Demand Forecasting:** Predict future electricity demand using XGBoost and ensemble models.
- **Clustering Analysis:** Discover usage behavior with K-Means, HDBSCAN, and hierarchical clustering.
- **Interactive UI:** Modern React dashboard with intuitive controls and real-time charts.
- **Real-time Analytics:** Visualize trends, anomalies, and forecast accuracy dynamically.

---

## 📊 Project Overview

This project is designed to model and forecast electricity demand by combining historical consumption data with meteorological variables such as temperature, humidity, and wind speed. Powerful machine learning models and insightful visualizations help support grid stability and inform energy management decisions.

---

## 🔍 Why Electricity Demand Forecasting?

Accurate energy forecasting is essential for:

- **Grid Stability:** Maintaining balanced supply and demand.
- **Resource Optimization:** Minimizing cost and waste.
- **Renewable Integration:** Planning around intermittent energy sources.
- **Environmental Responsibility:** Supporting sustainability goals.
- **Economic Forecasting:** Planning infrastructure and budgeting for load fluctuations.

---

## 🛠️ Key Technologies

- **Backend:** FastAPI, Python, scikit-learn, XGBoost
- **Frontend:** React, Vite, Tailwind CSS, Shadcn UI
- **ML Models:** XGBoost, Random Forest, Stacking, LSTM
- **Data Processing:** Pandas, NumPy, SciPy
- **Visualization:** Recharts, D3.js

---

## 💻 User Interface

**Dashboard:**
- Select cities and date ranges.
- Choose between forecasting models.
- View actual vs. predicted electricity demand.
- Explore clustering visualizations.

**Dark Mode Support:**
- Full support for light and dark themes, focusing on accessibility and comfort.

**Analytics:**
- Track prediction error (MAE, RMSE, MAPE) across models.
- Visualize time-based energy patterns.

---

## 🔬 Technical Approach

**Data Processing Pipeline:**
- Data sources include EIA930 electricity demand and historical weather datasets.
- Preprocessing involves merging multiple JSON/CSV datasets by timestamp and city, handling missing values (interpolation, median fill), and feature engineering (cyclical hour encoding, lag features).
- Anomaly detection is performed using Isolation Forest, z-score, and IQR methods.

**Dimensionality Reduction:**
- Utilize PCA, t-SNE, and UMAP for visualization and improving clustering input.

---

## 🧠 Clustering Analysis

**Algorithms Used:**
- K-Means Clustering
- HDBSCAN
- Hierarchical Clustering with Dendrograms

**Cluster Evaluation:**
- Silhouette Score
- Cluster profiling (mean usage, time of day, temperature)

**Example Clusters:**
- Cluster 0: High-demand hot afternoons
- Cluster 1: Low-demand cool nights
- Cluster 2: Winter morning peaks
- Cluster 3: Weekend steady plateaus

---

## 🤖 Forecasting Models

**Target Variable:**
- 24-hour ahead forecast of hourly electricity demand

**Features:**
- Temperature, humidity, wind speed
- Hour of day, day of week, month
- Previous day’s demand at same hour

**Models Implemented:**
- XGBoost
- Random Forest
- Stacked Ensemble (XGBoost + RF)
- Linear Regression (baseline)
- LSTM Neural Network (optional)

---

## 📊 Evaluation Metrics

- MAE: Mean Absolute Error
- RMSE: Root Mean Square Error
- MAPE: Mean Absolute Percentage Error

**Baseline Comparisons:**
- Previous day’s same hour demand
- Previous week’s same hour/day demand

---

## 🧪 Training Strategy

- TimeSeriesSplit Cross-Validation
- GridSearchCV for model tuning
- Recursive Feature Elimination
- SHAP for interpretability (optional)

---
