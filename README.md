# Employee Attrition Prediction

## Project Overview
This project aims to predict employee attrition (the likelihood of employees leaving the company) using machine learning techniques. The goal is to develop a predictive model that can identify which employees are more likely to quit based on features such as job satisfaction, job involvement, education, performance rating, relationship satisfaction, and work-life balance. By accurately predicting attrition, companies can take proactive measures to retain valuable employees and reduce the costs associated with employee turnover.

---

## Business Case & Problem Statement

Employee attrition is a significant challenge for companies, with high costs associated with both employee turnover and recruitment. On average, companies lose **1-2.5% of their total revenue** while onboarding new hires and bringing them up to speed. Furthermore, organizations often spend **15-20% of an employee's salary** on recruitment and hiring costs. These statistics highlight the importance of understanding employee attrition patterns and being able to predict which employees are at risk of leaving the company.

By predicting employee attrition, companies can:
- Take targeted action to retain high-performing employees.
- Reduce recruitment and onboarding costs.
- Create a more stable workforce and increase overall productivity.

---

## Objectives
The key objectives of this project are:
1. **Data Preprocessing**: Clean and prepare employee data for analysis.
2. **Exploratory Data Analysis (EDA)**: Analyze the dataset to uncover patterns and trends related to employee attrition.
3. **Model Training**: Train machine learning models to predict employee attrition.
4. **Model Evaluation**: Evaluate the performance of the models using classification metrics like accuracy, precision, recall, and F1 score.
5. **Model Comparison**: Compare the performance of different machine learning algorithms (e.g., Logistic Regression vs. XGBoost).
6. **Business Insights**: Provide insights based on the model’s predictions that can inform HR decision-making processes.

---

## Dataset

The dataset used in this project is the `employee_data.csv` file, which contains information about employees and whether they have left the company (attrition). The features in the dataset include both numerical and categorical data, such as:
- **Numerical Features**: Age, Daily Rate, Distance from Home, Monthly Income, Years at Company, Total Working Years, etc.
- **Categorical Features**: Business Travel, Department, Education, Gender, Job Role, Marital Status, etc.
- **Target Variable**: Attrition (binary: 1 if the employee left, 0 if the employee stayed).

---

## Steps Taken in the Project

1. **Import Libraries & Dataset**: The necessary libraries (Pandas, Numpy, Seaborn, Matplotlib, Scikit-learn, etc.) were imported, followed by loading the employee data into a Pandas DataFrame.

2. **Data Preprocessing**:
   - Categorical columns (e.g., Attrition, OverTime) were converted into numerical values (1 and 0).
   - Irrelevant columns such as `EmployeeCount`, `EmployeeNumber`, and `Over18` were dropped from the dataset.
   - One-hot encoding was applied to categorical features like Business Travel, Department, Gender, etc.

3. **Exploratory Data Analysis (EDA)**:
   - **Statistical Summary**: We obtained a statistical summary of the dataset to understand the mean, min, max, and other statistical metrics for various features, including employee age.
   - **Data Visualization**: Various visualizations were created, including histograms, count plots, and KDE plots to explore relationships between features and attrition.
   - **Correlation Matrix**: A correlation heatmap was plotted to understand how different numerical features relate to each other.

4. **Feature Engineering**:
   - The dataset was split into categorical and numerical features.
   - The numerical features were normalized using **MinMaxScaler** to ensure that all features are on the same scale.

5. **Model Training**:
   - The dataset was split into training and testing sets (75% for training and 25% for testing).
   - A **Logistic Regression** model was trained to predict employee attrition, and performance metrics were evaluated (accuracy, confusion matrix, classification report).
   - **XGBoost** was used as an alternative model to compare performance.

6. **Model Evaluation**:
   - The accuracy of both models (Logistic Regression and XGBoost) was evaluated.
   - Performance metrics like confusion matrix, precision, recall, F1 score were calculated.

---

## Insights and Findings

- **Key Factors Contributing to Employee Attrition**:
  - Employees with **lower job satisfaction**, **lower work-life balance**, and **lower performance ratings** are more likely to leave the company.
  - Employees with **higher job involvement** and **longer years with the current manager** tend to stay longer.
  - Certain job roles (e.g., Sales Representatives) and marital status (e.g., single employees) were found to have a higher tendency to leave the company.

- **Correlations**:
  - **Job level** is strongly correlated with **total working years** and **monthly income**. Higher job levels are associated with higher incomes and more years of work experience.
  - **Monthly income** is also highly correlated with **job level** and **total working years**, which suggests that employees who have worked longer tend to earn more and are in higher job levels.

---

## Model Performance

- **Logistic Regression**: 
  - Achieved good performance on the test data with high accuracy. The confusion matrix and classification report showed that the model performed well in predicting both attrition and non-attrition cases.
  
- **XGBoost**:
  - The XGBoost model also showed strong performance, with improvements in prediction accuracy and a better classification report compared to Logistic Regression.
  
- **Comparison**:
  - XGBoost outperformed Logistic Regression in terms of accuracy and precision, making it a better choice for this specific task.

---

## Conclusion & Business Impact

- By predicting which employees are more likely to leave the company, businesses can take proactive measures to reduce attrition. For instance:
  - **Targeted retention strategies** for employees with low job satisfaction or poor work-life balance.
  - **Training and career development opportunities** for employees in lower job levels to increase job satisfaction and reduce turnover.
  
- The **XGBoost model** has shown to be more effective in predicting attrition, and its implementation can lead to a better understanding of employee behavior, enabling HR departments to make data-driven decisions.

---

## References

- Scikit-learn Documentation: [https://scikit-learn.org/](https://scikit-learn.org/)
- XGBoost Documentation: [https://xgboost.readthedocs.io/](https://xgboost.readthedocs.io/)
- Seaborn Documentation: [https://seaborn.pydata.org/](https://seaborn.pydata.org/)

