## Project Overview

This project explores the relationship between academic and lifestyle factors and their potential contribution to depression among students. The dataset undergoes preprocessing, analysis, and modeling using machine learning techniques. Key goals include:

- Preprocessing raw data and handling missing values.
- Conducting regression and classification analyses.
- Tuning hyperparameters for optimal model performance.
- Visualizing results for meaningful interpretation.

## Features

- **Correlation Analysis:** Identifies feature interdependencies.
- **Machine Learning Models:** Implements models like XGBoost for predictive insights.
- **Feature Importance:** Quantifies each variable's impact on depression.

## Files

- **Dataset:** Dataset for this project is used from Kaggle https://www.kaggle.com/datasets/hopesb/student-depression-dataset/data.
- **Main Script:** Contains preprocessing, modeling, and result evaluation.

## Instructions

### Requirements

1. Python 3.9+
2. Libraries:
   ```bash
   pip install pandas numpy seaborn matplotlib scikit-learn xgboost
   ```

### Running the Code

1. Clone the repository or save the script.
2. Update the dataset path.
3. Run the Python script:
   ```bash
   python depression_analysis.py
   ```

## Results

### Model Evaluation

The XGBoost classifier achieves an **accuracy score of 83%** on the test dataset. Below are detailed evaluation metrics:

- **Accuracy Score:** 0.829242
- **Classification Report:**
  - Class 0 (No Depression):
    - Precision: 0.81
    - Recall: 0.78
    - F1-Score: 0.79
    - Support: 2343 samples
  - Class 1 (Depression):
    - Precision: 0.84
    - Recall: 0.87
    - F1-Score: 0.85
    - Support: 3238 samples
  - Overall:
    - Macro Average F1-Score: 0.82
    - Weighted Average F1-Score: 0.83

### Feature Importance

Feature importance from the XGBoost model reveals the most significant predictors of depression:

1. **Have you ever had suicidal thoughts?**: 0.6922
2. **Academic Pressure**: 0.1108
3. **Financial Stress**: 0.0546
4. **Dietary Habits**: 0.0294
5. **Age**: 0.0210
6. **Study Satisfaction**: 0.0193
7. **Work/Study Hours**: 0.0186
8. **Sleep Duration**: 0.0150
9. **Family History of Mental Illness**: 0.0143
10. **CGPA**: 0.0125
11. **Gender**: 0.0123
12. **Work Pressure**: 0.0000
13. **Job Satisfaction**: 0.0000

### Hyperparameter Tuning

The best hyperparameters for the XGBoost model were found using grid search:

- **Max Depth:** 3
- **Learning Rate:** 0.1
- **Number of Estimators:** 300
- **Subsample:** 1.0
- **Colsample Bytree:** 1.0

With these parameters, the model achieved the highest accuracy of **84.04%**.

## Insights

1. **Correlation Findings:** Strong interdependencies exist between variables such as sleep duration, dietary habits, and mental health.
2. **Significant Features:** Suicidal thoughts, academic pressure, and financial stress are critical predictors.
3. **Optimization:** Model tuning improved accuracy by balancing learning rate and tree depth.

## Future Work

- Extend to multi-class mental health analysis.
- Add time-series components for longitudinal studies.
