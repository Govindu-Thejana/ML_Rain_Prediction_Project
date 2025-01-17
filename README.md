# 🌧️ Rain Prediction in Galle, Sri Lanka, using Machine Learning 🌧️

## 📋 Project Overview
This project focuses on predicting rainfall in Galle, Sri Lanka, using historical weather data spanning from January 1, 2010, to January 1, 2023. The primary objective is to develop a predictive model that assists in managing water resources, agricultural planning, and mitigating weather-related risks.

---

## ✨ Features
- **📊 Rich Dataset**: Includes multiple meteorological parameters for 30 cities in Sri Lanka.
- **📈 Exploratory Data Analysis (EDA)**: Detailed insights through visualizations and correlation analysis.
- **🤖 Model Implementation**:
  - Baseline Model: Linear Regression
  - Advanced Model: Random Forest Regressor with Hyperparameter Tuning
- **⚙️ Feature Engineering**: Incorporates cyclical encoding for time-related features.
- **📉 Performance Metrics**:
  - R², Mean Squared Error (MSE), and Mean Absolute Error (MAE).

---

## 💾 Dataset
The dataset was sourced from [kaggle](https://www.kaggle.com/datasets/rasulmah/sri-lanka-weather-dataset).

### 📝 Key Features:
- **🌡️ Temperature**: Maximum, minimum, and mean values.
- **💧 Precipitation**: Total rainfall, snowfall, and precipitation hours.
- **💨 Wind**: Speed, gusts, and dominant direction.
- **☀️ Solar Radiation**: Shortwave radiation sum.
- **🗺️ Geographical Information**: Latitude, longitude, elevation.

---

## 📋 Prerequisites

Before running this project, ensure you have the following installed:
- 🐍 Python (>=3.8)
- 📓 Jupyter Notebook or Google Colab

---

## 🚀 Getting Started

### 📥 Clone the Repository
```bash
git clone https://github.com/govindu-thejana/ML_Rain_Prediction_Project.git
cd ML_Rain_Prediction_Project
```

### ▶️ Run the Project
1. Open the Jupyter Notebook `ML_Project.ipynb`.
2. Follow the steps for EDA, data preprocessing, and model training.
3. Evaluate model performance using the provided scripts.

---

## 🛠️ Implementation Details
### 🔄 Data Preprocessing

- Handling missing values
- Feature engineering (cyclic encoding of time features)
- Data standardization
- Outlier detection and treatment
- Duplicate removal

## 🤖 Models

### 1. Linear Regression
- **Training R²**: 0.62
- **Testing R²**: 0.60
- **Training MSE**: 16.96
- **Testing MSE**: 18.24
- **Training MAE**: 2.82
- **Testing MAE**: 2.81

### 2. Random Forest Regressor (After Tuning)
- **Training R²**: 0.93
- **Testing R²**: 0.83
- **Training MSE**: 3.33
- **Testing MSE**: 7.72
- **Training MAE**: 0.90
- **Testing MAE**: 1.35

---
## ⚙️ Feature Engineering

- Cyclical encoding of month features
- Feature scaling using StandardScaler
- Selection of key features based on correlation analysis

## 🔧 Hyperparameter Tuning
Best parameters for Random Forest:
```json
{
    "bootstrap": true,
    "max_depth": 10,
    "min_samples_leaf": 4,
    "min_samples_split": 10,
    "n_estimators": 100
}
```

## 📊 Model Comparison

### 🔍 Key Observations:
- **Performance**: Random Forest significantly outperforms Linear Regression in terms of both R² and error metrics.
- **Overfitting**: While Random Forest shows a high training R², then hyperparameter tuning prevent overfitting, as evidenced by a consistent testing R².
- **Complexity**: Random Forest captures non-linear relationships better, making it more suitable for this dataset.

### 📈 Visualizations:
- Scatter plots comparing actual vs. predicted rainfall indicate a better fit with Random Forest.
- Feature importance analysis in Random Forest highlights key contributors like temperature and precipitation hours.

--- 

## 🎯 Key Results
- Random Forest achieved a higher R² (0.83) on the test set compared to Linear Regression (0.60).
- Feature engineering and hyperparameter tuning further enhanced the model's performance.

---

## 📚 References
1. [Random Forest Algorithm - GeeksforGeeks](https://www.geeksforgeeks.org/random-forest-algorithm-in-machine-learning/)
2. [Sri Lanka Weather Dataset - Kaggle](https://www.kaggle.com/datasets/rasulmah/sri-lanka-weather-dataset)

---

## 👥 Authors
- **Govindu Thejana** - 📧 govinduthejana@gmail.com
- **Yasiru Kularathna** - 📧 yasirukularathne1234@gmail.com

## 🤝 Contributing
Contributions are welcome! Please fork this repository and create a pull request for any suggestions or improvements.
