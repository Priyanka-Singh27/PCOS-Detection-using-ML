🧠 PCOS Detection Web Application using Machine Learning

This project is a machine learning-based web application that detects **Polycystic Ovary Syndrome (PCOS)** using medical data. It provides a user-friendly interface where individuals can input their clinical parameters through a form, and the app returns the predicted probability of being diagnosed with PCOS. The system is built using Python and Flask, and leverages advanced feature selection techniques and optimized machine learning models for high diagnostic accuracy.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Technologies Used](#technologies-used)
- [How to Run](#how-to-run)
- [Results](#results)
- [Screenshots](#screenshots)
- [Contributors](#contributors)

---

## 📖 Overview

Polycystic Ovary Syndrome (PCOS) is a common hormonal disorder among women of reproductive age. Early and accurate diagnosis is crucial for treatment. This project aims to assist in diagnosis by using a combination of feature selection techniques and machine learning models to identify individuals at risk of PCOS. The application uses a user input form to collect health parameters and provides a real-time probability of diagnosis.

---

## 📊 Dataset

- **Source**: Kaggle  
- **Datasets**:  
  - Dataset 1: `541 samples × 44 features`  
  - Dataset 2: `1000 samples × 6 features`  
- **Collected from**: Multiple hospitals in India (2020 release)  
- **Final Merged Dataset**: Created by vertical union of common features from both datasets.  
- **Class Distribution (after merging)**:  
  - PCOS: 24.39%  
  - Non-PCOS: 73.61%

---

## 🧪 Methodology

<img width="1748" height="1240" alt="workflow chart" src="https://github.com/user-attachments/assets/83710d6d-47b4-4bf1-bb56-038791efee53" />

### 1. **Preprocessing**
- Column renaming for readability
- Union of datasets based on common features
- KNN imputation for missing values
- Z-score standardization
- SMOTE for class balancing

### 2. **Feature Selection**
Five techniques were evaluated:
- SHAP (Shapley Additive Explanations)
- Boruta
- Lasso (L1 Regularization)
- RFECV
- mRMR

**Final 20 Features Used**:
Menstrual_Irregularity, BMI, Testosterone_Levelng_dL, Follicle_No_R, Antral_Follicle_Count,
Weight_gainY_N, hair_growthY_N, Skin_darkening_Y_N, Follicle_No_L, Weight_Kg, CycleR_I,
PimplesY_N, AMHng_mL, Fast_food_Y_N, Hair_lossY_N, FSH_LH, Waistinch,
Marraige_Status_Yrs, Hipinch, Age


### 3. **Model Training & Evaluation**
- Train-test split: 85% training, 15% testing
- Models compared:
  - Random Forest
  - XGBoost
  - LightGBM
  - CatBoost
- Hyperparameter tuning with **Optuna**
- Final selection based on highest accuracy and generalization

✅ **Best Model**: CatBoost with SHAP-selected features  
✅ **Accuracy Achieved**: *~99.56%*

---

## 🛠 Technologies Used

- Python
- Flask
- HTML/CSS/JavaScript
- Pandas, NumPy
- Scikit-learn, SHAP, BorutaPy, Optuna
- XGBoost, LightGBM, CatBoost
- SMOTE (Imbalanced-learn)

---

## 🚀 How to Run

### 🔧 Requirements

Make sure Python 3.8+ is installed.

```bash
git clone https://github.com/Priyanka-Singh27/PCOS-Detection-using-ML.git
cd PCOS-Detection-using-ML
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
python app.py
```

## Results

<img width="812" height="544" alt="Screenshot 2025-07-21 185854" src="https://github.com/user-attachments/assets/769648b4-228e-4dab-a86d-07fd845a6cd3" />

## 🖼️Screenshots

![ss1](https://github.com/user-attachments/assets/6b753195-5dcd-40bc-98ca-307b75389778)

![ss2](https://github.com/user-attachments/assets/451a8a69-124c-4625-bf09-e5d7836c0352)

## Contributors
- Priyanka Singh
- Prathamesh Vishwakarma
- Pratik Deore
- Priyansh Gaur
- Vidya Pujari
