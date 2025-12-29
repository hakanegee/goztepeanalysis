# Submission 3 — ML Methods (Pre vs Post Sport Republic)

## Objective
We apply supervised ML to test whether player-season performance metrics can classify observations as **Pre–Sport Republic** vs **Post–Sport Republic**, and to interpret which features drive the separation.

## Problem Setup
- **Task:** Binary classification (Pre vs Post)
- **Target (y):** period ∈ {pre, post}
- **Features (X):** selected FBref performance metrics (e.g., 90s, goal contributions per 90, defensive actions)

## Models
1. **Logistic Regression** (baseline, interpretable)
2. **Random Forest Classifier** (nonlinear, feature importance)

## Workflow
1. Data cleaning and train/test split
2. Model training with standard evaluation
3. Metrics: Accuracy, F1-score, Confusion Matrix
4. Interpretation via coefficients (LR) and feature importance (RF)

## Deliverables
- `Analysis_sub3.ipynb` contains all code, results, and visual outputs.
- This README summarizes the ML objective, approach, and evaluation.
