# 🏡 House Price Prediction Project  

## 📌 Overview  
This project focuses on predicting **house prices** using the `housing.csv` dataset.  
The workflow includes **data preprocessing, exploratory data analysis (EDA), feature engineering, visualization, modeling, and evaluation**.  

---

## ⚙️ Steps  

### 1. Import & Setup  
- Import all necessary Python libraries (Pandas, Numpy, Seaborn, Matplotlib, Scikit-learn).  

### 2. Load & Clean Data  
- Load the dataset (`housing.csv`).  
- Drop missing values.  

### 3. Train-Test Split  
- Split the dataset into **train (80%)** and **test (20%)**.  

### 4. Exploratory Data Analysis (EDA)  
- Histograms of numerical features.  
- Correlation heatmaps.  
- Pairplots & scatterplots.  
- Skewness and Kurtosis analysis.  

### 5. Data Transformation  
- Apply **log transformation** to skewed features (`total_rooms`, `total_bedrooms`, `median_income`, `population`).  

### 6. Encoding  
- Perform **OneHotEncoding** on the categorical feature `ocean_proximity`.  

### 7. Feature Engineering  
Created new features:  
- `rooms_per_household`  
- `bedrooms_per_room`  
- `population_per_household`  
- `price_per_room`  

### 8. Scaling & PCA  
- StandardScaler applied to features.  
- PCA visualization of explained variance.  
- PCA(95%) pipeline with Linear Regression.  

### 9. Models Implemented  
- **Linear Regression**  
- **Decision Tree**  
- **K-Nearest Neighbors (KNN)**  
- **Random Forest**  

### 10. Model Evaluation  
Metrics used:  
- RMSE (Root Mean Squared Error)  
- MAE (Mean Absolute Error)  
- R² Score  

### 11. Model Comparison  
- Comparison of all models using bar plots of RMSE.  

### 12. Cross Validation  
- Cross validation applied on Linear Regression.  

### 13. Hyperparameter Tuning  
- GridSearchCV applied on **Random Forest** to find best hyperparameters.  

### 14. Feature Importances  
- Plotted top 15 important features from Random Forest.  

---

## 📊 Results  

| Model              | RMSE   | MAE    | R²   |
|--------------------|--------|--------|------|
| Linear Regression  | 11474.28 | 6524.01 | 0.9899 |
| Decision Tree      | 6571.82 | 2773.84 | 0.9967 |
| KNN                | 24738.97 | 16678.26 | 0.9530 |
| Random Forest      | 3463.65 | 861.00 | 0.9991 |
| RF (Tuned)         | 10178.19 | 5786.53 | 0.9920 |
| Linear + PCA       | 19053.97 | 13718.32 | 0.9721 |

---

## 📌 Visualizations Included  
- Histograms & KDE plots.  
- Boxplots for outliers.  
- Heatmaps of correlations.  
- Pairplots of numerical variables.  
- Residual plots.  
- Feature importances.  

---

## 🚀 How to Run  
1. Clone the repo or download the files.  
2. Make sure you have Python 3.x installed.  
3. Install dependencies:  
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
