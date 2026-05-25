# 🚢 Titanic Survival Prediction
 
A binary classification project that predicts whether a Titanic passenger survived, using a **Gaussian Naive Bayes** model built with scikit-learn.
 
---
 
## 📁 Project Files
 
| File | Description |
|---|---|
| `titanic.csv` | Raw dataset with passenger information |
| `assignment.ipynb` | Jupyter Notebook with full analysis and model |
 
---
 
## 📊 Dataset
 
The dataset (`titanic.csv`) contains **12 columns** describing each passenger:
 
| Column | Description |
|---|---|
| `passenger_id` | Unique identifier for each passenger |
| `name` | Full name of the passenger |
| `p_class` | Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd) |
| `sex` | Gender of the passenger |
| `age` | Age of the passenger |
| `sib_sp` | Number of siblings/spouses aboard |
| `parch` | Number of parents/children aboard |
| `ticket` | Ticket number |
| `fare` | Ticket fare paid |
| `cabin` | Cabin number |
| `embarked` | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |
| `survived` | Target variable — 1 = Survived, 0 = Did not survive |
 
---
 
## 🔧 Requirements
 
Install all dependencies using pip:
 
```bash
pip install pandas matplotlib seaborn scikit-learn notebook
```
 
---
 
## 🚀 How to Run
 
1. **Clone or download** this repository.
2. Place `titanic.csv` in the **same directory** as `assignment.ipynb`.
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook assignment.ipynb
   ```
4. Run all cells sequentially (`Kernel → Restart & Run All`).
---
 
## 🗂️ Notebook Structure
 
### Task 1 — Data Preparation & Exploration
- Load dataset into a DataFrame
- Display shape, head, and missing values
- Drop low-value columns: `passenger_id`, `name`, `sib_sp`, `parch`, `ticket`, `cabin`, `embarked`
- Bar charts for `survived` and `p_class` distributions
- Pie chart for `sex` distribution
- Histograms for `age` and `fare` distributions
### Task 2 — Data Preprocessing
- Fill missing values in `age` and `fare` with their **median**
- One-hot encode the `sex` column
- Standardize `fare` using `StandardScaler`
- Select features: `p_class`, `sex`, `age`, `fare`
- Split data: **70% training / 30% testing**
### Task 3 — Model Training & Evaluation
- Train a **Gaussian Naive Bayes** classifier
- Predict on the test set
- Print the **classification report** (precision, recall, F1-score)
- Visualize the **confusion matrix** using a heatmap
---
 
## 📈 Model
 
| Detail | Value |
|---|---|
| Algorithm | Gaussian Naive Bayes |
| Library | `sklearn.naive_bayes.GaussianNB` |
| Features used | `p_class`, `sex_male`, `sex_female`, `age`, `fare` |
| Target | `survived` (0 or 1) |
| Test size | 30% |
 
---
 
## 📦 Libraries Used
 
```python
import pandas as pd
from matplotlib import pyplot as plt
import seaborn as sns
from sklearn.preprocessing import StandardScaler
from sklearn.naive_bayes import GaussianNB
from sklearn.model_selection import train_test_split
from sklearn.metrics import classification_report, confusion_matrix
```
 
---
 
## 📝 Notes
 
- The `cabin` column has a high rate of missing values and is dropped during preprocessing.
- One-hot encoding of `sex` produces two binary columns (`sex_male`, `sex_female`).
- `StandardScaler` is applied only to the `fare` column to normalize its range.
 
