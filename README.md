# Supply Chain Late Delivery Risk Prediction Using Machine Learning

## Project Overview

Late deliveries can increase operating costs, reduce customer satisfaction, and create challenges for supply chain teams trying to manage orders proactively.

This project analyzes a large supply chain dataset to identify the factors associated with late deliveries and develop a machine learning model capable of flagging orders that are at risk of arriving late.

The analysis was completed in Python and covers the full workflow from data cleaning and exploratory analysis through feature engineering, model development, evaluation, and business recommendations.

---

## Business Problem

The objective of this project was to answer the following question:

**Can historical order, customer, shipping, and product information be used to identify orders that are at risk of late delivery before the delay occurs?**

A useful predictive model could help supply chain teams:

- Identify high-risk orders earlier
- Prioritize orders requiring intervention
- Improve customer communication
- Make better shipping decisions
- Reduce the operational impact of late deliveries

---

## Dataset

The original DataCo Supply Chain dataset contained approximately:

- **180,519 records**
- **53 original features**

Following data cleaning, feature selection, and removal of variables that were not required for the analysis, the analytical dataset contained **22 variables**.

The dataset includes information related to:

- Customer characteristics
- Customer segments and locations
- Markets and order regions
- Product and order values
- Discounts and quantities
- Shipping modes
- Scheduled shipment times
- Order dates
- Late delivery risk

---

## Tools & Technologies

- **Python**
- **Pandas** – data manipulation and cleaning
- **NumPy** – numerical operations
- **Matplotlib** – data visualization
- **Seaborn** – exploratory visualizations
- **Scikit-learn** – preprocessing, feature selection and machine learning
- **Jupyter Notebook** – development environment

---

## Project Workflow

### 1. Data Understanding

The dataset was initially explored to understand:

- Dataset dimensions
- Column types
- Missing values
- Duplicate records
- Numerical and categorical features
- Distribution of the target variable

The target variable for the analysis was:

**Late_delivery_risk**

where the objective was to distinguish between orders at risk of late delivery and those not at risk.

---

### 2. Data Cleaning & Preprocessing

The preprocessing stage included:

- Reviewing missing values
- Checking duplicate records
- Removing unnecessary or noisy variables
- Reviewing categorical values for inconsistencies
- Preparing numerical and categorical features
- Creating time-based features for analysis
- Exporting the cleaned dataset for further analysis

Categorical variables were converted into numerical form using Scikit-learn's `LabelEncoder` to prepare the data for correlation analysis and machine learning.

---

### 3. Exploratory Data Analysis

Exploratory analysis was conducted to better understand the factors associated with delivery performance.

Areas investigated included:

- Shipping mode
- Customer segment
- Geographic markets
- Scheduled shipping days
- Product and order characteristics
- Late versus on-time delivery patterns

One finding from the analysis was that **shipping mode showed a meaningful relationship with late-delivery risk**, indicating that delivery performance varied across shipping methods.

---

### 4. Correlation & Feature Selection

A correlation analysis was performed after categorical variables were encoded.

Feature selection techniques were then used to identify variables with stronger predictive relationships with late-delivery risk.

`SelectKBest` with the `f_classif` scoring method was also used to evaluate feature importance and reduce unnecessary noise in the modelling process.

---

## Machine Learning Models

Three classification algorithms were developed and compared:

1. **Logistic Regression**
2. **Random Forest Classifier**
3. **Decision Tree Classifier**

The models were evaluated using:

- Accuracy
- Precision
- Recall

Recall was particularly important for this business problem because failing to identify an order that will actually arrive late may prevent the business from intervening before the customer is affected.

---

## Model Performance

| Model | Accuracy | Precision | Recall |
|---|---:|---:|---:|
| Logistic Regression | 69.38% | 79.82% | 58.80% |
| Random Forest | 70.64% | 75.17% | **69.07%** |
| Decision Tree | 70.66% | 77.11% | 65.82% |

Although the Decision Tree produced a marginally higher accuracy score, the **Random Forest Classifier was selected as the preferred model** because it provided the strongest balance between precision and recall.

Most importantly, it achieved the **highest recall**, allowing it to identify approximately 7 out of every 10 actual late deliveries.

---

## Recommended Model

### Random Forest Classifier

The Random Forest model achieved approximately:

- **70.6% accuracy**
- **75.2% precision**
- **69.1% recall**

For this business problem, the higher recall makes the model particularly useful because identifying potentially late orders is more valuable than simply maximizing overall accuracy.

---

## Business Impact

A model like this could support supply chain operations by helping teams:

- Flag high-risk orders for priority handling
- Notify customers proactively when delays are likely
- Review and optimize shipping-mode selection
- Allocate operational resources toward orders requiring attention
- Improve overall delivery performance

The model should be viewed as a decision-support tool rather than a replacement for operational judgment.

---

## Key Takeaways

This project demonstrates my ability to:

- Clean and preprocess large datasets using Python
- Perform exploratory data analysis
- Translate business problems into analytical questions
- Work with numerical and categorical variables
- Conduct correlation and feature-selection analysis
- Build classification models using Scikit-learn
- Compare models using appropriate performance metrics
- Translate model results into practical business recommendations

---

## Repository Contents

`SupplyChain_Analysis.ipynb`

The Jupyter Notebook contains the complete analysis, including data preparation, exploratory analysis, visualizations, feature engineering, modelling, evaluation, and conclusions.

`README.md`

Provides an overview of the business problem, methodology, results, and business implications.

---

## How to Run the Project

1. Clone this repository.
2. Open `SupplyChain_Analysis.ipynb` in Jupyter Notebook or JupyterLab.
3. Ensure the required Python libraries are installed:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
