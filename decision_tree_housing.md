# 🏡 Boston Housing Price Prediction Using Decision Tree

## 📌 Overview
This project uses a Decision Tree Regression model to predict housing prices in Boston using various features such as crime rate, number of rooms, accessibility to highways, and more. The dataset is cleaned, visualized, and optimized with hyperparameter tuning using GridSearchCV.

## 📊 Dataset
- **Source**: `HousingData.csv`
- **Target Variable**: `MEDV` (Median value of owner-occupied homes in $1000s)
- **Features**: 13 numerical features including CRIM, ZN, INDUS, CHAS, NOX, RM, AGE, etc.

## ❓ Problem Statement
Predict the house prices based on features like number of rooms, accessibility, pollution index, etc. This can help stakeholders in real estate make informed decisions.

## 🔄 Data Preprocessing
- Handled missing values using **median imputation**
- Applied **outlier capping** using the 1st and 99th percentiles for columns with high variance
- Split data into training and testing sets (80/20)

## 📈 Modeling
- **Model Used**: DecisionTreeRegressor
- **Baseline Model Parameters**: `max_depth=4`
- **Hyperparameter Tuning**: Used GridSearchCV with 5-fold cross-validation

## ⚙️ Best Hyperparameters (from GridSearchCV)
```python
{
  'ccp_alpha': 0.0,
  'max_depth': 5,
  'min_samples_leaf': 6,
  'min_samples_split': 2
}
```

## 📈 Modeling Results
| Model              | R² Score | MAE   | MSE   |
|--------------------|----------|-------|--------|
| **Baseline** (`max_depth=4`) | **0.83** | **2.77** | **12.35** |
| **Tuned (GridSearchCV)**     | **0.75** | **2.78** | **18.17** |

- ✅ **Best R² in Cross-Validation**: 0.7202
- 🔍 **Observation**: The baseline model slightly outperforms the tuned one on test data.

## 📊 Visualizations
- Boxplots and Violin plots to identify outliers
- Heatmap to study correlations
- Pairplots and Regression plots for important features
- Residual plot to assess model errors

## 🛠 Tools & Libraries Used
- Python, Pandas, NumPy
- Scikit-learn (modeling & preprocessing)
- Seaborn, Matplotlib (visualization)

## 📁 Structure
```
👉 HousingData.csv
👉 DecisionTree_Housing_Model.ipynb
👉 README.md
```

## 🚀 How to Run
1. Clone the repository
2. Install requirements with `pip install -r requirements.txt`
3. Run the notebook or Python script

## 🧐 Author
**Ahmed Osama**  
Data Science & AI Enthusiast

---
> This project is part of my data science learning journey. Feel free to fork, explore, and connect!

