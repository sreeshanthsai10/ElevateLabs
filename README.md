# 🚢 AI & ML INTERNSHIP - Task 1: Data Cleaning & Preprocessing

## Overview
This repository contains the solution for **Elevate Labs AI & ML INTERNSHIP Task 1**. The goal of this task was to demonstrate proficiency in cleaning and preparing a raw dataset for subsequent use in Machine Learning models.

## 🎯 Objective
To transform the raw **Titanic Dataset** into a clean, numerical, and scaled format by systematically implementing core data preprocessing steps.

## 💾 Dataset
The project uses the classic **`Titanic-Dataset.csv`**.

## 🛠️ Implementation & Code
The preprocessing logic is contained in the Python script (e.g., `titanic_preprocessing.py`).

### Mini Guide Steps Implemented:

| Step | Action Taken | Techniques Used |
| :--- | :--- | :--- |
| **1. Exploration** | Loaded data and checked for missing values and data types. | `df.info()`, `df.isnull().sum()` |
| **2. Handle Missing Values** | **Dropped**: `Cabin`, `Name`, `Ticket`, `PassengerId`. **Imputed `Age` and `Fare`** with the **median**. **Imputed `Embarked`** with the **mode**. | Median Imputation, Mode Imputation, `df.drop()`, `df.fillna()` |
| **3. Encoding** | Converted nominal categorical features (`Sex`, `Embarked`, `Pclass`) into numerical format. | **One-Hot Encoding** (`pd.get_dummies()`, `drop_first=True`) |
| **4. Feature Scaling** | Scaled numerical features (`Age`, `Fare`) to a range between 0 and 1. | **StandardScaling** from `StandardScaler` |
| **5. Outlier Handling** | Detected and managed extreme values in the `Age` column. | **Interquartile Range (IQR) Method** used to **Cap** the outliers. |

## 💻 Technologies & Libraries
* **Python 3**
* **Pandas** (Data manipulation)
* **NumPy** (Numerical operations)
* **Scikit-learn** (Feature scaling)
* **Matplotlib / Seaborn** (Visualization for outlier detection)

---
*This project successfully prepares the Titanic data, resulting in a dataset with no missing values, all numerical features, and scaled values, making it ready for model training.*
