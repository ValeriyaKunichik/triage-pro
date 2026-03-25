# TRIAGE PRO: Early Clinical Risk Prediction under Epidemic Conditions

This repository presents a reproducible machine learning pipeline for early-stage clinical risk prediction based on large-scale epidemiological data.

The project focuses on predicting patient outcomes at the moment of hospital admission using only information available at that stage (EHR-lite setting), reflecting real-world clinical constraints.

---

## Motivation

During epidemic outbreaks, clinicians must make decisions under uncertainty and with limited data.

Many existing machine learning models:
- rely on post-admission features such as laboratory tests or imaging;
- suffer from limited generalization across time and settings;
- provide insufficient interpretability for real clinical use.

This project focuses on realistic early prediction under these constraints.

---

## Pipeline Overview

The pipeline includes:

- multi-year data ingestion;
- schema harmonization;
- feature construction (EHR-lite);
- outcome definition;
- data cleaning and validation;
- exploratory data analysis (EDA);
- model training (baseline + boosting);
- ensemble construction;
- probability calibration (isotonic regression);
- decision curve analysis (clinical utility);
- fairness analysis;
- surrogate interpretation;
- demo generation.

---

## Key Features

- Large-scale real-world dataset
- Temporal validation across epidemic years
- Admission-only feature design (no data leakage)
- Ensemble of boosting models (LightGBM, XGBoost, HGB)
- Calibrated risk probabilities
- Decision Curve Analysis
- Fairness evaluation
- Interpretable surrogate model

---

## Project Structure

```text
triage-pro/
├── 01_triage_pipeline_public.ipynb # main pipeline
└── README.md
```

---

## Getting Started

1. Open the notebook:
   `01_triage_pipeline_public.ipynb`

2. Run all cells step by step

3. Review generated outputs (tables, figures, metrics)

---

## Modeling Approach

The repository includes:

- Logistic Regression (baseline)
- Gradient Boosting models
- Ensemble of top-performing models

Evaluation metrics:

- ROC-AUC
- PR-AUC
- Brier score
- Decision Curve Analysis

---

## Clinical Perspective

The model is designed for early triage and clinical decision support using only admission-time data.

This reflects real hospital conditions, where detailed diagnostic information may not yet be available.

---

## Interpretability

The project includes:

- calibrated risk probabilities
- surrogate model for explaining ensemble behavior

---

## Author

**Valeria Kunichik**  
Machine Learning / Data Science / Clinical AI

---

## Future Work

- External validation on other countries and datasets
- Robustness to temporal distribution shift
- Integration into clinical workflows
- Extensions with explainable AI methods
