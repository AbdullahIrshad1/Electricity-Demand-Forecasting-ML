# Electricity-Demand-Forecasting-ML
End-to-end electric load forecasting system using clustering, anomaly detection, and machine learning models with a front-end dashboard for visualization and control.

## 🌟 Features

- **Demand Forecasting**: Predict future electricity demand using XGBoost and ensemble models  
- **Clustering Analysis**: Discover usage behavior with K-Means, HDBSCAN, and hierarchical clustering  
- **Interactive UI**: Modern React dashboard with intuitive controls and real-time charts  
- **Real-time Analytics**: Visualize trends, anomalies, and forecast accuracy dynamically

---

## 📊 Project Overview

This project is designed to model and forecast electricity demand by combining historical consumption data with meteorological variables such as temperature, humidity, and wind speed. Through powerful machine learning algorithms, the system delivers predictive insights to help energy providers optimize infrastructure, respond to demand shifts, and improve operational efficiency.

---

## 🔍 Why Electricity Demand Forecasting?

Accurate energy forecasting is essential for:

- **⚖️ Grid Stability** – Maintaining balanced supply and demand  
- **💰 Resource Optimization** – Minimizing cost and waste  
- **🌞 Renewable Integration** – Planning around intermittent energy sources  
- **🌍 Environmental Responsibility** – Supporting sustainability goals  
- **📈 Economic Forecasting** – Planning infrastructure and budgeting for load fluctuations

---

## 🛠️ Key Technologies

| Category          | Stack                                    |
|------------------|-------------------------------------------|
| **Backend**       | FastAPI, Python, scikit-learn, XGBoost   |
| **Frontend**      | React, Vite, Tailwind CSS, Shadcn UI     |
| **ML Models**     | XGBoost, Random Forest, Stacking, LSTM   |
| **Data Processing**| Pandas, NumPy, SciPy                    |
| **Visualization** | Recharts, D3.js                          |

---

## 💻 User Interface

### 📌 Dashboard

- Select cities and date ranges
- Choose between forecasting models
- View actual vs. predicted electricity demand
- Explore clustering visualizations

### 🌙 Dark Mode Support

Full support for light and dark themes for accessibility and comfort.

### 📈 Analytics

Track prediction error (MAE, RMSE, MAPE) across models and visualize time-based energy patterns.

---
## 🔬 Technical Approach

### ✅ Data Processing Pipeline

- **Data Sources**: EIA930 electricity demand + historical weather datasets
- **Preprocessing Steps**:
  - Merge multiple JSON/CSV datasets by timestamp and city
  - Handle missing values (interpolation, median fill)
  - Feature engineering (cyclical hour encoding, lag features)
- **Anomaly Detection**:
  - Isolation Forest, z-score, and IQR methods

### 📦 Dimensionality Reduction

- PCA, t-SNE, and UMAP used for visualization and improving clustering input

---

## 🧠 Clustering Analysis

### Algorithms Used:

- **K-Means Clustering**  
- **HDBSCAN**  
- **Hierarchical Clustering with Dendrograms**

### Cluster Evaluation:

- Silhouette Score  
- Cluster Profiling (mean usage, time of day, temperature)

### Example Clusters:

- **Cluster 0**: High-demand hot afternoons  
- **Cluster 1**: Low-demand cool nights  
- **Cluster 2**: Winter morning peaks  
- **Cluster 3**: Weekend steady plateaus

---

## 🤖 Forecasting Models

### Target Variable:
- 24-hour ahead forecast of hourly electricity demand

### Features:
- Temperature, humidity, wind speed  
- Hour of day, day of week, month  
- Previous day’s demand at same hour

### Models Implemented:
- **XGBoost**  
- **Random Forest**  
- **Stacked Ensemble (XGBoost + RF)**  
- **Linear Regression (baseline)**  
- **LSTM Neural Network (optional)**

---

## 📊 Evaluation Metrics

- **MAE** – Mean Absolute Error  
- **RMSE** – Root Mean Square Error  
- **MAPE** – Mean Absolute Percentage Error  
- **Baseline Comparisons**:
  - Previous day’s same hour demand
  - Previous week’s same hour/day demand

---

## 🧪 Training Strategy

- TimeSeriesSplit Cross-Validation  
- GridSearchCV for model tuning  
- Recursive Feature Elimination  
- SHAP for interpretability (optional)

---

## 🚀 How to Run

### Backend

```bash
cd src/
pip install -r ../requirements.txt
uvicorn main:app --reload
