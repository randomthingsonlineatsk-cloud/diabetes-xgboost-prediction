# Diabetes Prediction with XGBoost and SHAP Explainability

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20332710.svg)](https://doi.org/10.5281/zenodo.20332710)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)

## Overview
A complete machine learning pipeline that predicts diabetes risk using the 
Pima Indians Diabetes Dataset. Built with XGBoost ensemble learning, 
feature engineering, and SHAP explainability for clinical interpretability.

## Model Performance
| Metric | Score |
|---|---|
| Accuracy | 87.0% |
| Precision | 79.3% |
| Recall | 85.2% |
| F1 Score | 82.1% |
| ROC-AUC | 94.7% |
| 5-Fold CV AUC | 0.944 ± 0.014 |

## Dataset
Pima Indians Diabetes Dataset
- 768 patients
- 9 features (Age, BMI, Glucose, Blood Pressure, Insulin, etc.)
- Binary outcome: Diabetic (1) or Non-Diabetic (0)
- Source: Smith et al., 1988, National Institute of Diabetes

## Pipeline Steps
1. Data Cleaning — impute impossible zero values, IQR outlier clipping
2. Exploratory Data Analysis — distributions, correlation heatmap, box plots
3. Feature Engineering — 6 new features including BMI category, Glucose category, interaction terms
4. Model Training — XGBoost with 300 trees, class weighting, regularization
5. Evaluation — confusion matrix, ROC curve, feature importance
6. SHAP Explainability — beeswarm and bar plots for clinical interpretability
7. Prediction — individual patient risk scoring with High/Moderate/Low category

## Output Figures
| Figure | Description |
|---|---|
| fig1_distributions.png | Feature distributions by diabetes status |
| fig2_correlation.png | Feature correlation heatmap |
| fig3_boxplots.png | Box plots by diabetes status |
| fig4_evaluation.png | Full evaluation dashboard |
| fig5_eda_insights.png | Diabetes rate by Age, BMI, Glucose category |
| fig6_shap_summary.png | SHAP beeswarm plot |
| fig7_shap_bar.png | SHAP global feature importance |

## How to Run
Install dependencies:
```bash
pip install -r requirements.txt
```

Run the pipeline:
```bash
python diabetes_model.py
```

## Key Findings
- Glucose is the strongest single predictor of diabetes
- Engineered interaction features (Glucose x BMI) rank among top contributors
- Model achieves 85.2% recall meaning 85 out of 100 diabetic patients correctly identified
- SHAP analysis confirms clinical validity of feature importance

## Author
Khan Gulrez Shagufa Fazal Ahmed
Regulatory Affairs Specialist | MSc Bioanalytical Sciences

## Citation
If you use this code in your research, please cite this repository using 
the DOI badge above (available after Zenodo registration).
