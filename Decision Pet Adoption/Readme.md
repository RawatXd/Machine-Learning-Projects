# Pet Adoption Likelihood Prediction

A binary classification project that predicts whether a pet is likely to be adopted, using Decision Tree models built with scikit-learn.

Dataset credits: [Rabie El Kharoua](https://www.kaggle.com/datasets/rabieelkharoua/predict-pet-adoption-status-dataset)

---

## Dataset

The dataset (`pet_adoption_data.csv`) contains 2007 rows and 13 columns:

| Column | Description |
|--------|-------------|
| `pet_id` | Unique identifier for each pet |
| `pet_type` | Type of pet (Dog, Cat, Bird, Rabbit) |
| `breed` | Specific breed of the pet |
| `age_months` | Age of the pet in months |
| `color` | Color of the pet |
| `size` | Size category (Small, Medium, Large) |
| `weight_kg` | Weight of the pet in kilograms |
| `vaccinated` | Vaccination status (0 = No, 1 = Yes) |
| `health_condition` | Health condition (0 = Healthy, 1 = Medical condition) |
| `timein_shelter_days` | Number of days spent in the shelter |
| `adoption_fee` | Adoption fee in dollars |
| `previous_owner` | Whether the pet had a previous owner (0 = No, 1 = Yes) |
| `adoption_likelihood` | Target variable (0 = Unlikely, 1 = Likely) |

---

## Project Structure

```
├── pet_adoption_data.csv
└── decision_pet_adoption.ipynb
```

---

## Notebook Structure

### Task 1 — Data Preparation and Exploration
- Load dataset and display shape and first few rows
- Drop the `pet_id` column
- Bar chart for `adoption_likelihood` distribution
- Histograms for `age_months` and `adoption_fee`

### Task 2 — Data Encoding and Scaling
- Ordinal encoding for `size` (Small=1, Medium=2, Large=3)
- One-hot encoding for `color`, `pet_type`, and `breed`
- MinMax scaling for `weight_kg`
- Standard scaling for `adoption_fee`

### Task 3 — Model Training and Evaluation
- Train a default Decision Tree Classifier (accuracy: 0.86)
- Train a tuned Decision Tree Classifier with custom hyperparameters (accuracy: 0.91)
- Classification report and confusion matrix for both models
- Decision tree text visualization using `export_text`

---

## Results

| Model | Accuracy |
|-------|----------|
| Decision Tree (Default) | 0.86 |
| Decision Tree (Tuned) | 0.91 |

Tuning hyperparameters improved precision, recall, and F1-score for the "Likely" adoption class.

---

## Requirements

```bash
pip install pandas scikit-learn matplotlib seaborn notebook
```

---

## How to Run

1. Place `pet_adoption_data.csv` in the same directory as the notebook.
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook decision_pet_adoption.ipynb
   ```
3. Run all cells sequentially.
