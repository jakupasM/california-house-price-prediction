# 🏠 California House Price Prediction Using Machine Learning

## 📌 Project Overview

This project develops and evaluates multiple machine learning regression models to predict California housing prices using the California Housing Dataset provided by Scikit-learn.

The project follows a complete machine learning workflow, including:

- Data Exploration
- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Feature Scaling
- Model Training
- Model Evaluation
- Model Comparison
- Feature Importance Analysis
- Prediction Analysis
- Residual Analysis

The objective is to compare multiple regression algorithms and identify the best-performing model for predicting California housing prices.

---

# 📂 Dataset

**Dataset:** California Housing Dataset

**Source:** Scikit-learn

```python
from sklearn.datasets import fetch_california_housing
```

### Dataset Information

- **Rows:** 20,640
- **Features:** 8
- **Target Variable:** Median House Value

---

# 📊 Features

| Feature | Description |
|----------|-------------|
| MedInc | Median income in the district |
| HouseAge | Median house age |
| AveRooms | Average number of rooms |
| AveBedrms | Average number of bedrooms |
| Population | District population |
| AveOccup | Average household occupancy |
| Latitude | Geographic latitude |
| Longitude | Geographic longitude |

Target Variable:

**Price (Median House Value)**

---

# 🔍 Exploratory Data Analysis

Several visualizations were created to better understand the data before building the models.

## Price Distribution

This histogram illustrates how house prices are distributed across California.

![Price Distribution](images/price_distribution.png)

---

## Correlation Matrix

The heatmap shows the correlation between all numerical variables.

It helps identify relationships between features and the target variable.

![Correlation Matrix](images/correlation_matrix.png)

---

## Geographic Distribution of House Prices

This visualization displays California districts geographically.

- Color represents house prices.
- Point size represents district population.

![Geographic Distribution](images/geographic_distribution.png)

---

# ⚙ Data Preprocessing

The following preprocessing steps were performed:

- Converted the dataset into a Pandas DataFrame
- Checked for missing values
- Exploratory Data Analysis
- Feature and target separation
- Train/Test Split (80/20)
- Feature Scaling (Linear Regression only)

Tree-based models (Random Forest and Gradient Boosting) were trained using the original feature values because they are not affected by feature scaling.

---

# 🤖 Machine Learning Models

Three regression algorithms were implemented and compared.

## 1. Linear Regression

Used as the baseline regression model.

---

## 2. Random Forest Regressor

An ensemble learning algorithm that combines multiple decision trees to improve prediction accuracy.

---

## 3. Gradient Boosting Regressor

A boosting algorithm that sequentially improves previous prediction errors.

---

# 📈 Model Performance

| Model | MAE | RMSE | R² Score |
|------|------:|------:|------:|
| Linear Regression | 0.5332 | 0.7456 | 0.5758 |
| Random Forest Regressor | **0.3268** | **0.5040** | **0.8062** |
| Gradient Boosting Regressor | 0.3483 | 0.5114 | 0.8004 |

## Model Comparison

![Model Comparison](images/model_comparison.png)

---

# 🌳 Feature Importance

Random Forest Feature Importance was used to identify the variables that contributed most to house price prediction.

Main observations:

- Median Income is the strongest predictor.
- Latitude and Longitude also have significant predictive power.
- Geographic location plays a major role in determining house prices.

![Feature Importance](images/feature_importance.png)

---

# 🎯 Prediction Analysis

## Actual vs Predicted Values

This visualization compares predicted house prices with the actual values.

The red diagonal line represents perfect predictions.

Most observations are located close to the diagonal, indicating strong predictive performance.

![Actual vs Predicted](images/actual_vs_predicted.png)

---

## Residual Plot

Residual analysis evaluates the prediction errors made by the model.

Most residuals are randomly distributed around zero, indicating that the Random Forest model generalizes well.

The diagonal boundary visible in the residual plot is caused by the capped target values in the California Housing Dataset rather than by poor model performance.

![Residual Plot](images/residual_plot.png)

---

# 🏆 Best Performing Model

Among the three regression models, the **Random Forest Regressor** achieved the best overall performance.

### Performance

- **MAE:** 0.3268
- **RMSE:** 0.5040
- **R² Score:** 0.8062

The Random Forest model significantly outperformed Linear Regression by capturing nonlinear relationships within the housing data while maintaining lower prediction errors.

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# 📁 Project Structure

```
california-house-price-prediction
│
├── images/
│   ├── price_distribution.png
│   ├── correlation_matrix.png
│   ├── geographic_distribution.png
│   ├── model_comparison.png
│   ├── feature_importance.png
│   ├── actual_vs_predicted.png
│   └── residual_plot.png
│
├── notebooks/
│   └── california_house_price_prediction.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

# 🚀 Future Improvements

Possible future improvements include:

- Hyperparameter tuning using GridSearchCV
- Cross-validation
- XGBoost Regressor
- LightGBM Regressor
- SHAP feature importance analysis
- Model deployment using Flask or Streamlit

---

# 👨‍💻 Author

**Mario Jakupas**

Master of Science in Computer Science

Machine Learning • Data Analytics • Python
