# ✈️ Flight Delay Prediction & Analytics

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--learn-orange)
![Dashboard](https://img.shields.io/badge/Dashboard-Plotly%20Dash-brightgreen)
![Explainability](https://img.shields.io/badge/Explainability-SHAP-purple)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Model](https://img.shields.io/badge/Best%20Model-Random%20Forest-darkgreen)
![Accuracy](https://img.shields.io/badge/Accuracy-0.91-success)
![ROC--AUC](https://img.shields.io/badge/ROC--AUC-0.94-blueviolet)

A machine learning capstone project focused on predicting flight delays, comparing classification models, interpreting model decisions, and presenting findings through interactive visual analytics.

---

## Overview

Flight delays affect airline operations, customer satisfaction, and scheduling efficiency. This project uses historical flight data to:

- predict whether a flight will be delayed
- compare machine learning models for classification performance
- identify the most influential factors behind delays
- explain model decisions using SHAP
- support exploration through an interactive dashboard

This project combines **data cleaning, exploratory analysis, supervised learning, model evaluation, explainability, and dashboard development** in one end-to-end workflow. :contentReference[oaicite:1]{index=1}

---

## Business Problem

Airlines and airport operations teams need better ways to anticipate delays before they happen. A reliable classification model can help flag risky flights early, while interpretability tools can highlight the operational factors most associated with delays.

---

## Project Goals

- Build a classification pipeline for flight delay prediction
- Compare a **Decision Tree** and **Random Forest**
- Evaluate models with:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - ROC-AUC
  - Confusion Matrix
- Analyze feature importance
- Use SHAP for model explainability
- Create an interactive dashboard for stakeholders

---

## Dataset

The dataset contains **300,000+ flight records** and includes time, airline, route, and delay-related variables. The PDF shows a working dataset with roughly **336,776 rows** and features such as `dep_time`, `sched_dep_time`, `arr_time`, `sched_arr_time`, `arr_delay`, `air_time`, `distance`, `flight`, `tailnum`, `origin`, `dest`, and engineered time features. :contentReference[oaicite:2]{index=2}

### Target Variable

The project predicts:

- `is_delayed = 1` → delayed
- `is_delayed = 0` → not delayed

The delay logic in the notebook is based on whether **arrival delay exceeds 15 minutes**. :contentReference[oaicite:3]{index=3}

---

## Tech Stack

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **SHAP**
- **Plotly**
- **Dash**

These libraries are visible throughout the notebook and dashboard sections in the PDF. :contentReference[oaicite:4]{index=4}

---

## Workflow

### 1. Data Preparation
- Loaded and inspected flight records
- Assessed missing values
- Cleaned and transformed features
- Encoded categorical variables using **Label Encoding**

### 2. Exploratory Data Analysis
Visualizations included:
- delayed vs not delayed count
- service quality distribution
- arrival delay distribution
- missingness matrix
- missing values by column

### 3. Modeling
Two classification models were trained and compared:
- **Decision Tree**
- **Random Forest**

### 4. Evaluation
Performance was assessed using:
- Accuracy
- ROC-AUC
- Classification report
- Confusion matrix
- ROC curves

### 5. Explainability
Interpretability methods included:
- feature importance plots
- SHAP summary plot
- SHAP waterfall plot

### 6. Dashboard
An interactive dashboard was built with **Dash + Plotly** to explore:
- delay distributions
- airline comparisons
- route patterns
- model outputs
- summary insights

All of these steps appear in the uploaded capstone file. :contentReference[oaicite:5]{index=5}

---

## Model Results

| Model | Accuracy | ROC-AUC |
|---|---:|---:|
| Decision Tree | 0.8773 | 0.9150 |
| Random Forest | 0.9084 | 0.9443 |

The Random Forest achieved the strongest overall performance in the project, while the Decision Tree remained easier to interpret. :contentReference[oaicite:6]{index=6}

---

## Key Findings

- **Departure delay** was the most important predictive feature
- Time-related variables such as **departure time**, **departure hour**, and **air time** also had strong influence
- The **Random Forest** outperformed the Decision Tree on both accuracy and ROC-AUC
- SHAP analysis reinforced that higher departure delay values strongly push predictions toward the delayed class

These findings are supported by the feature importance and SHAP plots in the report. :contentReference[oaicite:7]{index=7}

---

## Visual Highlights

The project includes:
- class distribution chart
- service quality chart
- arrival delay histogram
- missingness plots
- confusion matrices
- ROC curve comparison
- model comparison bar chart
- feature importance chart
- SHAP beeswarm plot
- SHAP waterfall plot

These visuals make the project especially useful as a portfolio piece because they show both technical modeling and business interpretation. :contentReference[oaicite:8]{index=8}

---

## Why This Project Stands Out

This project demonstrates the ability to:

- work with a large real-world style dataset
- engineer and transform features for modeling
- compare multiple machine learning algorithms
- evaluate classification models correctly
- communicate findings visually
- apply explainable AI techniques
- build an end-to-end data product with an interactive dashboard

---

## Suggested Repository Structure

```text
flight-delay-prediction/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── raw/
│   │   └── flights.csv
│   └── processed/
│       └── model_df.csv
│
├── notebooks/
│   └── INFO6151_CAPSTONE_GROUP1.ipynb
│
├── src/
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   ├── train_decision_tree.py
│   ├── train_random_forest.py
│   ├── evaluate_models.py
│   └── explainability.py
│
├── dashboard/
│   └── app.py
│
├── outputs/
│   ├── figures/
│   │   ├── delayed_vs_not_delayed.png
│   │   ├── service_quality.png
│   │   ├── arrival_delay_distribution.png
│   │   ├── missingness_matrix.png
│   │   ├── decision_tree_confusion_matrix.png
│   │   ├── random_forest_confusion_matrix.png
│   │   ├── roc_curve.png
│   │   ├── model_comparison.png
│   │   ├── feature_importance.png
│   │   ├── shap_summary.png
│   │   └── shap_waterfall.png
│   └── reports/
│       └── capstone_report.pdf
│
└── assets/
    └── dashboard_screenshots/
