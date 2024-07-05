# Heart Disease Prediction Using Logistic Regression and PCA

This notebook demonstrates how to predict heart disease using logistic regression and principal component analysis (PCA).

## Overview

The script begins by loading the dataset (`heart.csv`) and checking for missing values. It performs feature engineering to create age categories and interaction features based on cholesterol levels (`chol`). The dataset is split into training and testing sets, and numerical and categorical features are preprocessed separately using `ColumnTransformer`. 

## Methodology

1. **Data Loading and Preprocessing:**
   - Load `heart.csv` and check for missing values.
   - Feature engineering: Create age categories and interaction features (`age_chol_interaction`).
   - Separate features (`X`) and target (`Y`).

2. **Model Training:**
   - Split data into training and testing sets (`train_test_split`).
   - Preprocess numerical features with `StandardScaler` and categorical features with `OneHotEncoder`.
   - Apply PCA for dimensionality reduction (`PCA`).

3. **Model Selection and Evaluation:**
   - Initialize logistic regression model.
   - Use `GridSearchCV` for hyperparameter tuning (`C` regularization parameter).
   - Evaluate model performance on training and test sets using accuracy score, ROC-AUC score, and confusion matrix.
   - Visualize the confusion matrix using `matplotlib` and `seaborn`.

4. **Prediction Function:**
   - Define a function to predict heart disease based on input data (`predict_heart_disease`).
   - Convert input data to a pandas DataFrame, preprocess using `ColumnTransformer`, and transform using PCA.
   - Make predictions and interpret results.

## Conclusion

This notebook provides a comprehensive example of using logistic regression and PCA for heart disease prediction, covering data preprocessing, model training and evaluation, as well as prediction for new data inputs.

