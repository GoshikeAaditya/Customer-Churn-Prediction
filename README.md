# 📊 Customer Churn Prediction — Model Development, Validation, and Deployment  

## 🧠 Overview  
This project applies **Inferential Statistics** and **Predictive Analytics** techniques to forecast customer churn in the telecom industry. It combines **Logistic Regression** and a **Random Forest (CHAID-like)** model to identify high-risk customers and provide actionable insights for customer retention.  

Customer churn represents one of the biggest challenges for telecom service providers. By predicting which customers are likely to leave, organizations can take proactive steps such as offering personalized incentives or improving customer service to retain them.  

---

## 🎯 Objectives  
- Predict which customers are most likely to churn using real-world data.  
- Identify key behavioral, demographic, and billing factors influencing churn.  
- Build interpretable and high-performing predictive models.  
- Validate models using multiple performance metrics.  
- Develop a framework for deployment, monitoring, and retraining.  

---

## 🗂️ Dataset  
**Dataset Name:** `Iranian Churn.csv`  

**Description:**  
A telecom dataset containing customer demographic, behavioral, and billing information. Each record represents a unique customer with a binary target variable **Churn (1 = churned, 0 = retained)**.  

**Dataset Size:** ~3,000 records × 20 attributes  

**Key Features:**  
- **Demographics:** Gender, age, region  
- **Service Data:** Contract type, internet service, tenure  
- **Billing Info:** Monthly charges, total charges, payment method  
- **Target Variable:** `Churn`  

This dataset provides a realistic representation of telecom customer behavior, allowing for meaningful churn analysis and model generalization.  

---

## ⚙️ Data Preparation Steps  
Data preprocessing ensures that the dataset is clean, consistent, and ready for modeling.  

1. **Data Cleaning:** Removed duplicates, standardized text, corrected datatypes.  
2. **Handling Missing Values:** Imputed missing data using median/mode.  
3. **Outlier Treatment:** Detected and capped extreme anomalies.  
4. **Encoding:** Applied Label and One-Hot Encoding for categorical variables.  
5. **Scaling:** Standardized numerical features for uniformity.  
6. **Train-Test Split:** Stratified sampling (75:25) for balanced model evaluation.  

---

## 🧩 Model Development  
Two models were built and compared for performance and interpretability:  

### 1. Logistic Regression  
- Establishes linear relationships between predictors and churn probability.  
- Offers high interpretability with coefficients indicating feature influence.  

### 2. Decision Tree (CHAID-like)  
- Built using Scikit-learn’s `DecisionTreeClassifier()`.  
- Mimics CHAID segmentation logic using Gini Impurity.  
- Generates readable, rule-based outputs for business interpretation.  

---

## 📈 Model Evaluation  

| Metric | Logistic Regression | Decision Tree |
|:--|:--:|:--:|
| **Accuracy** | 0.83 | 0.81 |
| **ROC-AUC** | 0.87 | 0.84 |
| **Precision** | 0.73 | 0.70 |
| **Recall** | 0.68 | 0.64 |
| **F1-Score** | 0.70 | 0.67 |

**Insights:**  
- Logistic Regression achieved better overall performance and generalization.  
- The Decision Tree model provided interpretable segmentation rules.  

**Top Predictors of Churn:**  
- Contract Type  
- Tenure  
- Monthly Charges  
- Payment Method  

---

## 📊 Visualizations  
- **ROC Curves** – to compare classification performance.  
- **Lift and Gains Charts** – to measure business effectiveness.  
- **Confusion Matrix** – for true vs. false predictions.  
- **Feature Importance Plot** – highlighting top churn drivers.  

---

## 🚀 Deployment Framework  
The model deployment plan ensures continuous usability and accuracy through MLOps principles:  

### 1. Model Monitoring  
- Track key metrics (accuracy, ROC-AUC, calibration).  
- Detect **data drift** and **model drift** in production.  
- Use real-time dashboards for performance tracking.  

### 2. Model Updating & Retraining  
- Retrain models every 3–6 months with new customer data.  
- Employ version control and validation before redeployment.  
- Automate retraining using tools like **MLflow**, **Airflow**, or **Kubeflow**.  

### 3. Meta-Modeling (Future Scope)  
- Combine multiple models (e.g., Logistic + Random Forest) via stacking or blending for better performance.  

---

## 💡 Key Findings  
- Short-term customers with **month-to-month contracts** and **high monthly charges** are most likely to churn.  
- Long-term customers on **yearly or two-year contracts** exhibit higher loyalty.  
- Payment method and tenure significantly affect retention likelihood.  

These insights can guide telecom providers to design targeted retention campaigns and improve customer satisfaction.  

---

## 🧭 Conclusion  
This project demonstrates how combining **Inferential Statistics** with **Machine Learning** can create a robust, interpretable, and business-friendly churn prediction system.  

By implementing this analytical pipeline, organizations can:  
- Reduce churn rates through proactive engagement.  
- Strengthen customer relationships.  
- Achieve data-driven business decision-making.  

The developed framework serves as a scalable model that can be applied across industries like banking, e-commerce, and insurance where customer retention is critical.  

---

## 👥 Contributors  
**Team Members:**  
- **Aaditya Goshike** – RA2211047010009  
- **M. Benarjee** – RA2211047010012  

**Course:** 21AIC401T – *Inferential Statistics and Predictive Analysis*  
**Branch:** B.Tech. Artificial Intelligence – A  

---

## 📜 License  
This project is licensed under the **MIT License** — you are free to use, modify, and distribute this project with attribution.  
