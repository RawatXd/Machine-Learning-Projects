🫘 Dry Bean Multiclass Classification
A machine learning project that applies Logistic Regression to classify dry beans into seven distinct varieties using geometric and shape-based features extracted from computer vision data.

📌 Problem Statement
Given a set of visual and geometric measurements of dry beans (area, perimeter, shape factors, etc.), the goal is to train a classification model that accurately predicts the bean variety. This is a multiclass classification problem with 7 target classes.

📂 Project Structure
dry-bean-classification/
├── assignment.ipynb          # Main Jupyter Notebook
├── dry_bean_dataset.xlsx     # Dataset
├── requirements.txt          # Python dependencies
└── README.md

📊 Dataset
The dataset contains 17 features extracted from images of dry beans:
FeatureDescriptionareaNumber of pixels within bean boundariesperimeterLength of the bean's bordermajorAxisLengthLength of the longest axisminorAxisLengthLength of the perpendicular axisaspectRatioRatio of major to minor axis lengtheccentricityEccentricity of the equivalent ellipseconvexAreaPixels in the smallest convex polygon around the beanequivDiameterDiameter of a circle with the same areaextentRatio of bean pixels to bounding box pixelssolidityRatio of bean pixels to convex hull pixelsroundness(4 × π × Area) / Perimeter²compactnessEquivalentDiameter / MajorAxisLengthshapeFactor1–4Additional shape descriptorsclassTarget variable (7 bean varieties)
Target Classes: SEKER, BARBUNYA, BOMBAY, CALI, DERMASON, HOROZ, SIRA
Citation

KOKLU, M. and OZKAN, I.A. (2020). Multiclass Classification of Dry Beans Using Computer Vision and Machine Learning Techniques. Computers and Electronics in Agriculture, 174, 105507.
DOI: 10.1016/j.compag.2020.105507
Dataset: muratkoklu.com/datasets


🔧 Tasks Covered
Task 1 — Data Exploration

Loaded dataset from .xlsx
Checked shape, head, and missing values
Visualized class distribution
Scatter plots of key features using seaborn.pairplot

Task 2 — Data Preprocessing

Separated features (X) and target (y)
Train/test split: 70% train / 30% test (random_state=42)

Task 3 — Default Logistic Regression

Trained with default sklearn parameters
Evaluated with classification report and confusion matrix heatmap

Task 4 — Tuned Logistic Regression

Trained with custom parameters:

python  LogisticRegression(max_iter=300, C=0.5, tol=0.001, class_weight='balanced')

Compared performance against the default model


📈 Results
ModelAccuracyDefault Logistic Regression71%Tuned Logistic Regression76%
Tuning with class_weight='balanced' and adjusted regularization (C=0.5) improved precision, recall, and F1-score across most bean classes.

🚀 How to Run

Clone the repository

bash   git clone https://github.com/your-username/dry-bean-classification.git
   cd dry-bean-classification

Install dependencies

bash   pip install -r requirements.txt

Launch the notebook

bash   jupyter notebook assignment.ipynb

🛠️ Tech Stack

Python 3.x
pandas, numpy
scikit-learn
matplotlib, seaborn
openpyxl (for .xlsx reading)
