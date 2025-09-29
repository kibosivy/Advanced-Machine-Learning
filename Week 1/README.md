# Car Price Prediction with PCA and Gradient Boosting  

## Project Overview  
This project aims to predict used car prices using machine learning. The dataset contains information such as car brand, model, year of manufacture, mileage, and other features. The target variable is **Price**.  

Due to the high dimensionality from categorical encoding, **Principal Component Analysis (PCA)** was applied to reduce features while retaining most of the variance. Multiple regression models were evaluated, with **Gradient Boosting Regressor** emerging as the best-performing model after hyperparameter tuning.  

---

## Workflow  

### 1. Data Preprocessing  
- Dropped irrelevant columns such as `Registration Number`.  
- Encoded categorical variables.  
- Standardized numerical features using **StandardScaler**.  

### 2. Dimensionality Reduction with PCA  
- Applied PCA on scaled features.  
- Selected components explaining **95% of variance (766 components)**.  
- This step reduced dimensionality and improved computational efficiency.  

### 3. Model Training and Hyperparameter Tuning  
- Train/test split (80/20).  
- Models tested: Linear Regression, Ridge, Lasso, Kernel, Support Vector Regression Random Forest, Gradient Boosting.  
- Performed **hyperparameter tuning** on Gradient Boosting using `RandomizedSearchCV`.  
- Final tuned model showed the best performance on the test set.  

### 4. Model Evaluation  
- Metrics: MSE, RMSE, MAE, R² Score.  
- Gradient Boosting achieved the lowest error and highest R² compared to other models.  

### 5. Learning and Loss Curves  
- Plotted **learning curves** to check for underfitting or overfitting.  
- Plotted **loss curves** (training vs validation error over iterations).  

### 6. Error Analysis  
- Residual plots to visualize prediction errors.  
- Distribution of errors to check normality.  
- Identified where the model underperformed (e.g., extreme high-value cars).  

---

## Results  
- PCA reduced the dataset to **766 features** while retaining 95% variance.  
- Gradient Boosting Regressor with tuned parameters achieved the best performance.  

