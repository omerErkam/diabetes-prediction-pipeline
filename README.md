# Diabetes Prediction Using Machine Learning Classification Algorithms

## 📌 Project Overview
Chronic diabetes is a widespread global health issue. Early and accurate diagnosis plays a critical role in effective treatment and restoring patient health. This project applies machine learning classification algorithms to predict the onset of diabetes based on diagnostic measurements from the UCI Pima Indians Diabetes Database. The primary objective is to evaluate multiple predictive models and identify the most accurate classifier to streamline the diagnostic process.

## 🛠 Tech Stack & Tools
* **Programming Language:** Python
* **Data Manipulation & Preprocessing:** Pandas, NumPy
* **Machine Learning Framework:** Scikit-Learn (scikit-learn)
* **Data Visualization:** Matplotlib
* **Development Environment:** Google Colab / Jupyter Notebook

## 🔬 Methodology
Our pipeline is designed to handle medical data anomalies and rigorously evaluate various models:

1. **Data Preprocessing & Class-Based Imputation:**
   * The dataset contained medically impossible `0` values in critical features (e.g., BMI, Blood Pressure, Glucose, Skin Thickness).
   * Instead of a standard global mean/median imputation, we implemented a **class-based median imputation strategy**. Missing values were calculated and replaced separately depending on whether the patient was classified as diabetic or healthy.
2. **Feature Engineering:**
   * Applied Exploratory Data Analysis (EDA) to extract two new predictive features based on clinical thresholds (e.g., identifying high-risk patients with a blood pressure over 80 and glucose over 105).
3. **Model Training & Pipeline:**
   * Split the dataset into a strict **70% Training / 30% Testing** split.
   * Trained and evaluated five distinct machine learning classifiers: Random Forest (RF), K-Nearest Neighbors (KNN), Support Vector Machine (SVM), Artificial Neural Network (ANN), and Decision Tree (DT).

## 📊 Results & Evaluation
The models were evaluated using Accuracy, Precision, Recall, and F1-Score metrics. The **Random Forest** algorithm emerged as the highest-performing model, demonstrating its robustness in handling clinical data.

| Algorithm | Accuracy | Precision | Recall | F1-Score |
| :--- | :--- | :--- | :--- | :--- |
| **Random Forest (RF)** | **87.01%** | **0.86** | **0.85** | **0.85** |
| K-Nearest Neighbors | 86.15% | 0.85 | 0.84 | 0.84 |
| Decision Tree (DT) | 83.55% | 0.82 | 0.81 | 0.82 |
| Support Vector Machine | 83.12% | 0.81 | 0.83 | 0.82 |

*(Note: The implementation successfully reproduced the high-performance baseline established in the original Nahzat & Yağanoğlu (2021) study.)*
