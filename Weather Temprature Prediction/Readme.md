## 🌤️ Weather Temperature Prediction — Linear Regression
 
A machine learning project that applies **Linear Regression** to predict daily temperature based on sunlight hours and humidity level using a meteorological dataset.
 
---
 
## 📌 Problem Statement
 
Given daily weather measurements — hours of sunlight and humidity level — the goal is to build a regression model that accurately **predicts the daily temperature** in degrees Celsius. This covers both single-variable and multi-variable linear regression approaches.
 
---
 
## 📂 Project Structure
 
```
weather-temperature-prediction/
├── assignment.ipynb          # Main Jupyter Notebook
├── weather_data.csv          # Dataset
├── requirements.txt          # Python dependencies
└── README.md
```
 
---
 
## 📊 Dataset
 
The dataset contains **3 columns** of daily weather records:
 
| Column | Description |
|---|---|
| `hours_sunlight` | Total hours of sunlight received in a day |
| `humidity_level` | Humidity level as a percentage (%) |
| `daily_temperature` | Target variable — temperature recorded at end of day (°C) |
 
---
 
## 🔧 Tasks Covered
 
### Task 1 — Single Variable Linear Regression
- Loaded dataset from `.csv` and explored shape and first few rows
- Trained a Linear Regression model using only `hours_sunlight` to predict `daily_temperature`
- Printed model coefficient and intercept
- Predicted temperature for:
  - 5 hours of sunlight
  - 8 hours of sunlight
  - 12 hours of sunlight
### Task 2 — Multiple Variable Linear Regression
- Trained a Linear Regression model using both `hours_sunlight` and `humidity_level`
- Printed model coefficients and intercept
- Predicted temperature for 3 real-world conditions:
| Hours of Sunlight | Humidity Level | Predicted Temp |
|---|---|---|
| 5 hrs | 60% | Model output |
| 8 hrs | 75% | Model output |
| 12 hrs | 50% | Model output |
 
---
 
## 📈 Key Concepts Demonstrated
 
- **Simple Linear Regression** — one input feature → one output
- **Multiple Linear Regression** — two input features → one output
- Model coefficients interpretation (effect of sunlight & humidity on temperature)
- Prediction on custom unseen inputs
---
 
## 🚀 How to Run
 
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/weather-temperature-prediction.git
   cd weather-temperature-prediction
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
- pandas
- scikit-learn
---
 
## 📄 License
 
This project is for educational purposes only.
 
