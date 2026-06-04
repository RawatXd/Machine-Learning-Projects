# 🍄 Mushroom Classification — Binary Classification Assignment

A machine learning project that builds and evaluates multiple classification models to predict whether a mushroom is **edible (0)** or **poisonous (1)**, using the [Mushroom Dataset](https://www.kaggle.com/datasets/prishasawhney/mushroom-dataset/data) by Prisha Sawhney.

---

## 📁 Project Structure

```
├── assignment_solution.ipynb   # Main Jupyter notebook with full solution
├── mushroom_classification.csv # Dataset file
└── README.md
```

---

## 📊 Dataset

**File:** `mushroom_classification.csv`

| Feature | Description |
|---|---|
| `cap_diameter` | Diameter of the mushroom cap |
| `cap_shape` | Shape of the mushroom cap (integer-encoded) |
| `gill_attachment` | Attachment of the gills (integer-encoded) |
| `gill_color` | Color of the gills (integer-encoded) |
| `stem_height` | Height of the mushroom stem |
| `stem_width` | Width of the mushroom stem |
| `stem_color` | Color of the mushroom stem (integer-encoded) |
| `season` | Season when mushroom was found (integer-encoded) |
| `class` | **Target** — `0` = Edible, `1` = Poisonous |

---

## 🛠️ Requirements

Install dependencies with:

```bash
pip install pandas matplotlib scikit-learn
```

| Library | Purpose |
|---|---|
| `pandas` | Data loading & manipulation |
| `matplotlib` | Visualization (box plots, bar charts) |
| `scikit-learn` | Model training & evaluation |

---

## 🚀 How to Run

1. Clone or download this repository.
2. Ensure `mushroom_classification.csv` is in the same directory as the notebook.
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook assignment_solution.ipynb
   ```
4. Run all cells sequentially (`Kernel → Restart & Run All`).

---

## 📋 Tasks Overview

### Task 1 — Data Preparation & Exploration
- Load the CSV into a DataFrame
- Display shape and first few rows

### Task 2 — Exploratory Data Analysis (EDA)
- Group-by on target class to compute mean of `cap_diameter`, `stem_height`, `stem_width`
- Visualize feature distributions using **box plots**

### Task 3 — Basic Model Training
- Train/test split: **75% train / 25% test** (`random_state=10`)
- Train and evaluate:
  - **Logistic Regression**
  - **Decision Tree Classifier**
- Print classification reports for both

### Task 4 — Gradient Boosting Classifier
- Train with default parameters
- Display **feature importances** via horizontal bar chart

### Task 5 — Hyperparameter Tuning
- Re-train Gradient Boosting with custom parameters:
  ```python
  learning_rate=0.05, n_estimators=150,
  max_depth=4, min_samples_split=3, min_samples_leaf=2
  ```

---

## 📈 Results Summary

| Model | Accuracy |
|---|---|
| Logistic Regression | 0.62 |
| Decision Tree Classifier | **0.98** |
| Gradient Boosting (default) | 0.88 |
| Gradient Boosting (custom params) | 0.90 |
