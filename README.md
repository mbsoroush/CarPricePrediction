
# 🚗 Car Price Prediction | Regression Modeling

A machine learning project focused on predicting used car selling prices using regression algorithms, exploratory data analysis, and feature engineering.

## 📌 Overview

Car prices depend on several factors, including the vehicle's age, current market price, mileage, fuel type, transmission, and ownership history.

This project analyzes these factors and develops regression models to estimate car selling prices. It explores data preprocessing, categorical encoding, model evaluation, feature scaling, and polynomial feature engineering to investigate how different approaches affect prediction performance.

## 🎯 Objectives

- Explore the relationships between car characteristics and selling prices.
- Clean and preprocess the dataset.
- Visualize feature distributions and relationships.
- Build and compare regression models.
- Evaluate model performance using standard regression metrics.
- Investigate normalization and polynomial feature engineering.
- Generate selling-price predictions for hypothetical car samples.

## 📊 Dataset

The notebook works with a dataset containing **301 car records** and the following features:

| Feature | Description |
|---|---|
| `Year` | Manufacturing year of the car |
| `Age` | Derived age of the car |
| `Selling_Price` | Target variable: car selling price |
| `Present_Price` | Present market price of the car |
| `Kms_Driven` | Distance driven in kilometers |
| `Fuel_Type` | Fuel type |
| `Seller_Type` | Whether the seller is an individual or dealer |
| `Transmission` | Transmission type |
| `Owner` | Number of previous owners |

The `Car_Name` column is removed during preprocessing, and the car's age is derived from its manufacturing year.

## 🔍 Exploratory Data Analysis

The project uses visualizations to investigate the dataset and identify relationships between features and the target variable.

Key analyses include:

- Distribution plots and box plots for numerical features.
- Selling price versus present price.
- Selling price versus kilometers driven.
- Selling price versus manufacturing year.
- Distributions of fuel type, seller type, transmission, and ownership.
- Correlation analysis between numerical features.

## 🧹 Data Preprocessing

The preprocessing workflow includes:

- Inspecting dataset structure and descriptive statistics.
- Checking for missing values and duplicate records.
- Removing duplicate records.
- Dropping the car-name feature.
- Creating an `Age` feature from `Year`.
- Applying dummy encoding to categorical variables.
- Separating input features from the target variable.
- Splitting the dataset into training and testing sets.

The initial train-test split uses 75% of the data for training and 25% for testing.

## 🤖 Regression Models

The notebook explores the following regression approaches.

### 1. Ridge Regression

Uses L2 regularization to penalize large model coefficients and investigate regularized linear prediction.

### 2. Lasso Regression

Uses L1 regularization, which can shrink some coefficients to zero and support feature selection.

### 3. Linear Regression

Establishes a linear baseline for predicting car selling prices from the available features.

### 4. Polynomial Regression

Expands the feature set with interaction terms and polynomial features to model more complex relationships between car characteristics and selling prices.

## ⚙️ Feature Scaling

The project investigates two scaling techniques:

- **MinMaxScaler:** Scales features to a specified range.
- **StandardScaler:** Standardizes features based on their mean and standard deviation.

The notebook compares the resulting regression metrics to examine how scaling affects model evaluation.

## 📈 Model Evaluation

Model performance is evaluated using:

| Metric | Purpose |
|---|---|
| Mean Absolute Error (MAE) | Measures the average absolute prediction error |
| Mean Squared Error (MSE) | Measures the average squared prediction error |
| Root Mean Squared Error (RMSE) | Expresses prediction error on the target's scale |
| R² Score | Measures the proportion of target variance explained by the model |

The notebook also applies **7-fold cross-validation** to examine model performance across multiple data splits.

## 🏆 Results

In the displayed experiment, the polynomial feature-engineering model reports:

| Metric | Result |
|---|---:|
| Training R² | 0.9768 |
| Test R² | 0.9651 |
| MAE | 0.6474 |
| RMSE | 0.9541 |

The displayed 7-fold cross-validation results for this experiment have a mean R² score of approximately **0.9578**.

These are the results recorded in the notebook, not independently reproduced results. The evaluation pipeline should be reviewed before treating them as a reliable estimate of generalization performance.

## 🔮 Price Prediction

The final section demonstrates how a trained regression model can generate a predicted selling price for a hypothetical car sample using its input features.

The notebook includes an example prediction of approximately **4.17 thousand dollars**. This is an illustrative prediction for the constructed sample, not a general performance guarantee.

## 🛠️ Technologies & Libraries

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat-square)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat-square&logo=plotly&logoColor=white)

## 🚀 Getting Started

Clone the repository:

```bash
git clone https://github.com/mbsoroush/CarPricePrediction.git
```

Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn plotly scikit-learn
```

Open `Regression Project.ipynb` in Jupyter Notebook or JupyterLab and run the cells to explore the analysis and modeling workflow.

**Note:** The notebook currently reads the dataset from a local Windows file path. Update the `pd.read_csv()` path to point to your local copy of the dataset before running the notebook.

## 📚 Key Learning Outcomes

- Exploratory data analysis and visualization.
- Data cleaning and categorical feature encoding.
- Regression modeling and performance evaluation.
- Regularization with Ridge and Lasso regression.
- Feature scaling and polynomial feature engineering.
- Cross-validation for model assessment.
- Generating predictions from trained regression models.
