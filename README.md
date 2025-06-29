# Workforce Attrition Analysis: A Data-Driven Predictive Approach
-- By Omkar Masurekar | May 2025

This repository contains code, dashboards, and documentation for a comprehensive workforce attrition analysis project.
This project focused on applying advanced data science techniques to understand, visualize, and predict employee attrition over a 5-year period. The work combined interactive Power BI dashboards for descriptive analytics and a Python XGBoost model for predictive insights, enabling data-driven HR decision-making.

## Technical Approach
### Data Engineering & Preprocessing
- Data sources: Integrated multiple HR datasets (employee records, surveys, performance ratings) using Python (Pandas).

#### Cleaning:
- Handled missing values via imputation (e.g., median SEW scores).
- Standardized date formats and derived features like Tenure, ExitYear.
- Applied outlier detection (Modified Z-score, DBSCAN) on tenure and engagement scores.

#### Feature engineering:
- Calculated rolling attrition rates per year.
- Derived SEW (Satisfaction, Engagement, Work-Life Balance) as a composite metric.
- Created categorical bins for tenure, performance, and SEW scores.

## Power BI Visualization
Built an interactive dashboard showing:
- Attrition trends by year, job type, tenure group.
- Voluntary vs. involuntary terminations.
- Drilldowns for gender, job type, and SEW band analysis.

![image](https://github.com/user-attachments/assets/78c88b3a-6053-4c5e-bff8-5ee69cdacd9f)


## Predictive Modelling
- Model: XGBoost classifier
- Target: Binary attrition label (1 = terminated, 0 = active)
- Key features: Tenure group, SEW score band, performance rating, job type, gender
- Hyperparameter tuning: Used GridSearchCV for parameters like max_depth, learning_rate, n_estimators.
- Validation: 80/20 train-test split, model achieved:
  - Accuracy: 97.2%
  - AUC: 0.98
  - Precision on high-risk group: 95%
- Explainability:
  - Applied SHAP values to rank feature importance.
  - Identified Tenure <1yr, Low SEW, and Medium Performance as top risk drivers.

 ## Key Findings
- Attrition Rate: ~51% overall, dominated by voluntary exits.
- Risk groups: Early tenure (<1yr), low SEW scores, medium/low performers.
- High-risk job types: Managers, academic staff, and professional officers in mid-career stages.
- Engagement vs. performance: Low SEW had stronger correlation with attrition than performance alone.

## 📈 Recommendations
### ✅ Short-term
- Flag high-risk staff for engagement interventions.
- Prioritize SEW improvement initiatives (surveys, work-life balance programs).

### 🌱 Long-term
- Integrate XGBoost model into HR dashboards for continuous risk monitoring.
- Design data-driven career pathing and retention plans.

### 🛠 Tools & Technologies
- Python: Pandas, PySpark, XGBoost, SHAP, Matplotlib, Seaborn
- Power BI: Custom visuals, row-level security, drillthrough pages
- Databricks: Data wrangling

## 📝 Conclusion
This project demonstrates the power of combining predictive modelling and business intelligence tools to tackle workforce challenges. The integration of machine learning, automation, and visualization can significantly enhance HR’s ability to make proactive, data-driven decisions.

## ✨ About Me
I'm a Data Scientist passionate about turning complex data into actionable insights through machine learning, automation, and visualization.

