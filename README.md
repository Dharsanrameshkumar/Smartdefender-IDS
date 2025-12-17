# SmartDefender – Ensemble-Based Intrusion Detection System

SmartDefender is a research-grade machine learning pipeline designed for accurate intrusion detection on imbalanced network traffic data. The system leverages advanced feature engineering, data balancing, and ensemble learning to improve attack detection reliability.

## 🔍 Project Overview
Modern intrusion detection systems often suffer from class imbalance, where normal traffic dominates attack instances. This results in misleadingly high accuracy but poor recall for real attacks.

SmartDefender addresses this challenge by combining:
- Robust feature engineering
- SMOTE-based data balancing
- A stacked ensemble of XGBoost, LightGBM, and Random Forest
- Logistic Regression as a meta-learner
- Decision threshold optimization

## 📊 Dataset
- **Dataset:** UNSW-NB15
- **Classes:** Normal vs Attack traffic
- **Preprocessing:** One-hot encoding, scaling, feature selection

## 🧠 Model Architecture
- **Base Models:**  
  - XGBoost  
  - LightGBM  
  - Random Forest  
- **Meta Model:** Logistic Regression  
- **Ensemble Strategy:** Stacking

## ⚙️ Key Techniques
- RobustScaler for outlier handling  
- SelectKBest (ANOVA F-test) for feature selection  
- SMOTE for minority-class balancing  
- Threshold optimization for improved recall  

## 📈 Performance Highlights
- **Accuracy:** ~94.99%  
- **F1-Score:** ~96%  
- **AUC-ROC:** ~99.2%  
- Significant improvement in attack detection sensitivity

## 🗂 Project Structure
