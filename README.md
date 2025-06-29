# GHG_Data_Cleaning_And_Feature_Engineering.ipynb

# 🌱 GHG Emission Prediction Preprocessing

This repository contains the preprocessing workflow for a greenhouse gas (GHG) emission prediction project. The notebook includes comprehensive data cleaning, transformation, and feature preparation steps to build a robust foundation for predictive modeling.

---

## 📁 File Overview

### `GHG_Emission_Prediction_Preprocessing.ipynb`
- Merges and cleans data from various Excel sheets (industry and commodity-based)
- Handles missing values, inconsistent formats, and duplicates
- Encodes categorical variables (`Unit`, `Substance`, `Source`) using one-hot encoding
- Detects and processes outliers using IQR method:
  - Removal for extreme cases
  - Capping (Winsorization) to retain structure
- Analyzes skewness and normality using:
  - Skew/Kurtosis metrics
  - KDE plots
- Applies transformations (`log1p`, Yeo-Johnson) to reduce skewness (only for unimodal features)
- Leaves bimodal/multimodal distributions untransformed to preserve separability
- Prepares the data for model training (e.g., regression, tree-based, ML pipelines)

---

## 📊 Goal

To prepare a clean, structured, and model-ready dataset for predicting **Supply Chain Emission Factors** using relevant features such as substance, unit, and source.

---

## 📌 Key Techniques Used

- `pandas` for data handling
- `seaborn` and `matplotlib` for visualization
- `scikit-learn` for encoding and transformation
- IQR-based outlier detection
- Power transformations (Yeo-Johnson, log)
- KDE and bar plots for distribution and group analysis

---

## 🔍 Next Steps

- Model training and evaluation (Linear Regression, Random Forest, XGBoost, etc.)
- Hyperparameter tuning
- Feature importance analysis
- Deployment-ready pipelines (optional)

---

## 💡 Author Notes

If using this notebook, make sure to install the required packages:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
