# Mental-Health-Risk-Classification
Introduction
Mental health in the workplace is a critical issue, and understanding its patterns is crucial for designing effective policies and interventions.
In this project, we focused on classifying individuals into low, medium, or high mental health risk categories.
It also seeks to identify the best predictor of mental health risk
Our predictions are based on a variety of features, including demographic information, employment details, and levels of support in the workplace.
To build our model, we used data from a global mental health survey of 10,000 individuals.
The dataset is synthetic, meaning it's been generated to reflect realistic patterns observed in workplace mental health studies, while also ensuring complete privacy and anonymity for all participants.
Methodology
Our goal in this project is to classify individuals into low, medium, or high mental health risk categories using machine learning.
We started by exploring all the features using visualizations and summary statistics to better understand how each variable relates to mental health risk.
Next, we moved to feature selection, where we tried to identify the most relevant variables so that we kept only features that added value to the model.
Then came preprocessing: the data was already clean, so there was no need to, for example, handle missing values. However, we did need to do encoding of the categorical features to prepare the dataset for modeling.
Finally, we trained and evaluated four classifiers — Logistic Regression, Random Forest, XGBoost, and LightGBM — and compared their performance using metrics like accuracy and recall to determine the best-performing model.
