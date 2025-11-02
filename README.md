# CO₂ Emission Prediction from Vehicle Specifications

This project aims to **predict CO₂ emissions** based on various **vehicle specifications** such as engine size, fuel type, and fuel consumption.  
By building and analyzing regression models, the goal is to identify which features have the greatest influence on CO₂ emissions.

---

## Overview
The automotive industry is under increasing pressure to reduce greenhouse gas emissions.  
Understanding which vehicle characteristics contribute most to CO₂ emissions can help manufacturers and policymakers make more sustainable decisions.

This project uses **Linear Regression and Regularized Regression Models (Ridge, Lasso, ElasticNet)** to predict CO₂ emissions based on data from **Kaggle**.

---

## Dataset
**Source:** [Vehicle CO₂ Emissions Dataset (Kaggle)](https://www.kaggle.com/datasets/brsahan/vehicle-co2-emissions-dataset)

| Variable | Description |
|-----------|-------------|
| `Make` | Manufacturer or brand of the vehicle |
| `Model` | Specific type of vehicle |
| `Vehicle Class` | Category of vehicle (SUV, Sedan, etc.) |
| `Engine Size (L)` | Engine displacement in liters |
| `Cylinders` | Number of engine cylinders |
| `Transmission` | Type of transmission system |
| `Fuel Type` | Type of fuel used (Gasoline, Diesel, etc.) |
| `Fuel Consumption (City/Hwy/Comb)` | Fuel usage in L/100 km |
| `CO2 Emissions (g/km)` | Target variable — CO₂ emitted per kilometer |

---

## Methods
1. **Data Preprocessing**
   - Handled missing values
   - Encoded categorical features
   - Scaled numerical features using `StandardScaler`
2. **Exploratory Data Analysis (EDA)**
   - Checked variable distributions
   - Correlation analysis to find relationships between engine specs and CO₂ emissions
   - Visualized feature relationships using scatter plots and heatmaps
3. **Modeling**
   - Linear Regression
   - Ridge, Lasso, and ElasticNet
4. **Evaluation**
   - Metrics used: R², MSE, RMSE
   - Compared model performance
5. **Feature Importance Analysis**
   - Identified which vehicle attributes have the highest influence on CO₂ emissions

---

## Results
| Model | R² Score | RMSE |
|--------|-----------|------|
| Linear Regression | 0.85 | 13.2 |
| Ridge Regression | 0.84 | 13.4 |
| Lasso Regression | 0.83 | 13.7 |
| ElasticNet | 0.83 | 13.5 |

> The analysis shows that **fuel type** and **fuel consumption features** are the most significant predictors of CO₂ emissions.  
> Meanwhile, features like **vehicle class** and **transmission** have relatively smaller impacts.

---

## Key Insights
- Vehicles with higher fuel consumption tend to emit more CO₂.
- Engine size and number of cylinders are positively correlated with emissions.
- Regularization slightly reduces overfitting but doesn’t significantly improve performance — suggesting a mostly linear relationship.

---

## Future Work
- Add **non-linear models** (Random Forest, XGBoost) for better accuracy.
- Perform **cross-validation** for more reliable performance metrics.
- Use **SHAP or Permutation Importance** for deeper interpretability.
- Deploy the model as a simple web app using Streamlit.

---

## Tech Stack
- **Python**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **Scikit-learn**
- **Google Colab**

---

