
# MedBridge Cardiac Readmission — Model Comparison


## Overview

A clinical machine-learning case study comparing four tabular classifiers — Random Forest, XGBoost, LightGBM, and CatBoost — for flagging cardiac patients at risk of 30-day hospital readmission. Built around a fictional health system, MedBridge, running readmissions 5 points above the national average, the analysis works through 10,000 patient records spanning clinical and social determinants of health (SDOH) features: age, blood pressure, glucose, comorbidities, medication compliance, insurance, and ZIP code.

The deck walks from the business problem, through exploratory data analysis, into a head-to-head model comparison, and ends on a deployment recommendation.

## The Core Trade-Off

The headline finding is a classic accuracy-vs-recall trap: Random Forest posts the highest raw accuracy (0.823) but catches only 15% of patients who actually get readmitted. In a hospital setting, a missed high-risk patient is far costlier than a false alarm on a low-cost intervention like a follow-up call — so accuracy alone is the wrong metric to optimize.

| Model | Accuracy | Recall | F1 | AUC |
|---|---|---|---|---|
| Random Forest | 0.823 | 0.149 | 0.244 | 0.741 |
| XGBoost | 0.760 | 0.414 | 0.397 | 0.710 |
| LightGBM | 0.744 | 0.592 | 0.469 | 0.753 |
| **CatBoost** | 0.734 | **0.613** | 0.468 | **0.764** |

**CatBoost** comes out ahead on the metrics that matter clinically — best recall (61%) and best AUC (0.764) — at a deliberate cost in raw accuracy, and it handles the insurance/ZIP categorical features natively without preprocessing.

## What Drives Risk

Exploratory analysis surfaced clear, clinically sensible gradients: prior admissions is the steepest risk driver (climbing from ~10% with no prior admissions to over 70% at four or more), followed by comorbidity burden (Charlson Comorbidity Index) and age, with medication adherence acting as a protective factor. These align with the correlation coefficients computed against the readmission outcome (prior admissions 0.29, comorbidities 0.21, age 0.12, adherence −0.13).

## Recommendation

Deploy CatBoost as a discharge-time risk score. On the 2,000-patient holdout set it flags 234 of 382 true high-risk patients (61% recall) — 148 still slip through, which is the clear gap to close in a future iteration — at a precision of 0.38. For an intervention as low-cost as a follow-up call, that trade-off is clinically worth making, and it acts proactively before discharge rather than relying on a static post-hoc score.

## Skills Demonstrated

- Imbalanced classification (80.9/19.1 class split) and metric selection beyond accuracy
- Comparative model evaluation across tree-based ensemble methods (Random Forest, XGBoost, LightGBM, CatBoost)
- Healthcare/SDOH feature engineering and correlation analysis
- Translating model trade-offs (precision/recall) into a clinical and operational recommendation

[View the full presentation](./assets/MedBridge_Readmission_Presentation.pptx)
