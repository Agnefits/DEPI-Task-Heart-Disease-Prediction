# 🫀 Heart Disease Prediction Using Logistic Regression

---

## 📌 Project Information

**Names:**  
- Abdallah Salah  
- Ahmed Adel  
- Morad Ahmed  
- Shahd Mohamed  
- Yussef Ahmed  

**Group Code:** AST4_AIS2_S1  
**Instructor:** Eng. Mahmoud Talaat  
**Program:** DEPI – Round 4  
**Track:** AI & Data Science – Microsoft Machine Learning Engineer  

---

## 1. Problem Overview

The objective of this project is to predict whether an individual has **heart disease** based on health, lifestyle, and demographic features.

This is a **binary classification** problem:

- **0** → No heart disease  
- **1** → Heart disease  

Accurate early prediction can support preventive healthcare decisions and risk assessment.

---

## 2. Dataset Description

The dataset contains **16,859 records** with **26 features**, covering numerical, binary, and categorical health indicators.

### 🔹 Feature Types

#### Numerical Features
- **BMI**
- **PhysicalHealth**
- ~~MentalHealth~~ *(removed)*
- ~~SleepTime~~ *(removed)*

#### Categorical / Binary Features (already encoded)
- Smoking  
- AlcoholDrinking  
- Stroke  
- PhysicalActivity  
- GenHealth  
- Asthma  
- KidneyDisease  
- SkinCancer  

#### One-Hot Encoded Features
- Race (Race_White, Race_Black, etc.)
- Diabetes status (Diabetic_Yes, Diabetic_No, etc.)

#### Target Variable
- **HeartDisease**

---

## 3. Data Splitting Strategy

The dataset was split as follows:

- **80%** Training set  
- **20%** Testing set  

A **stratified split** was applied to preserve the original distribution of heart disease cases in both subsets.  
This ensures fair evaluation and reliable performance metrics.

---

## 4. Model Selection

We used **Logistic Regression**, a well-established and interpretable algorithm for binary classification.

### Why Logistic Regression?
- Suitable for binary outcomes  
- Computationally efficient  
- Produces probabilistic predictions  
- Widely adopted in healthcare risk modeling  

---

## 5. Preprocessing and Pipeline

Since all categorical variables were already encoded, no additional encoding was required.

### Preprocessing Steps
- **RobustScaler** was applied to numerical features to reduce the influence of outliers  
- Binary and boolean features were passed directly to the model  
- All steps were integrated into a **Pipeline** to:
  - Prevent data leakage  
  - Ensure reproducibility  
  - Simplify experimentation  

---

## 6. Model Performance

The trained Logistic Regression model achieved:

- **Training Accuracy:** 90.24%  
- **Testing Accuracy:** 90.50%  

---

## 7. Performance Interpretation

The close similarity between training and testing accuracy indicates:

- Strong generalization to unseen data  
- No evidence of overfitting  
- Stable and reliable model behavior  

The model correctly predicts heart disease status in approximately **9 out of 10 cases**.

---

## 8. Practical Implications

This model can serve as a **baseline clinical decision-support tool**, helping identify individuals at higher risk of heart disease.

Due to its interpretability, Logistic Regression allows transparent analysis of how different health factors influence predictions—an important requirement in healthcare applications.

---

## 9. Future Improvements

Potential extensions of this project include:

- Evaluating additional metrics such as **ROC–AUC** and **confusion matrix**  
- Handling class imbalance using `class_weight='balanced'`  
- Analyzing feature importance using model coefficients  
- Experimenting with advanced models (Random Forest, XGBoost)  
- Hyperparameter tuning using **GridSearchCV**

---

## 10. Conclusion

This project demonstrates that **careful preprocessing** and **proper pipeline design** can achieve strong predictive performance without relying on complex models.

The Logistic Regression model delivered:
- High accuracy  
- Good generalization  
- Strong interpretability  

These qualities make it a reliable and practical choice for healthcare-related prediction tasks.

---
