🧠 Mental Health Risk Classification
📌 Introduction
Mental health in the workplace is a growing concern, and early detection of risk levels is essential for providing timely support and intervention.
In this project, we aim to classify individuals into Low, Medium, or High mental health risk categories using machine learning techniques.

Our model is built on a synthetic dataset of 10,000 individuals, generated to reflect realistic trends found in global workplace mental health studies.
The data includes variables such as demographics, employment status, mental health history, treatment-seeking behavior, and social support — while maintaining complete privacy and anonymity.

🎯 Project Objective
Predict mental health risk levels (Low, Medium, High)

Prioritize recall for High-risk individuals to ensure they are correctly identified

Evaluate and compare multiple machine learning models to find the most effective approach

🧪 Methodology
We followed a structured pipeline:

1. Exploration
Performed data exploration using summary statistics and visualizations

Analyzed correlations between features and mental health risk levels

2. Feature Selection
Selected features based on correlation strength and interpretability

Final selected features: productivity_score, anxiety_score

3. Preprocessing
Encoded categorical variables

Split dataset into training and testing sets with stratified sampling

4. Model Training & Evaluation
Trained and compared four classifiers:

Logistic Regression

Random Forest

XGBoost

LightGBM

Used evaluation metrics:

Accuracy

Precision

Recall

F1 Score (macro)

Focused on High-risk recall as a critical metric

📈 Results
Model	Accuracy	High Recall	F1 Score (Macro)
Logistic Regression	0.890	0.87	0.88
Random Forest	0.857	0.86	0.84
XGBoost	0.887	0.87	0.88
LightGBM (Tuned)	0.872	0.93	0.87

⚡ After tuning LightGBM (with recall_macro as scoring), we achieved 93% recall for High-risk cases

Slight trade-off in accuracy was acceptable to increase model sensitivity for critical predictions

🔧 Tuning Strategy
Used GridSearchCV to optimize LightGBM hyperparameters:

learning_rate, num_leaves, n_estimators, max_depth

Scoring objective: recall_macro

Goal: Maximize recall across all classes, especially High-risk

💡 Key Insights
Productivity score and anxiety score were highly correlated with mental health risk

Simple models (like Logistic Regression) performed competitively

Prioritizing recall over accuracy led to more responsible, real-world-aligned performance

🚀 Future Improvements
Experiment with custom class weights to further emphasize High-risk detection

Add more features such as stress_level or mental_health_history

Test model robustness on unseen or noisy data

Deploy model for potential real-time mental health screening scenarios

