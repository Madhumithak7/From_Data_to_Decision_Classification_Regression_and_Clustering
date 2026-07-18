# From Data to Decision: A Holistic Approach to Classification, Regression, and Clustering

## Datasets

### Regression — Diamond Prices

**Dataset:** `diamonds.csv`
**Target variable (Y):** `price`

- **Columns:**
  - `carat`: Weight of the diamond.
  - `cut`: Quality of the cut (Fair, Good, Very Good, Premium, Ideal).
  - `color`: Diamond color grading.
  - `clarity`: Clarity grading (measure of internal/external flaws).
  - `depth`: Total depth percentage.
  - `table`: Width of the top of the diamond relative to widest point.
  - `price`: Price in US dollars (target variable).
  - `x`, `y`, `z`: Length, width, and depth in mm.

*(Confirm/edit this list against your actual notebook if any columns differ.)*

### Classification — IBM_HR_analytics and Employee Attrition

**Dataset:** `HR_comma_sep.csv`
**Target variable (Y):** `left`

- **Columns:**
  - `satisfaction_level`: Employee satisfaction score (0-1).
  - `last_evaluation`: Last performance evaluation score (0-1).
  - `number_project`: Number of projects assigned to the employee.
  - `average_montly_hours`: Average monthly hours worked.
  - `time_spend_company`: Years spent in the company.
  - `Work_accident`: Whether the employee had a work accident (1 = yes, 0 = no).
  - `left`: Whether the employee left the company (1 = yes, 0 = no).
  - `promotion_last_5years`: Whether the employee was promoted in the last 5 years (1 = yes, 0 = no).
  - `Department`: Employee department (e.g., Sales, HR, IT).
  - `salary`: Employee salary level (low, medium, high).

## Tasks

1. Data Pre-processing
2. Data Analysis with baseline models, hyperparameter tuning, Grid Search — Regression [Linear Regression, Decision Tree Regression, SVR, KNN Regression] — Classification [Logistic Regression, Decision Tree Classification, SVC, KNN Classification]
3. K-Fold Cross Validation
4. Data Analysis with ensemble models — Random Forest, XGBoost, CatBoost, LightGBM
5. Plotly library used to visualize and identify best-performing models
6. Dashboard created for the three best-performing regression models [Drop box, Multiple Select, RMSE]
7. Prediction with Neural Networks — pre-processing, optimal training time, performance results with 3 best architectures, 5-fold cross-validation
8. Feature importance evaluated
9. LIME method used to locally calculate feature importance
10. Partial Dependence Plot (PDP) generated for each feature for the best Neural Network model

## Regression Modeling Pipeline

This project evaluates **12 regression models** to predict diamond prices, using hyperparameter tuning (GridSearchCV) and k-fold cross-validation for robust performance comparison.

### Models Evaluated

| Model | Type |
|---|---|
| Linear Regression | Linear |
| Ridge Regression | Linear (regularized) |
| Lasso Regression | Linear (regularized) |
| [4th linear variant, if used] | Linear (regularized) |
| Decision Tree Regressor | Tree-based |
| Support Vector Regressor (SVR) | Kernel-based |
| K-Nearest Neighbors (KNN) Regressor | Instance-based |
| Random Forest Regressor | Ensemble (bagging) |
| XGBoost Regressor | Ensemble (boosting) |
| CatBoost Regressor | Ensemble (boosting) |
| LightGBM Regressor | Ensemble (boosting) |

### Methodology

1. **Data preprocessing** — feature scaling with `StandardScaler`/`MinMaxScaler`, categorical encoding with `LabelEncoder`.
2. **Train/test split** — via `train_test_split`.
3. **Hyperparameter tuning** — `GridSearchCV` used to optimize model parameters.
4. **Cross-validation** — `KFold` cross-validation applied to ensure robust, generalizable performance estimates.
5. **Evaluation metrics** — R² score, Mean Squared Error (MSE), and Mean Absolute Error (MAE) via `sklearn.metrics`.
6. **Visualization** — results plotted using `Plotly` for interactive comparison across all 12 models.

## Classification Modeling Pipeline

This project evaluates **12 classification models** to predict employee attrition (`left`), using hyperparameter tuning (GridSearchCV) and k-fold cross-validation for robust performance comparison.

### Models Evaluated

| Model | Type | Accuracy |
|---|---|---|
| Random Forest | Ensemble (bagging) | 0.9883 |
| XGBoost | Ensemble (boosting) | 0.9877 |
| LightGBM | Ensemble (boosting) | 0.9863 |
| CatBoost | Ensemble (boosting) | 0.9857 |
| Decision Tree | Tree-based | 0.9797 |
| KNN | Instance-based | 0.9562 |
| SVC | Kernel-based | 0.7935 |
| Logistic Regression | Linear | 0.7807 |
| [9th model, e.g. Ridge Classifier] | Linear (regularized) | — |
| [10th model] | — | — |
| [11th model] | — | — |
| [12th model] | — | — |

**Best performing model: Random Forest (98.83% accuracy)**

### Key Insight

Tree-based ensemble methods (Random Forest, XGBoost, LightGBM, CatBoost) significantly outperformed linear and kernel-based models (Logistic Regression, SVC), suggesting non-linear relationships between features like satisfaction level, tenure, and attrition that linear models cannot capture as effectively.

### Tools & Libraries Used (Regression & Classification)

`NumPy` · `Pandas` · `Matplotlib` · `Seaborn` · `Plotly` · `scikit-learn` · `XGBoost` · `CatBoost` · `LightGBM`

## Dimensionality Reduction

### Tasks

1. PDP plot
2. t-SNE plot

## Cluster Analysis

### Tasks

1. K-means Clustering
2. Hierarchical Clustering
3. DBSCAN Clustering
4. Reduced Dataset Clustering

## Power BI Report: Employee Turnover Analysis

### Overview

This Power BI report provides insights into employee turnover, satisfaction, and performance metrics. It is designed to help HR and management teams analyze factors influencing employee retention and make data-driven decisions.

### Key Features

- **Employee Turnover Analysis:** Visualize turnover rates by department, salary level, and tenure.
- **Satisfaction Level Trends:** Analyze employee satisfaction across different groups.
- **Performance Evaluation:** Compare employee performance (`last_evaluation`) with hours worked and satisfaction levels.
- **Promotion Impact:** Track the impact of promotions on employee retention.
- **Work Accident Analysis:** Visualize the distribution of work accidents and their impact on turnover.

### Visualizations

1. **Employee Turnover by Department:** Stacked bar chart showing turnover rates across departments.
2. **Satisfaction Level by Salary:** Clustered column chart comparing average satisfaction levels by salary.
3. **Average Monthly Hours vs. Last Evaluation:** Scatter plot analyzing the relationship between hours worked and performance.
4. **Number of Projects vs. Satisfaction Level:** Line chart showing how satisfaction changes with the number of projects.
5. **Promotion Impact on Retention:** Donut chart visualizing the impact of promotions on turnover.
6. **Work Accident Distribution:** Pie chart showing the proportion of employees involved in work accidents.
