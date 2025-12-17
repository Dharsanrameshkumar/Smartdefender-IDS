# 🛡️ SmartDefender – Intrusion Detection System (IDS)

**SmartDefender** is a **machine-learning–based Intrusion Detection System (IDS)** designed to detect malicious network traffic with high accuracy using an **advanced stacked ensemble model**.
This project applies **feature engineering, class imbalance handling, and ensemble learning** on the **UNSW-NB15 dataset** to achieve robust intrusion detection performance.

> 📌 **Project Type:** Mini Project / Research Project
> 📊 **Domain:** Cyber Security, Machine Learning
> 🎓 **Degree:** B.E. Computer Science and Engineering(cyber security)

---

## 📌 Key Features

* Advanced **feature engineering** for network traffic
* Handles **class imbalance** using SMOTE
* **Stacked Ensemble Model**:

  * XGBoost
  * LightGBM
  * Random Forest
  * Logistic Regression (Meta-Learner)
* **Threshold optimization** for improved detection
* Robust preprocessing and feature selection
* Research-oriented, modular codebase
* High accuracy suitable for academic evaluation

---

## 🧠 Model Architecture

```text
Input Network Traffic
        ↓
Feature Engineering
        ↓
Scaling (RobustScaler)
        ↓
Feature Selection (Top-K ANOVA)
        ↓
SMOTE (Train Data Only)
        ↓
Base Models
  ├── XGBoost
  ├── LightGBM
  └── Random Forest
        ↓
Meta-Learner (Logistic Regression)
        ↓
Final Intrusion Prediction
```

---

## 📂 Project Structure

```text
Smartdefender-IDS/
│
├── ai_model/
│   ├── train_model.py        # Main training script
│
├── dataset/
│   ├── UNSW_NB15_training-set.csv
│   ├── UNSW_NB15_testing-set.csv
│
├── models/                   # Saved models (ignored in Git)
│
├── logs/
│   └── training_log.txt
│
├── requirements.txt
├── README.md
├── .gitignore
```

---

## 📊 Dataset

**UNSW-NB15 Dataset**

* Realistic modern network traffic
* Normal and attack categories
* Features include:

  * Protocol, service, state
  * Packet statistics
  * Byte flow metrics
  * Timing and jitter attributes

📌 **Target Variable:**

* `0` → Normal Traffic
* `1` → Attack Traffic

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Dharsanrameshkumar/Smartdefender-IDS.git
cd Smartdefender-IDS
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

Activate:

```bash
# Windows
venv\Scripts\activate

# Linux / Mac
source venv/bin/activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🚀 Training the Model

Run the training pipeline:

```bash
cd ai_model
python train_model.py
```

The pipeline performs:

1. Data loading
2. Feature engineering
3. Scaling and feature selection
4. SMOTE balancing
5. Ensemble training
6. Threshold optimization
7. Evaluation
8. Model & metric saving

---

## 📈 Evaluation Metrics

The system evaluates the following metrics:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-Score**
* **AUC-ROC**

📌 Threshold optimization improves classification reliability.

---

## 🧪 Sample Output

```text
Accuracy   : 94.99%
Precision  : 96.15%
Recall     : 96.00%
F1 Score   : 96.08%
AUC-ROC    : 99.21% 
```

> Results may vary slightly depending on system and dataset splits.

---

## 🔒 Model Storage Policy

To comply with GitHub size limits:

* Trained models (`.pkl`) are **not committed**
* Models are saved locally under:

```text
models/
```

Ignored via `.gitignore`.

---

## 📌 Applications

* Network Intrusion Detection
* Cybersecurity monitoring
* Research on ensemble learning
* Academic ML projects
* Benchmarking IDS models

---

## 🧩 Technologies Used

* Python
* Scikit-learn
* XGBoost
* LightGBM
* Imbalanced-Learn
* Pandas, NumPy
* Joblib

---

## 🔮 Future Enhancements

* Real-time packet capture integration
* Deep learning models (LSTM / Autoencoders)
* Live dashboard for traffic monitoring
* Deployment using Flask / FastAPI
* Explainable AI (SHAP)

---

## 👨‍🎓 Author

**Dharsan R**
B.E. Computer Science and Engineering(Cyber Security)
Saveetha Engineering College

📧 GitHub: [Dharsanrameshkumar](https://github.com/Dharsanrameshkumar)

---

## 📜 License

This project is intended for **academic and research purposes only**.
Not for commercial deployment without permission.

---

⭐ **If you like this project, consider starring the repository!**

---

