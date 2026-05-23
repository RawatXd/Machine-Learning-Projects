# 📚 Student Score Prediction — Polynomial Regression
 
A machine learning project that applies **Polynomial Regression** to predict student exam scores based on the number of hours studied.
 
---
 
## 📌 Problem Statement
 
Given records of how many hours students studied and the marks they obtained, the goal is to build a regression model that accurately **predicts a student's score** from their study hours. This project uses **Polynomial Regression (degree 3)** to capture the non-linear relationship between study time and performance.
 
---
 
## 📂 Project Structure
 
```
student-score-prediction/
├── assignment.ipynb          # Main Jupyter Notebook
├── student_scores.csv        # Dataset
├── requirements.txt          # Python dependencies
└── README.md
```
 
---
 
## 📊 Dataset
 
The dataset contains **2 columns** of student study records:
 
| Column | Description |
|---|---|
| `hours` | Number of hours the student studied |
| `scores` | Marks obtained by the student (target variable) |
 
---
 
## 🔧 Tasks Covered
 
### Task 1 — Data Exploration
- Loaded dataset from `.csv`
- Checked shape and first few rows
- Visualized the relationship between `hours` and `scores` using a scatter plot
### Task 2 — Polynomial Regression Model Training
- Selected feature (`hours`) and target (`scores`)
- Train/test split: **75% train / 25% test** (`random_state=5`)
- Applied `PolynomialFeatures(degree=3)` to transform features
- Fitted a `LinearRegression` model on the transformed training data
- Printed model coefficients and intercept
### Task 3 — Model Evaluation
- Made predictions on the transformed test set
- Evaluated using:
  - **Mean Squared Error (MSE)**
  - **R-squared (R²)**
---
 
## 📈 Key Concepts Demonstrated
 
- **Polynomial Regression** — capturing non-linear patterns using degree-3 feature transformation
- `PolynomialFeatures` from scikit-learn — expanding input features into polynomial terms
- Model evaluation using **MSE** and **R²** metrics
- Difference between linear and polynomial fit for real-world data
---
 
## 🚀 How to Run
 
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/student-score-prediction.git
   cd student-score-prediction
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
