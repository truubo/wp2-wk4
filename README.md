# Interpretation
- **Which model performed better?** Based on test F1-score, Logistic Regression performed best (F1=0.289).
- **Overfitting check:** Logistic Regression train-test gap = 0.017; Random Forest train-test gap = 0.203. A larger gap suggests more overfitting risk.
- **False positives vs false negatives:** For heart disease, false negatives are worse (missed diagnoses). That makes recall the most critical metric.
- **Precision/recall tradeoff:** LR recall=0.491, RF recall=0.000; LR precision=0.205, RF precision=0.000. Choose the model with higher recall if missing positives is costlier.
- **Confusion matrix pattern:** Compare the Actual 1 / Pred 0 cell to see which model misses more true positives.
- **Feature importance:** LR top features: cat__Stress Level_Low, cat__Stress Level_Medium, cat__Sugar Consumption_Low. RF top features: num__Homocysteine Level, num__CRP Level, num__Sleep Hours.
- **Next improvements:** (1) Tune hyperparameters with cross-validation, (2) Try class-weighting or threshold tuning to improve recall.