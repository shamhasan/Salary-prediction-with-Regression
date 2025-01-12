# Salary Prediction

## Overview

This project focuses on predicting salaries based on years of experience using machine learning models. By utilizing a dataset with experience and salary data, regression techniques are applied to build an accurate predictive model.

## Dataset

The dataset used in this project consists of two columns:

- **`experience_years`**: The number of years of experience an individual has.
- **`salary`**: The salary corresponding to the individual's experience level.

## Methodology

The project workflow consists of the following steps:

1. **Data Ingestion**: Loading the salary dataset using Pandas.
2. **Exploratory Data Analysis (EDA)**: Analyzing data distribution, exploring correlations, and identifying potential outliers.
3. **Data Preparation**: Handling missing values and removing duplicates to ensure clean data.
4. **Data Splitting**: Dividing the dataset into training and testing sets using `train_test_split`.
5. **Model Training**: Training three regression models:
   - **Linear Regression**
   - **Decision Tree Regression**
   - **Random Forest Regression**
6. **Model Evaluation**: Assessing each model's performance using metrics such as:
   - Mean Squared Error (MSE)
   - R-squared (R²) score
7. **Model Selection**: Comparing model performances and selecting the best-performing model based on evaluation metrics.
8. **Model Saving**: Saving the best model for future use with `joblib`.

## Results

- **Model Performance**:
1. ![image alt](https://github.com/shamhasan/Salary-prediction-with-Regression/blob/33a02247223880f91cb8ab12ae5911a39122ecc2/Linear%20REgression.JPG)
2. ![image alt](https://github.com/shamhasan/Salary-prediction-with-Regression/blob/b28504976d5cce543bb815c94203e12c555cfbe5/Decision%20Tree.JPG)
3. ![image alt](https://github.com/shamhasan/Salary-prediction-with-Regression/blob/b28504976d5cce543bb815c94203e12c555cfbe5/Random%20forest.JPG)



- **Best Model**:
  After comparing the performance of the three models using Mean Squared Error (MSE) and R-squared (R²) score. the Random Forest Regression emerged as the best model for salary prediction. It achieved the lowest MSE on the test data (21,744.73) and the highest R² score on the test data (0.94). demonstrating excellent accuracy and strong generalization capabilities. Additionally. the gap between training and testing data MSE (18,007.29) is smaller compared to the other models. indicating a lower risk of overfitting. Therefore. the Random Forest Regression was selected as the final model for deployment.


## Usage

To use the saved model for salary prediction:

1. Load the model using:
   ```python
   from joblib import load
   model = load('random_forest_model.pkl')
