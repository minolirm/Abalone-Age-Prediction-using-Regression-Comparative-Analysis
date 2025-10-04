# Abalone-Age-Prediction-using-Regression-Comparative-Analysis
This project investigates the effectiveness of multiple regression and machine learning models for predicting the age of abalones using their physical characteristics. The study uses the Abalone dataset from the UCI Machine Learning Repository, which includes physical measurements such as length, diameter, height, and shell weight.

# 🐚 Regression and Classification Modelling in Predicting the Age of Abalone: A Comparative Analysis  

**Author:** Minoli R. Munasinghe  
**Institution:** Department of Mathematics and Statistics, Thompson Rivers University, Kamloops, Canada  
**Email:** [minolimunasinghe@outlook.com](mailto:minolimunasinghe@outlook.com)

---

## 📘 Overview  
This project investigates the effectiveness of multiple regression and machine learning models for predicting the **age of abalones** using their physical characteristics. The **Abalone dataset** from the **UCI Machine Learning Repository** is used, which includes measurements such as length, diameter, height, and shell weight.

Accurately predicting abalone age is essential for the **fisheries sector**, as age directly impacts the **economic value** of abalone. Traditional age estimation by counting shell rings is time-consuming; hence, this project uses statistical and machine learning approaches to automate and improve prediction accuracy.

---

## 🎯 Objectives  
- Compare different **regression models** for abalone age prediction.  
- Evaluate model performance using **RMSE** and **R²** values.  
- Assess **computational efficiency** across models.  
- Explore the impact of **feature engineering** (scaling, transformation).  
- Identify the **best-performing model** for practical use in fisheries.

---

## 📊 Dataset  
**Source:** [UCI Machine Learning Repository – Abalone Dataset](https://archive.ics.uci.edu/ml/datasets/abalone)  

| Variable | Type | Unit | Description |
|-----------|------|------|-------------|
| Sex | Categorical | - | Male, Female, or Infant |
| Length | Continuous | mm | Longest shell measurement |
| Diameter | Continuous | mm | Perpendicular to length |
| Height | Continuous | mm | Height with shell |
| Whole Weight | Continuous | grams | Weight of whole abalone |
| Shucked Weight | Continuous | grams | Weight of the flesh |
| Viscera Weight | Continuous | grams | Gut weight after bleeding |
| Shell Weight | Continuous | grams | Shell weight after drying |
| Rings | Integer | - | Number of rings (Age = Rings + 1.5 years) |

- **Observations:** 4,177  
- **Response variable:** Rings  
- **Outliers removed:** 164 records  

---

## ⚙️ Methodology  

### 🔹 Data Preprocessing  
- Converted `Sex` categorical variable to numeric.  
- Applied **Standard Scaling** to all predictors:  
  \[
  x_{scaled} = \frac{x - mean(x)}{sd(x)}
  \]
- Split dataset into **80% training** and **20% testing** subsets.  
- Applied **feature engineering** (scaling + log transformation).  
- Used **10-fold cross-validation** for all models to avoid overfitting and find optimal hyperparameters.

---

## 🤖 Models Used  

| Model | Purpose / Strength |
|--------|--------------------|
| **Multiple Linear Regression (MLR)** | Baseline model to determine linear relationships. |
| **Principal Component Regression (PCR)** | Reduces multicollinearity using dimensionality reduction. |
| **Ridge Regression** | Handles multicollinearity using L2 regularization. |
| **Lasso Regression** | Performs feature selection and handles multicollinearity via L1 regularization. |
| **Support Vector Regressor (SVR)** | Captures non-linear relationships between predictors and target. |
| **Decision Tree Regressor** | Handles interactions between predictors and minimizes residual variance. |
| **Random Forest Regressor (RFR)** | Prevents overfitting and improves prediction accuracy using ensemble learning. |
| **Neural Network (NN)** | Learns complex non-linear relationships in data. |
| **Bayesian Regression** | Incorporates uncertainty and prior distributions in prediction. |

---

## 🔧 Evaluation Metrics  
Each model was evaluated using:  
- **Root Mean Squared Error (RMSE)**  
- **R-squared (R²)**  
- **Computation Time**

---

## 🧠 Key Findings  
- **Random Forest Regressor** achieved the **best performance** overall in RMSE, R², and computational efficiency.  
- **Feature engineering** (scaling and log transformation) improved performance for most models.  
- Models like **PCR, Ridge, and Lasso** effectively handled multicollinearity, but ensemble models achieved higher predictive accuracy.

---

## 🧩 Tools and Technologies  
- **Language:** R  
- **Libraries:** `caret`, `tidyverse`, `randomForest`, `e1071`, `glmnet`, `nnet`, `MASS`  
- **IDE:** RStudio  

---

## 📈 Results Summary  

| Model | RMSE | R² | Remarks |
|--------|------|----|----------|
| Multiple Linear Regression | Moderate | Moderate | Baseline model |
| Ridge Regression | Improved | High | Handles collinearity |
| Lasso Regression | Similar to Ridge | High | Performs feature selection |
| SVR | High accuracy | High | Captures non-linearity |
| Decision Tree | Moderate | Medium | Sensitive to overfitting |
| **Random Forest** | **Lowest RMSE** | **Highest R²** | **Best overall** |
| Neural Network | Good | High | Computationally expensive |
| Bayesian Regression | Moderate | Medium | Handles uncertainty |

---

## 📚 References  
1. UCI Machine Learning Repository – [Abalone Dataset](https://archive.ics.uci.edu/ml/datasets/abalone)  
2. Jabeen, F., & Ahamed, S. – *Predicting Age of Abalone Using ANN*  
3. Mehta, K. – *Regression Models for Abalone Age Prediction*  
4. Other related studies and GitHub repositories (see paper for full reference list).  
