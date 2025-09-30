# 🏥 Insurance Charges Prediction  

This project predicts **insurance charges** for individuals based on demographic, lifestyle, and medical factors.  
It uses **Machine Learning regression models** and compares multiple algorithms to find the best-performing one.  

---

## 📌 Project Workflow  

1. **Data Source**  
   - Data is stored in **SQLite Database** (`Database.db`)  
   - Table used: `Insurance_Prediction`

2. **Data Preprocessing**  
   - Missing value treatment (mean, mode imputation)  
   - Outlier detection & treatment using **IQR method**  
   - Feature encoding:  
     - **Nominal features** → One-Hot Encoding  
     - **Ordinal features** (`exercise_frequency`, `coverage_level`) → Manual mapping  
   - Feature scaling using **MinMaxScaler**  

3. **Feature Selection**  
   - Correlation filter  
   - Lasso Regression (L1 regularization)  
   - Random Forest feature importance  

4. **Model Training**  
   Trained and evaluated the following models:  
   - Linear Regression  
   - Decision Tree Regressor  
   - Random Forest Regressor  
   - Gradient Boosting Regressor  
   - K-Nearest Neighbors Regressor  

5. **Model Evaluation Metrics**  
   - Mean Absolute Error (MAE)  
   - Mean Squared Error (MSE)  
   - Root Mean Squared Error (RMSE)  

6. **Validation**  
   - Validation dataset: rows `700,000 - 900,000` from original dataset  
   - Best model selected based on **lowest RMSE**  

7. **Model Saving**  
   - Final best model + preprocessing details saved with **joblib**  
   - File: `best_Insurance_Prediction_model.joblib`  
   - Saved components:  
     - Trained model  
     - Scaler  
     - Selected features list  

---

## ⚙️ Tech Stack  

- **Language**: Python  
- **Database**: SQLite  
- **Libraries**:  
  - Data Handling → Pandas, NumPy, SQLite3  
  - Visualization → Matplotlib, Seaborn  
  - ML Models → Scikit-learn  
  - Model Saving → Joblib  

---

## 📊 Results  

- Compared 5 ML models on validation dataset.  
- ✅ **Best Model:** *Displayed in console after execution* with **lowest RMSE score**.  

---
