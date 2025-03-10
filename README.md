# From Data to Decision: A Holistic Approach to Classification, Regression, and Clustering"
## Datasets:
### Regression - Diamond Prices:

Dataset: diamonds.csv
Variable to be Predict Y= “Price”

## Dataset
The report is based on the following dataset:
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

### Classification - IBM_HR_analytics and employee attrition:

Dataset: HR_comma_sep.csv
Variable to be Predict Y= “Left”

### Tasks:
1) Data Pre-processing
2) Data Analysis with 4 models, Hyperparameter tunning, Grid search
       - Regression [Linear Regression, Decision Tree Regression, SVM Regression, KNN Regression]
       - Classification [Logistic Regression, Decision Tree Classification, SVM Classification, KNN Classification]
3) K-Fold Cross Validation
4) Data Analysis with 4 different model and compare 8 models
       - Random Forest, XGBoost, CatBoost, LightGBM
5) Plotly Library to plot and find out best model with high accuracy
6) Create Dashboard for three best- performed regression model [Drop box, Multiple Select, RMSE]
7) Prediction with Neutral Networks
       - Pre-processing
       - Find optimal training time
       - Present Performance result with 3 best architectures
       - 5 fold cross-validation
6) Feature importance evaluated
7) LIME method for locally calculate feature importance
8) Partial Dependence Plot for each features for Best NN model

### Dimentionality Reduction
### Tasks:
1) PDP plot
2) tSNE Plot

### Cluster Analysis
### Tasks:
1) K-means Clustering
2) Hierarchical Clustering
3) DBScan Clustering
4) Reduced Dataset Clustering

### Power BI report
# Power BI Report: Employee Turnover Analysis

## Overview
This Power BI report provides insights into employee turnover, satisfaction, and performance metrics. It is designed to help HR and management teams analyze factors influencing employee retention and make data-driven decisions.

## Key Features
- **Employee Turnover Analysis:** Visualize turnover rates by department, salary level, and tenure.
- **Satisfaction Level Trends:** Analyze employee satisfaction across different groups.
- **Performance Evaluation:** Compare employee performance (`last_evaluation`) with hours worked and satisfaction levels.
- **Promotion Impact:** Track the impact of promotions on employee retention.
- **Work Accident Analysis:** Visualize the distribution of work accidents and their impact on turnover.

## Visualizations
The report includes the following visualizations:
1. **Employee Turnover by Department:** Stacked bar chart showing turnover rates across departments.
2. **Satisfaction Level by Salary:** Clustered column chart comparing average satisfaction levels by salary.
3. **Average Monthly Hours vs. Last Evaluation:** Scatter plot analyzing the relationship between hours worked and performance.
4. **Number of Projects vs. Satisfaction Level:** Line chart showing how satisfaction changes with the number of projects.
5. **Promotion Impact on Retention:** Donut chart visualizing the impact of promotions on turnover.
6. **Work Accident Distribution:** Pie chart showing the proportion of employees involved in work accidents.

