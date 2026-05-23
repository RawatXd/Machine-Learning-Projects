## 📢 Social Network Ads — Purchase Prediction
 
A machine learning project that applies **Logistic Regression** to predict whether a social network user will purchase a product based on their age, gender, and estimated salary.
 
---
 
## 📌 Problem Statement
 
Given basic demographic information about users from a social network platform, the goal is to build a binary classification model that predicts **purchase behavior** — whether a user bought a product (1) or not (0).
 
---
 
## 📂 Project Structure
 
```
social-network-ads-classification/
├── assignment_solution.ipynb     # Main Jupyter Notebook
├── social_network_ads.csv        # Dataset
├── requirements.txt              # Python dependencies
└── README.md
```
 
---
 
## 📊 Dataset
 
The dataset contains **5 columns** with demographic and behavioral data:
 
| Column | Description |
|---|---|
| `user_id` | Unique identifier for each user |
| `gender` | Gender of the user (Male / Female) |
| `age` | Age of the user |
| `estimated_salary` | Estimated annual salary of the user |
| `purchased` | Target variable — 1 (Purchased) or 0 (Not Purchased) |
 
**Dataset Credits:** [Akram on Kaggle](https://www.kaggle.com/datasets/akram24/social-network-ads)
 
---
 
## 🔧 Tasks Covered
 
### Task 1 — Data Exploration
- Loaded dataset from `.csv`
- Checked shape, first few rows, and missing values
- Visualized `age` vs `estimated_salary` scatter plot colored by purchase status
### Task 2 — Model Training
- Encoded `gender` column: Male → 0, Female → 1
- Selected features: `age`, `estimated_salary`, `gender`
- Train/test split: **70% train / 30% test** (`random_state=42`)
- Trained default Logistic Regression model
- Printed model coefficients and intercept
### Task 3 — Model Evaluation
- Made predictions on the test set
- Evaluated using full classification report (precision, recall, F1-score, accuracy)
---
 
## 📈 Results
 
| Metric | Score |
|---|---|
| Model | Logistic Regression (default) |
| Features used | age, estimated_salary, gender |
| Test size | 30% |
| Evaluation | Classification Report (Precision, Recall, F1) |
 
---
 
## 🚀 How to Run
 
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/social-network-ads-classification.git
   cd social-network-ads-classification
   ```
 
2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
 
3. **Launch the notebook**
   ```bash
   jupyter notebook assignment_solution.ipynb
   ```
 
---
 
## 🛠️ Tech Stack
 
- Python 3.x
- pandas
- scikit-learn
- matplotlib
---
 
## 📄 License
 
This project is for educational purposes. Dataset sourced from Kaggle under public usage — see dataset credits above.
