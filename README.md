# Heart Disease Risk Prediction: Logistic Regression

Implementation of logistic regression from scratch for heart disease prediction.

## Overview

This project implements logistic regression for binary classification to predict heart disease risk based on clinical features. All core algorithms are implemented from scratch using only NumPy, Pandas, and Matplotlib.

**Course:** AREP - Machine Learning Bootcamp
**Author:** David Felipe Velasquez Contreras

## Repository Structure

```
/
├── README.md
├── heart_disease_lr_analysis.ipynb    # Main analysis notebook
├── Heart_Disease_Prediction.csv       # Dataset
└── screenshots/                        # SageMaker evidence (to be added)
```

## Dataset Description

**Source:** [Kaggle Heart Disease Dataset](https://www.kaggle.com/datasets/neurocipher/heartdisease)

| Property | Value |
|----------|-------|
| Samples | 270 patients |
| Features | 13 clinical attributes |
| Target | Heart Disease (Presence/Absence) |
| Disease Rate | ~44% presence |

### Features

- **Age:** Patient age (29-77 years)
- **Sex:** Gender (0=Female, 1=Male)
- **Chest Pain Type:** 4 types of chest pain
- **BP:** Resting blood pressure (mm Hg)
- **Cholesterol:** Serum cholesterol (mg/dL, 112-564)
- **FBS over 120:** Fasting blood sugar > 120 mg/dL
- **EKG results:** Resting electrocardiographic results
- **Max HR:** Maximum heart rate achieved
- **Exercise angina:** Exercise induced angina
- **ST depression:** ST depression induced by exercise
- **Slope of ST:** Slope of peak exercise ST segment
- **Number of vessels fluro:** Number of major vessels (0-3)
- **Thallium:** Thallium stress test result

## Implementation Details

### Step 1: Data Preparation
- Load and explore dataset
- Binarize target variable (Presence=1, Absence=0)
- EDA: statistics, distributions, outlier analysis
- 70/30 stratified train/test split
- Feature normalization (z-score standardization)

### Step 2: Logistic Regression
- Sigmoid function implementation
- Binary cross-entropy cost function
- Gradient computation (vectorized)
- Gradient descent optimization
- Evaluation metrics (Accuracy, Precision, Recall, F1-Score)

### Results (Preliminary)

| Metric | Training | Test |
|--------|----------|------|
| Accuracy | 81.5% | 69.1% |
| Precision | 79.5% | 69.0% |
| Recall | 78.6% | 55.6% |
| F1-Score | 79.0% | 61.5% |

## Libraries Used

- **NumPy:** Numerical computations
- **Pandas:** Data manipulation
- **Matplotlib:** Visualization

**No scikit-learn** used for core training algorithms.

## Local Execution Evidence

### Screenshots

![alt text](screenshots/EDA_Local.png)

![alt text](screenshots/Class_Distributions.png)

## AWS SageMaker Execution Evidence

TODO

### Screenshots



---

## Progress

- [x] Step 1: Load and Prepare Dataset
- [x] Step 2: Implement Basic Logistic Regression
- [ ] Step 3: Visualize Decision Boundaries
- [ ] Step 4: Regularization (L2)
- [ ] Step 5: SageMaker Deployment
