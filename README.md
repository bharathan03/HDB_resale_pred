# HDB_resale_pred
This machine learning project aims to predict resale prices of HDB using a Supervised Learning technique (Regression).

Dataset link: https://data.gov.sg/collections/189/view

1. This project consists of 5 stages 
    1. Background Research and Data Exploration
    - Merging and cleaning multiple csv's from the different years
    - Conducted Exploratory Data Analysis (EDA) on features such as floor_area, remaining_lease etc 
    2. Feature Engineering
    - Transforming date columns
    - Standardizing duplicate values in columns 
    3. Model Pipeline
    - Build preprocessing pipelines using ColumnTransformer and Pipeline
    - Usage of multiple regression models: Linear Regression, Ridge, Lasso, Bayesian Ridge, Decision Tree
    4. Model Improvement
    - Use GridSearchCV and cross-validation to tune hyperparameters
    - Addition of new models (RandomForest, XBGoost)
    5. Other Tests for Possible Improvements
    - Log transforming testing
  
2. Models used:
   - Linear Regression
   - Ridge & Lasso Regression
   - Bayesian Ridge
   - Decision Tree Regressor
   - Random Forest Regressor
   - XGBoost Regressor

3. All the models were evaluated and compares based on the following metrics: 
   - **MSE** (Mean Squared Error) - Penalizes large errors heavily. Average of squared errors.  
   - **RMSE** (Root Mean Squared Error) - typical size of prediction errors, with more weight on big mistakes 
   - **MAE** (Mean Absolute Error) - Average absolute difference in $ between predicted and actual resale price 
   - **MAPE** (%) - Average percentage error. 50% means off by that % on average. 
   - **R² (Test)** - % of variance in resale price explained by model on test data 
   - **Train R²** - Helps to detect overfitting/underfitting     

4. Libraries used:
   - pandas
   - numpy 
   - matplotlib
   - seaborn
   - scikit-learn

 5. Key Insights and Observations
    - Features like floor_area_sqm, flat_model, and remaining_lease had        strong correlation to the resale_price (target_value).

    - Tree-based models like Random Forest and XGBoost outperformed     
      linear models on accuracy.

    - Grid search tuning significantly boosted model performance,               especially for XBGRegressor and Random Forest.  



