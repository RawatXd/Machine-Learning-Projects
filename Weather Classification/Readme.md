# Weather Type Classification using SVM
 
A machine learning project that predicts weather type (Rainy, Sunny, Cloudy, Snowy) from meteorological features using Support Vector Machine (SVM) classifiers.
 
---
 
## Dataset
 
**Source:** [Weather Type Classification – Kaggle (Nikhil Narayan)](https://www.kaggle.com/datasets/nikhil7280/weather-type-classification)  
**File:** `weather_classification_data.csv`  
**Size:** 13,200 rows × 11 columns
 
| Feature | Type | Description |
|---|---|---|
| `temperature` | int | Temperature in °C |
| `humidity` | int | Humidity percentage |
| `wind_speed` | float | Wind speed in km/h |
| `precipitation (%)` | int | Precipitation percentage |
| `cloud_cover` | str | Cloud cover description |
| `atmospheric_pressure` | float | Atmospheric pressure in hPa |
| `uv_index` | int | UV index |
| `season` | str | Season of recording |
| `visibility (km)` | float | Visibility in kilometres |
| `location` | str | Type of location |
| `weather_type` | str | **Target** — Rainy / Sunny / Cloudy / Snowy |
 
---
 
## Project Structure
 
```
weather_classification_data.csv   # Dataset
weather_classification.ipynb      # Main notebook
README.md
```
 
---
 
## Requirements
 
```bash
pip install pandas scikit-learn seaborn matplotlib
```
 
Python 3.8+ recommended.
 
---
 
## Workflow
 
The notebook is organised into six tasks:
 
### Task 1 — Data Preparation & Exploration
- Load the CSV into a pandas DataFrame
- Check shape, missing values, and data types
- Visualise key features:
  - `season` → pie chart
  - `temperature`, `humidity`, `wind_speed` → histograms
  - `precipitation (%)` → box plot
### Task 2 — Data Transformation
- **One-hot encode** categorical columns: `cloud_cover`, `location`, `season`
- **StandardScaler** applied to all seven numerical features
### Task 3 — SVM with Linear Kernel
- 70/30 train-test split (`random_state=42`)
- Train `SVC(kernel='linear')`
- Evaluate with accuracy score, classification report, and confusion matrix
### Task 4 — SVM with RBF Kernel
- Train `SVC(kernel='rbf')` on the same split
- Compare accuracy and evaluation metrics against the linear kernel
### Task 5 — Hyperparameter Experimentation
- Train a custom RBF SVM with `C=0.5`, `gamma='auto'`, `degree=2`
- Observe the effect on accuracy and per-class metrics
### Task 6 — Sklearn Pipeline
- Build a `Pipeline([StandardScaler → SVC(rbf)])`
- Fits and evaluates end-to-end in a single object — clean, reproducible, and leak-proof
---
 
## How to Run
 
```bash
jupyter notebook weather_classification.ipynb
```
 
Run all cells in order. Each task section is self-contained with inline comments.
 
---
 
## Key Concepts
 
- **SVM (Support Vector Machine):** Finds the optimal hyperplane that maximises the margin between classes.
- **Linear kernel:** Works well when classes are linearly separable.
- **RBF kernel:** Maps data to a higher-dimensional space; handles non-linear boundaries.
- **Pipeline:** Chains preprocessing and modelling into one estimator, preventing data leakage during cross-validation.
---
 
## References
 
- [sklearn.svm.SVC documentation](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html)
- [Kaggle Dataset](https://www.kaggle.com/datasets/nikhil7280/weather-type-classification)
