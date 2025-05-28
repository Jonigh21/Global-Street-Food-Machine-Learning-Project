# Global Street Food ML Project

## Project Overview
This project uses machine learning to predict the price of global street food dishes based on features like location, cooking method, ingredients, and dietary options. The goal is to uncover pricing patterns across countries and cuisines using real-world data and practical modeling techniques.

---

## Objective
To build a model that accurately predicts the typical price (USD) of a street food dish, helping explore how regional and preparation characteristics influence cost.

---

## Tools and Skills Used
- Python (Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib)
- Data Cleaning & Feature Engineering
- One-Hot Encoding & Standardization
- Linear Regression & Random Forest Regressor
- Hyperparameter Tuning with GridSearchCV
- RMSE and Residual Analysis
- Data Visualization and Reporting

---

## Workflow Summary

### 1. Exploratory Data Analysis (EDA)
- Reviewed value counts and distributions
- Removed 1,288 duplicate rows
- Identified top countries, cooking methods, and common price ranges

### 2. Preprocessing
- One-hot encoded categorical variables
- Scaled numeric features such as ingredient count
- Converted 'Vegetarian' column to binary
- Engineered new features:
  - Combined Country and Region into one Location feature
  - Parsed and counted ingredients

### 3. Modeling
- Built a Linear Regression pipeline
- Switched to Random Forest Regressor to model non-linear relationships
- RMSE settled at approximately 1.45

### 4. Hyperparameter Tuning
- Used GridSearchCV to tune the Random Forest model
- Best parameters did not significantly reduce RMSE, indicating a performance plateau

### 5. Visualization and Reporting
- Analyzed average price by country and cooking method
- Compared actual vs. predicted prices
- Evaluated residuals to assess model fit

---

## Key Takeaways
Despite tuning and feature engineering, the model’s RMSE remained steady at around 1.45. This suggests:
- Original categorical features already captured most of the predictive signal
- Added features were either redundant or weakly correlated with price
- The price variable may have inherent noise or missing context (e.g., portion size, vendor info)

---

## Final Model Performance
- Model: Random Forest Regressor
- Evaluation Metric: Root Mean Squared Error (RMSE)
- Final RMSE: 1.45

---

## Example Visualizations

**Average Price by Country:**  
Helps confirm country is a meaningful predictor of price. Countries like Japan and Turkey showed higher average street food costs.

**Average Price by Cooking Method:**  
Pan-fried dishes were the most expensive, while assembled and stir-fried were generally lower cost.

**Actual vs. Predicted Scatter Plot:**  
Shows model predictions hover around the average price. Good for visualizing accuracy and identifying underfitting.

**Residual Histogram:**  
Indicates prediction errors are somewhat centered but may lack symmetry, pointing to further room for improvement.

---

## Future Directions
- Add richer data: portion sizes, vendor types, or popularity scores
- Explore advanced models like XGBoost or LightGBM
- Deploy an interactive dashboard or web app for public insights

---

## Author
**Jonigh McGee**  
M.S. in Data Science  
