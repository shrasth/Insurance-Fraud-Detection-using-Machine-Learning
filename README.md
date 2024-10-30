# Insurance Data Analytics Project

This project focuses on analyzing insurance claim data provided by **an insurance company in Canada** to identify fraudulent claims and generate valuable KPIs. Using big data analytics and machine learning techniques, the project aims to detect fraudulent activities, generate KPIs (Key Performance Indicators), and provide actionable insights for improving business performance.

## Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Data Source](#data-source)
- [Notebooks](#notebooks-included)
  - [KPI Generation](#kpi-generation-notebook)
  - [Predictive Modeling](#predictive-modeling-notebook)
- [Key Insights and KPIs](#key-insights-and-kpis)
- [Predictive Modeling](#predictive-modeling)
- [Dashboard Visualization](#dashboard-visualization)
- [How to Use](#how-to-use)
---

## Project Overview

- **Description**: This project investigates fraudulent insurance claims using advanced data analytics techniques. It generates KPIs to understand the performance of various aspects of the insurance business, including claims and policyholder behavior. It also builds predictive models to detect fraudulent claims and assess model performance.
  
- **Objective**: 
  - Identify fraudulent claims.
  - Generate KPIs for various insurance metrics.
  - Build predictive models to classify fraudulent vs. non-fraudulent claims.
  - Visualize the results in interactive dashboards.

---

## Technologies Used

- **Python**: For data processing, predictive modeling, and analysis.
- **Pandas**: For data cleaning and manipulation.
- **Matplotlib/Seaborn**: For data visualization and charting.
- **Scikit-learn**: For implementing machine learning models like Random Forest.
- **SMOTE (Synthetic Minority Over-sampling Technique)**: To balance the dataset for predictive modeling.
- **Power BI/Tableau**: For building interactive dashboards to visualize KPIs and trends.

---

## Data Source

- The dataset contains over 15,000 rows and 33 columns, covering various aspects of insurance claims such as policy details, agent information, car models, insurance types, and claim types. The data was provided by **an insurance company in Canada**.

---

## Notebooks Included

### 1. KPI Generation Notebook

- **File**: [`KPI_Generation.ipynb`] (https://github.com/shrasth/Fraud-Detection-Data-Pipeline/blob/main/insurance_data.ipynb)
- **Description**: This notebook generates key performance indicators (KPIs) for insurance claims. It analyzes policyholder behavior, claim settlement times, agent performance, and much more. KPIs help the business make data-driven decisions.

### 2. Predictive Modeling Notebook

- **File**: [`ML_-_fraud_data_updated.ipynb`](https://github.com/shrasth/Insurance-Data-Analytics/blob/main/ML_-_fraud_data_updated.ipynb)
- **Description**: This notebook focuses on building and evaluating machine learning models for fraud detection. It applies techniques like Random Forest, SMOTE, and evaluates model accuracy, precision, recall, and F1 score.

---

## Key Insights and KPIs

### KPIs Generated:

1. **Age Group Trends**:
   - The highest number of claims comes from the 31-35 age group (~2800 claims), followed by the 26-30 age group (~2700 claims).
   
2. **Agent Policies**:
   - Agent 7 handles the most policies (1072), while Agent 13 handles the least (880).
   
3. **Automobile Claims**:
   - **Most Claimed Brands**: Pontiac, Toyota, Honda, Mazda, and Chevrolet.
   - **Luxury Brands with Fewer Claims**: Lexus, Ferrari, Mercedes, Porsche, Jaguar.
   
4. **Claim Settlement Time**: The average claim is settled in **5 days**.
   
5. **Retention and Churn**:
   - Retention Rate: **95%**
   - Churn Rate: **5%**

6. **Yearly Trends**:
   - The total number of policies has been declining over the past three years.
   - Collision-type policies are the most common, followed by liability and all-perils policies.

---

## Predictive Modeling

The **Machine Learning** part of this project focused on detecting fraudulent claims using supervised learning models. Multiple models were trained and evaluated to determine the best performance for fraud detection.

### Steps Involved:
1. **Data Preprocessing**: 
   - Handled missing values, encoded categorical variables, and split the dataset into training and testing sets.
   
2. **Class Imbalance Handling**: 
   - Used **SMOTE** (Synthetic Minority Over-sampling Technique) to address class imbalance, as the dataset had fewer fraudulent claims compared to non-fraudulent claims.

3. **Models Evaluated**:
   - **Logistic Regression**: A baseline model.
   - **Decision Trees**: A simple, interpretable model.
   - **Random Forest**: A powerful ensemble model.
   - **Support Vector Machines (SVM)**: To classify data points with a high-dimensional hyperplane.
   - **K-Nearest Neighbors (KNN)**: To classify claims based on their closest neighbors.
   - **Gradient Boosting**: A boosting model for more complex patterns.
   - **Random Forest with SMOTE** (Chosen Model): This combination yielded the best results for fraud detection.

### Model Evaluation Metrics:
- **Accuracy**: Measures the overall performance of the model.
- **Precision**: The percentage of predicted fraudulent claims that were correct.
- **Recall**: The percentage of actual fraudulent claims that were correctly identified.
- **F1 Score**: The harmonic mean of precision and recall.

### Final Model Performance (Random Forest X SMOTE):
- **Overall Accuracy**: 95%
- **Case 0 (Non-Fraud)**:
  - Precision: 96%
  - Recall: 96%
  - F1 Score: 96%
- **Case 1 (Fraud)**:
  - Precision: 96%
  - Recall: 96%
  - F1 Score: 96%

The **Random Forest X SMOTE** model was chosen based on its ability to handle class imbalance and its high performance in predicting both fraudulent and non-fraudulent claims.

---

## Dashboard Visualization

The final phase of the project involved building an interactive dashboard to visualize the insights derived from the analysis. The dashboard includes:

1. **KPIs**:
   - Quote Rate, Fraud Found, Total Policies, Retention Rate, and Churn Rate.
   
2. **Claim Analysis**:
   - A pie chart showing the frequency of claims per policy (35% of policyholders made 2-4 claims, 27% made no claims).
   
3. **Fraud Trends**:
   - Bar charts visualizing fraudulent vs. non-fraudulent claims over the years, with a declining trend in the total number of policies.

4. **Policy Distribution by Area**:
   - A donut chart showing the majority of claims are from **urban regions**.

5. **Agent Performance**:
   - Bar charts comparing agents' performances based on the number of policies they handle.

---

## How to Use

### 1. Clone the Repository

To download and work with this project locally, clone the repository:

```bash
git clone https://github.com/shrasth/Insurance-Data-Analytics.git
