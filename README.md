# ☀️ SolarSense: Solar Power Generation Forecasting Using Machine Learning

## 📌 Project Overview
**SolarSense** is a machine learning project aimed at forecasting solar power generation using atmospheric and solar position data. With the growing importance of renewable energy, accurately predicting power output from solar panels can help optimize grid management, energy storage, and sustainability planning.

This project leverages **regression algorithms** to model and predict solar output in kilowatts (kW) based on various features such as temperature, cloud cover, humidity, and solar angles (azimuth, zenith, etc.).

---

## 🔍 Problem Statement
Can we accurately predict the amount of solar energy generated using weather and positional data?  
This prediction task is treated as a **supervised regression problem**, where the target is `generated_power_kw`.

---

## 🧠 Skills Demonstrated
- Regression Modeling
- Ensemble Learning: XGBoost & Random Forest
- Hyperparameter Tuning (GridSearchCV & RandomizedSearchCV)
- Feature Engineering & Selection
- Model Evaluation (R², RMSE, Relative RMSE)
- Data Visualization

---

## 📁 Dataset Overview
The dataset includes:
- Meteorological features (e.g. temperature, humidity, pressure, precipitation)
- Solar irradiance & cloud cover at multiple layers
- Wind metrics at different altitudes
- Solar angle measurements (azimuth, zenith, angle of incidence)
- **Target**: `generated_power_kw`

> Total Records: 4,213  
> Missing Values: None  
> Format: CSV  

---

## 🔧 Tools & Technologies
- **Python**
- **Pandas**, **NumPy** – data handling
- **Matplotlib**, **Seaborn** – visualizations
- **Scikit-learn** – modeling and evaluation
- **XGBoost** – gradient boosting regression
- **GridSearchCV**, **RandomizedSearchCV** – hyperparameter tuning

---

## 📈 Models & Performance

| Model                 | R² Score | Relative RMSE |
|----------------------|----------|----------------|
| XGBoost (GridSearch) | **0.83** | **0.34**       |
| XGBoost (Randomized) | 0.82     | 0.35           |
| Random Forest (Base) | 0.82     | 0.36           |

🔹 **Best Model**: XGBoost with GridSearch – showing the best balance of accuracy and error.

---

## 🧪 Feature Engineering
- Solar angles: `azimuth`, `zenith`, `angle_of_incidence`
- Categorized cloud cover: low, mid, high, total
- Combined directional wind features
- Removed low-variance and highly correlated features

---

## 📊 Visualizations
- Scatter plot: `angle_of_incidence` vs. `generated_power_kw`
- Barcharts: Cloud cover vs. average power generated
- Double barchart: Comparing R² and RMSE scores across models

---

## 💡 Key Takeaways
- Weather and solar angles are strong predictors of solar energy output.
- Hyperparameter tuning (especially GridSearch) significantly improves model performance.
- Ensemble methods like XGBoost and Random Forest work well for this task.

---

## 🚀 Future Work
- Integrate SHAP for model explainability
- Test models on real-time solar datasets
- Deploy with a cloud service (Azure ML / AWS Sagemaker)
- Build a dashboard for live prediction and monitoring

---

## 📂 How to Run

```bash
# Clone the repo
git clone https://github.com/yourusername/SolarSense.git
cd SolarSense

# Install dependencies
pip install -r requirements.txt

# Run the notebook or Python scripts
