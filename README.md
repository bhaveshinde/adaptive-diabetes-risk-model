This code builds an adaptive diabetes risk prediction system using logistic regression. The model is designed to improve itself when data, features, or patient populations change.

Key Steps Explained

1. Baseline Model
Trains a standard logistic regression model using scaled clinical features.
Uses cross-validation and hyperparameter tuning to establish a strong baseline.
Evaluates performance with F1 score, ROC-AUC, and confusion matrix.

2. Data Tailoring (Feature Engineering)
Adds medically meaningful engineered features (e.g., insulin-to-glucose ratio, BMI × glucose).
Retrains the model on the enriched feature set.
Demonstrates how new features can improve predictive performance.

3. Clustering + Prediction
Applies K-Means clustering to learn hidden patient “phenotypes.”
Adds the cluster label as a new feature.
Retrains the classifier, allowing it to leverage population structure to boost accuracy.

4. Cohort Shift & Drift Detection
Splits patients into younger vs. older cohorts based on age.
Uses the Kolmogorov–Smirnov test to detect distribution drift between cohorts.

5. Model Adaptation
When drift is detected, the model relearns clusters on combined cohorts.
Retrains the classifier on the updated data distribution.
Evaluates performance on the new cohort to confirm successful adaptation.


Why This Matters
Demonstrates real-world ML behavior, where data evolves over time.
Combines feature engineering, unsupervised learning, supervised learning, and drift detection.
Shows how to build models that remain accurate across changing populations.
