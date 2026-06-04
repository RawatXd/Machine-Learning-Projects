# 🌲 Ensemble Learning — Cancer Prediction
 
A hands-on exercise comparing **Decision Tree** and **Random Forest** classifiers on a medical dataset to predict cancer diagnosis. Includes parameter tuning experiments demonstrating how ensemble methods outperform single-tree models.
 
---
 
## 📋 Problem Statement
 
Given medical and lifestyle data for **1,500 patients**, the goal is to predict whether a patient has cancer (`diagnosis = 1`) or not (`diagnosis = 0`).
 
The project answers a practical question in medical ML:  
*How much do we gain by moving from a single Decision Tree to a Random Forest — and can thoughtful hyperparameter tuning push performance even further?*
 
---
 
## 📁 Repository Structure
 
```
Ensemble_learning_Exercise1/
│
├── assignment.ipynb            # Starter notebook (tasks without solutions)
├── assignment_solution.ipynb   # Completed notebook with full implementation
└── cancer_data.csv             # Dataset — 1,500 patients, 9 features
```
 
---
 
## 📊 Dataset Overview
 
**Source:** [Cancer Prediction Dataset – Rabie El Kharoua (Kaggle)](https://www.kaggle.com/datasets/rabieelkharoua/cancer-prediction-dataset)
 
| Feature | Type | Description |
|---|---|---|
| `age` | Integer (20–80) | Patient age |
| `gender` | Binary | 0 = Male, 1 = Female |
| `bmi` | Continuous (15–40) | Body Mass Index |
| `smoking` | Binary | 0 = No, 1 = Yes |
| `genetic_risk` | Categorical | 0 = Low, 1 = Medium, 2 = High |
| `physical_activity` | Continuous (0–10) | Hours/week of physical activity |
| `alcohol_intake` | Continuous (0–5) | Alcohol units/week |
| `cancer_history` | Binary | 0 = No, 1 = Yes |
| `diagnosis` *(target)* | Binary | 0 = No Cancer, 1 = Cancer |
 
No missing values. 1,500 rows × 9 columns.
 
---
 
## 🔬 Tasks Covered
 
**Task 1 — Data Preparation & Exploration**
- Load dataset and inspect shape, sample rows, and null values
**Task 2 — Decision Tree Classifier**
- 75/25 train-test split (`random_state=5`)
- Default `DecisionTreeClassifier`
- Evaluated with a full classification report
**Task 3 — Random Forest Classifier**
- `RandomForestClassifier(n_estimators=25)`
- Same train-test split for fair comparison
**Task 4 — Hyperparameter Tuning**
- Custom RF with: `n_estimators=50`, `criterion='entropy'`, `max_depth=15`, `min_samples_split=5`, `min_samples_leaf=3`, `max_features='log2'`, `bootstrap=False`
---
 
## 📈 Results Summary
 
| Model | Accuracy | Notes |
|---|---|---|
| Decision Tree (default) | **86%** | Baseline single-tree model |
| Random Forest (25 trees) | **91%** | +5% gain from ensembling |
| Random Forest (tuned) | **94%** | Best — entropy + depth control |
 
