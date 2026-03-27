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

This project addresses early risk prediction in realistic admission-time settings, where uncertainty is unavoidable and model outputs must remain clinically usable.

---

## Pipeline Overview

The pipeline is designed as a full end-to-end workflow, from raw data ingestion to clinically interpretable decision support outputs.

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

- Large-scale real-world hospitalization data
- Temporal validation across epidemic years
- Admission-only feature design to avoid post-admission leakage
- Ensemble of boosting models (LightGBM, XGBoost, HistGradientBoosting)
- Calibrated risk probabilities
- Decision-focused evaluation with Decision Curve Analysis
- Fairness evaluation across patient subgroups
- Interpretable surrogate model for ensemble behavior

---

## Getting Started

To explore the project:

1. Open `01_triage_pipeline_public.ipynb`
2. Run the notebook sequentially
3. Review the generated tables, figures, and evaluation outputs
4. Open `demo/index.html` to inspect the privacy-preserving offline prototype

---

## Modeling Approach

The repository includes:

- Logistic Regression (baseline)
- Gradient Boosting models
- Ensemble of top-performing models

The modeling strategy emphasizes not only discrimination, but also calibration and practical decision utility under temporal shift.

Evaluation metrics:

- ROC-AUC
- PR-AUC
- Brier score
- Decision Curve Analysis

---

## Clinical Perspective

The model is designed for early triage and clinical decision support using only admission-time data.

This reflects real hospital conditions, where detailed laboratory or imaging information may not yet be available, but decisions still need to be made.

---

## Interpretability

The project includes:

- calibrated risk probabilities for more reliable interpretation of predicted risk
- a surrogate model to approximate and explain ensemble behavior in a transparent form

---

## 🔗 Demo

Interactive offline prototype:

Open `demo/index.html`

The demo contains no patient-level data and is fully privacy-preserving.

---

## Author

**Valeria Kunichik**  
Machine Learning and Data Science focused on trustworthy decision support under uncertainty

---

## Future Work

- External validation on other countries and datasets
- Improved robustness under temporal distribution shift
- Integration into clinical workflows
- Extensions with explainable AI methods
- Validation of decision utility in broader high-stakes settings
