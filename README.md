# Diamond Price Prediction with XGBoost

Predicting diamond prices using the Kaggle Diamonds dataset with **XGBoost regression**.  
The notebook demonstrates preprocessing, feature engineering, model training, evaluation, and interpretability using SHAP.



## Dataset
- Diamonds dataset (~50,000 rows, CSV included in `diamonds.csv`)  
- Features include: `carat`, `cut`, `color`, `clarity`, `depth`, `table`, `x`, `y`, `z`  
- Target variable: `price`



## Key Steps
1. **Preprocessing:**  
   - Categorical variables encoded using one-hot encoding  
   - Created a new feature `Volume = x * y * z`  
   - Applied log transformation to `price` to reduce skewness  

2. **Model Training & Evaluation:**  
   - XGBoost Regressor trained on the training set  
   - Evaluated using R² score, MSE, and 5-fold cross-validation  
   - Achieved R² ~0.992 after log-transforming the target  

3. **Model Explainability:**  
   - SHAP summary plot to show global feature importance  
   - SHAP waterfall plot for local prediction explanations  
   - Key features: `Carat`, `y`, `Clarity`



## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/Reyhane-Ha/diamond-price-prediction.git
2. Install dependencies:
- pip install -r requirements.txt
3. Open diamonds.ipynb in Jupyter Notebook or VS code and run the cells sequentially.
