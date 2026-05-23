# 🏥 Patient Health Risk Prediction — Linear, Lasso & Ridge Regression
 
A machine learning project that applies **Linear Regression with L1 (Lasso) and L2 (Ridge) Regularization** to predict a composite health risk score for patients based on various health indicators.
 
---
 
## 📌 Problem Statement
 
Given health records of patients including vitals, lifestyle habits, and biological markers, the goal is to build a regression model that accurately **predicts the health risk score**. The project compares standard Linear Regression against regularized models (Lasso and Ridge) across multiple alpha values to identify the best-performing approach.
 
---
 
## 📂 Project Structure
 
```
patient-health-risk-prediction/
├── assignment.ipynb              # Main Jupyter Notebook
├── patient_health_data.csv       # Dataset
├── requirements.txt              # Python dependencies
└── README.md
```
 
---
 
## 📊 Dataset
 
The dataset contains **250 rows** and **12 columns** of patient health records:
 
| Column | Description |
|---|---|
| `age` | Age of the patient |
| `bmi` | Body Mass Index |
| `blood_pressure` | Blood pressure reading |
| `cholesterol` | Cholesterol level |
| `glucose` | Glucose level |
| `insulin` | Insulin level |
| `heart_rate` | Heart rate |
| `activity_level` | Physical activity level |
| `diet_quality` | Quality of diet score |
| `smoking_status` | Smoking status — Yes (1) / No (0) |
| `alcohol_intake` | Alcohol intake amount |
| `health_risk_score` | Target variable — composite health risk score |
 
---
 
## 🔧 Tasks Covered
 
### Task 1 — Data Preparation & Exploration
- Loaded dataset from `.csv` (250 rows × 12 columns)
- Checked shape, first few rows, and missing values (no nulls found)
- Encoded categorical variable `smoking_status`: Yes → 1, No → 0
### Task 2 — Model Training & Comparison
- Features: all columns except `health_risk_score`
- Target: `health_risk_score`
- Train/test split: **75% train / 25% test** (`random_state=42`)
- Trained and evaluated three model types:
| Model | Alpha | R² Score |
|---|---|---|
| Linear Regression | — | 0.7639 |
| Lasso (L1) | 0.01 | 0.7641 |
| Lasso (L1) | 0.1 | 0.7660 |
| Lasso (L1) | 1.0 | 0.7820 |
| Lasso (L1) | **10.0** | **0.7873** ✅ |
| Ridge (L2) | 0.01 | 0.7639 |
| Ridge (L2) | 0.1 | 0.7639 |
| Ridge (L2) | 1.0 | 0.7640 |
| Ridge (L2) | 10.0 | 0.7650 |
 
---
 
## 📈 Key Findings
 
- **Lasso Regression (alpha=10.0)** achieved the best R² of **0.7873**, outperforming both the default Linear Regression and all Ridge variants
- Lasso (L1) showed stronger improvement with increasing alpha, suggesting some features contribute little and benefit from shrinkage to zero
- Ridge (L2) showed minimal improvement over base Linear Regression, indicating multicollinearity is not a major issue in this dataset
---
 
## 🚀 How to Run
 
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/patient-health-risk-prediction.git
   cd patient-health-risk-prediction
   ```
 
2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
 
3. **Launch the notebook**
   ```bash
   jupyter notebook assignment.ipynb
   ```
 
---
 
## 🛠️ Tech Stack
 
- Python 3.x
- pandas, numpy
- scikit-learn
- matplotlib
---
 
## 📄 License
 
This project is for educational purposes only.
