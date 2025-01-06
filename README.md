# Screentime Analysis and Prediction

This project analyzes and predicts app usage behavior based on features such as notifications and times opened. The analysis includes exploratory data analysis (EDA), insights generation, and predictive modeling using multiple machine learning techniques.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Dataset Description](#dataset-description)
3. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
4. [Machine Learning Models](#machine-learning-models)
5. [Insights and Findings](#insights-and-findings)
6. [Feature Importance](#feature-importance)
7. [Technologies Used](#technologies-used)
8. [Usage](#usage)
9. [Results](#results)
10. [Future Work](#future-work)

---

## Project Overview

This project leverages a small dataset (55 rows) containing app usage details to perform the following:
- Understand user behavior on apps like Instagram and WhatsApp.
- Identify key features influencing app usage.
- Predict usage times based on features using machine learning models.

---

## Dataset Description

The dataset contains the following columns:
- **Date**: The date of the recorded data.
- **Usage**: The amount of time spent on the app (in minutes).
- **Notifications**: The number of notifications received.
- **Times opened**: The number of times the app was opened.
- **App**: The app name (e.g., Instagram, WhatsApp).

---

## Exploratory Data Analysis (EDA)

1. **Time Series Analysis**:
   - A line plot of app usage over time shows that WhatsApp has higher overall usage than Instagram.
   
2. **Bar Chart**:
   - The average usage of WhatsApp significantly surpasses Instagram.

3. **Scatter Plot**:
   - **WhatsApp**: A positive correlation exists between notifications and usage.
   - **Instagram**: The correlation between notifications and usage is less evident.

4. **Correlation Heatmap**:
   - Strong positive relationships between `Usage`, `Notifications`, and `Times opened`.

---

## Machine Learning Models

### 1. Models Used
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**
- **Random Forest Regressor** (with hyperparameter tuning)

### 2. Evaluation Metrics
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **R-squared Score (R²)**

### 3. Results:
| Model                | MAE   | MSE     | R²   |
|----------------------|-------|---------|------|
| Linear Regression    | 26.21 | 1277.34 | 0.70 |
| Ridge Regression     | 26.50 | 1300.28 | 0.69 |
| Lasso Regression     | 26.24 | 1280.17 | 0.70 |
| Random Forest Regressor | 30.62 | 1478.73 | 0.65 |

- **Linear Regression and Lasso Regression** achieved the highest R² of 0.70.

---

## Insights and Findings

1. **App Usage**:
   - WhatsApp dominates in both total and average usage.

2. **Feature Correlations**:
   - **Usage** is strongly correlated with **Notifications** and **Times opened**.

3. **Model Performance**:
   - Simpler linear models perform better than Random Forest, possibly due to the dataset's size and linear relationships.

---

## Feature Importance

Using the **Random Forest Regressor**, feature importance scores were calculated:
- **Times Opened**: ~0.64 (most significant feature).
- **Notifications**: ~0.36.

![Feature Importance Chart](https://github.com/coder-akram-khan/Screentime-App-Usage-Analysis/blob/main/feature.png?raw=true)

---

## Technologies Used

- **Programming Language**: Python
- **Libraries**:
  - Data Analysis: `pandas`, `numpy`
  - Visualization: `plotly`
  - Machine Learning: `scikit-learn`

---

## Usage

1. **Clone the Repository**:
   ```bash
   https://github.com/coder-akram-khan/Screentime-App-Usage-Analysis.git
   cd Screentime-App-Usage-Analysis
2. **Install Requirements**:
   ```bash
   pip install -r requirements.txt
3. **Run the Analysis**: Open ScreenTimeAnalysis.ipynb in Jupyter Notebook to reproduce the analysis and results.

## Results

  - **Best Model**: Linear Regression and Lasso Regression (R² = 0.70).
  -  **Key Feature**: "Times Opened" has the greatest influence on predicted usage.

## Future Work

  - **Expand Dataset**: Include more apps and user interactions to improve model generalization.
  - **Advanced Models**: Explore deep learning techniques for prediction.
  - **Interaction Effects**: Investigate the interaction between features like notifications and times opened.
