# 🧠 Mental Health Risk Classification

> A machine learning project to classify individuals into **Low**, **Medium**, or **High** mental health risk levels based on workplace-related survey data.  
> Focus: Improve **recall for High-risk cases** using model tuning and careful feature selection.

---

## 📌 Project Overview

- 📊 Dataset: Synthetic mental health survey data (10,000 individuals)  
- 🎯 Goal: Predict mental health risk level and prioritize early detection of **high-risk individuals**
- 🔧 Tools: Python, Pandas, Scikit-learn, XGBoost, LightGBM, Matplotlib, Seaborn

---

## 🧪 Methodology

### 1. **Explore**
- Analyzed distributions and correlations between features and risk levels

### 2. **Select**
- Chose most predictive features based on insight & correlation  
  → Final features: `productivity_score`, `anxiety_score`

### 3. **Preprocess**
- Encoded categorical variables  
- Stratified train/test split for balanced evaluation

### 4. **Train**
- Trained and compared four models:
  - Logistic Regression
  - Random Forest
  - XGBoost
  - LightGBM

### 5. **Tune**
- Tuned LightGBM with `GridSearchCV`  
- Scoring metric: `recall_macro`  
- Goal: Improve **High-risk recall**

---

## 📈 Results Summary

| Model               | Accuracy | High Recall | F1 Score (Macro) |
|--------------------|----------|-------------|------------------|
| Logistic Regression | 0.890    | 0.87        | 0.88             |
| Random Forest       | 0.857    | 0.86        | 0.84             |
| XGBoost             | 0.887    | 0.87        | 0.88             |
| **LightGBM (Tuned)**| 0.872    | **0.93**    | 0.87             |

> ✅ LightGBM tuning helped us **maximize recall for High-risk individuals**  
> 🎯 Even with slight accuracy tradeoff, the model became more sensitive and intervention-focused

---

## 💡 Key Insights

- `productivity_score` and `anxiety_score` are strong predictors of mental health risk  
- LightGBM outperformed others in **recall**, especially for High risk  
- Simpler models (like Logistic Regression) still gave strong performance

---

## 🚀 Future Work

- Add more behavioral and stress-related features (e.g., `stress_level`, `mental_health_history`)
- Fine-tune with **custom class weights**
- Evaluate generalizability on noisy or external data

---

## 👩‍💻 Authors

- [Your Name]  
- [Teammate 1]  
- [Teammate 2]

---

## 📁 Project Structure

