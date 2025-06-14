# 🏁 MotoGP Lap Time Prediction with XGBoost

📌 **[👉 Run this notebook on Google Colab](https://colab.research.google.com/drive/1rLMN4X6FyOpQV72AK5zY8aH-UD62sgX4?usp=sharing)**

This repository contains my solution for the MotoGP Lap Time Prediction task, where I developed and tested machine learning models to accurately predict riders' lap times using race and rider features.

---

## 📌 Project Objective

> Predict `Lap_Time_Seconds` using race conditions, bike configuration, rider history, and environmental data.

---

## 🛠️ Workflow Summary

✅ **Data Import & Cleaning**
- Loaded datasets (`train`, `test`)
- Handled missing values (e.g., filled `Penalty` column)

✅ **Feature Engineering**
- Created binary flags for penalties
- Mapped tire compounds to numeric
- Mapped weather and track conditions
- Computed aggregate features: `Total_Pit_Time`, `Temperature_Gradient`, `Tire_Wear_Score`
- Target encoding for `bike_name` and `team_name`

✅ **Exploratory Data Analysis**
- Univariate and bivariate analysis (visualizations)
- Correlation heatmap
- Residual analysis to check model fit

✅ **Modeling**
- Trained and evaluated  XGBoost
- Selected XGBoost as final model
- Performed cross-validation (RMSE ~4.89)
- Feature importance analysis
- Generated predictions for submission

---

## ⚙️ Technologies Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost

---

## 📈 Results

- Final XGBoost RMSE: **4.79**
- CV RMSE: **4.89**
- Residuals: Symmetric distribution, minimal bias
- Public leaderboard score: **~4.79**

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/your-username/motogp-lap-time-prediction.git
cd motogp-lap-time-prediction

# (Optional) Create virtual environment
python -m venv venv
source venv/bin/activate  # For Linux/Mac
venv\Scripts\activate     # For Windows

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook MotoGP_Lap_Time_Prediction.ipynb
