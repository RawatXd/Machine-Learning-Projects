# 🫘 Dry Bean Multiclass Classification
 
A machine learning project that applies **Logistic Regression** to classify dry beans into seven distinct varieties using geometric and shape-based features extracted from computer vision data.
 
---
 
## 📌 Problem Statement
 
Given a set of visual and geometric measurements of dry beans (area, perimeter, shape factors, etc.), the goal is to train a classification model that accurately predicts the bean variety. This is a **multiclass classification** problem with **7 target classes**.
 
---
 
## 📂 Project Structure
 
```
dry-bean-classification/
├── assignment.ipynb          # Main Jupyter Notebook
├── dry_bean_dataset.xlsx     # Dataset
├── requirements.txt          # Python dependencies
└── README.md
```
 
---
 
## 📊 Dataset
 
The dataset contains **17 features** extracted from images of dry beans:
 
| Feature | Description |
|---|---|
| `area` | Number of pixels within bean boundaries |
| `perimeter` | Length of the bean's border |
| `majorAxisLength` | Length of the longest axis |
| `minorAxisLength` | Length of the perpendicular axis |
| `aspectRatio` | Ratio of major to minor axis length |
| `eccentricity` | Eccentricity of the equivalent ellipse |
| `convexArea` | Pixels in the smallest convex polygon around the bean |
| `equivDiameter` | Diameter of a circle with the same area |
| `extent` | Ratio of bean pixels to bounding box pixels |
| `solidity` | Ratio of bean pixels to convex hull pixels |
| `roundness` | `(4 × π × Area) / Perimeter²` |
| `compactness` | `EquivalentDiameter / MajorAxisLength` |
| `shapeFactor1–4` | Additional shape descriptors |
| `class` | Target variable (7 bean varieties) |
 
**Target Classes:** `SEKER`, `BARBUNYA`, `BOMBAY`, `CALI`, `DERMASON`, `HOROZ`, `SIRA`
 
### Citation
> KOKLU, M. and OZKAN, I.A. (2020). *Multiclass Classification of Dry Beans Using Computer Vision and Machine Learning Techniques.* Computers and Electronics in Agriculture, 174, 105507.
> DOI: [10.1016/j.compag.2020.105507](https://doi.org/10.1016/j.compag.2020.105507)
> Dataset: [muratkoklu.com/datasets](https://www.muratkoklu.com/datasets/)
 
---
 
## 🔧 Tasks Covered
 
### Task 1 — Data Exploration
- Loaded dataset from `.xlsx`
- Checked shape, head, and missing values
- Visualized class distribution
- Scatter plots of key features using `seaborn.pairplot`
### Task 2 — Data Preprocessing
- Separated features (`X`) and target (`y`)
- Train/test split: **70% train / 30% test** (`random_state=42`)
### Task 3 — Default Logistic Regression
- Trained with default `sklearn` parameters
- Evaluated with classification report and confusion matrix heatmap
### Task 4 — Tuned Logistic Regression
- Trained with custom parameters:
  ```python
  LogisticRegression(max_iter=300, C=0.5, tol=0.001, class_weight='balanced')
  ```
- Compared performance against the default model
---
 
## 📈 Results
 
| Model | Accuracy |
|---|---|
| Default Logistic Regression | 71% |
| Tuned Logistic Regression | **76%** |
 
Tuning with `class_weight='balanced'` and adjusted regularization (`C=0.5`) improved precision, recall, and F1-score across most bean classes.
 
---
 
## 🚀 How to Run
 
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/dry-bean-classification.git
   cd dry-bean-classification
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
- matplotlib, seaborn
- openpyxl (for `.xlsx` reading)
---
 
## 📄 License
 
This project is for educational purposes. Dataset used under academic citation guidelines — see citation above.
 
