# EEG-Tumour Detection

## Problem Definition

This project focuses on EEG analysis using advanced algorithms to detect brain tumors. By leveraging machine learning models, it identifies distinct patterns in EEG data, highlighting abnormal electrical activity linked to tumor presence. High-resolution EEG cap designs enhance signal acquisition, capturing minute irregularities. Advanced spectral and connectivity analyses are used to uncover subtle biomarkers, distinguishing tumor signatures from normal neural activity. Integration with neuroimaging techniques like MRI further strengthens accuracy, enabling precise localization and characterization of tumors. Real-time monitoring and cloud-based collaboration expedite diagnosis and treatment planning. These advancements in EEG-based tumor detection aim to provide non-invasive, early, and precise identification of brain tumors in clinical settings.

---

## Data Preprocessing

**1. Data Loading and Exploration**
- The EEG dataset is loaded using pandas and basic exploration is performed, including displaying the first and last few rows, checking data types, shape, and for missing or duplicated values.
- The dataset contains 14 EEG channel readings (AF3, F7, F3, FC5, T7, P7, O1, O2, P8, T8, FC6, F4, F8, AF4) and a `result` column indicating tumor presence (0 or 1).

**2. Descriptive Statistics**
- Summary statistics (mean, std, min, max, quartiles) are generated for all columns to understand data distribution.
- The dataset is checked for skewness and kurtosis to assess the distribution and presence of outliers.

**3. Data Integrity**
- Ensures there are no missing (`isnull().sum()`) or duplicated (`duplicated().sum()`) entries.
- Confirms the data is clean and ready for analysis.

---

## Statistical Analysis

**1. Covariance and Correlation**
- The covariance matrix is computed to assess the linear relationship between different EEG channels.
- The correlation matrix is also calculated, helping to identify which channels are most related.

**2. Chi-square Test**
- A chi-square test is performed to evaluate the independence of features, which can inform feature selection for machine learning models.

---

## Feature Engineering

- Skewness and kurtosis are calculated for each feature to further understand the data's distribution and potential need for transformation.
- Data normalization and scaling can be performed using `StandardScaler` to prepare for model training.

---

## Machine Learning Preparation

- The dataset is split into training and testing sets using `train_test_split`.
- Features are scaled, and target labels are separated for model input.

---

## Model Training and Evaluation

- A Gaussian Naive Bayes classifier is used to train on the EEG data.
- Model performance is evaluated using confusion matrix, accuracy, precision, recall, and F1-score.

---

## Advanced Analysis

- Additional analyses such as connectivity, spectral analysis, and integration with MRI data can be performed for enhanced tumor detection.
- Real-time and cloud-based processing can be implemented for collaborative diagnostics.

---

## Summary

This project demonstrates a comprehensive pipeline for EEG-based brain tumor detection, from data loading and preprocessing to statistical analysis and machine learning classification. The approach emphasizes data integrity, robust statistical evaluation, and practical application in clinical diagnostics.
