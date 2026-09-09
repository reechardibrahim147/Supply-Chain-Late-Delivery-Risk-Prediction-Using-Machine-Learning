# Supply Chain Late Delivery Risk Prediction Using Machine Learning

## Project Overview

Late deliveries can increase operating costs, reduce customer satisfaction, and create challenges for supply chain teams trying to manage orders proactively.

In this project, I used **Python and machine learning** to analyze a large supply chain dataset, identify factors associated with late deliveries, and develop a classification model capable of flagging orders at risk of delay.

The project covers the complete analytics workflow:

**Data Cleaning → Exploratory Data Analysis → Feature Engineering → Feature Selection → Machine Learning → Model Evaluation → Business Recommendations**

---

## Key Results

- Analyzed approximately **180,519 supply chain records**
- Worked with **53 original features**
- Cleaned and prepared the dataset for analysis and machine learning
- Compared **Logistic Regression, Random Forest, and Decision Tree** classifiers
- Random Forest achieved approximately **70.6% accuracy**
- Random Forest achieved the highest recall at approximately **69.1%**
- The selected model can identify roughly **7 out of 10 actual late deliveries**
- Recommended Random Forest as the preferred model for proactive delivery-risk identification

---

## Business Problem

The main business question was:

> **Can historical order, customer, shipping, and product information be used to identify orders at risk of late delivery before the delay occurs?**

A reliable prediction model could help supply chain teams:

- Identify high-risk orders earlier
- Prioritize orders requiring intervention
- Improve customer communication
- Make better shipping decisions
- Reduce the operational impact of late deliveries

---

## Dataset

The original supply chain dataset contained approximately:

- **180,519 records**
- **53 original features**

The data included information relating to:

- Customer segments
- Customer locations
- Markets and regions
- Shipping modes
- Scheduled shipment times
- Product prices
- Order quantities
- Discounts
- Order values
- Delivery performance

Following cleaning, preprocessing, and feature selection, the analytical dataset was reduced to the variables most relevant to the analysis.

The target variable was:

**`Late_delivery_risk`**

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Python | Core analysis and modelling |
| Pandas | Data cleaning and manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Exploratory data visualization |
| Scikit-learn | Preprocessing, feature selection and machine learning |
| Jupyter Notebook | Analysis environment |

---

## Data Cleaning & Preparation

The preprocessing stage included:

- Inspecting dataset structure and data types
- Reviewing missing values
- Checking duplicate records
- Examining categorical values for inconsistencies
- Removing unnecessary variables
- Separating numerical and categorical features
- Creating time-related variables
- Preparing the cleaned dataset for analysis

Categorical variables were converted into numerical format using **LabelEncoder** so they could be used in correlation analysis and machine learning models.

The cleaned dataset was also exported for use in subsequent stages of the project.

---

## Exploratory Data Analysis

Exploratory analysis was used to understand patterns associated with late delivery risk.

Areas investigated included:

- Shipping modes
- Customer segments
- Geographic markets
- Scheduled shipping days
- Product and order characteristics
- Late versus on-time delivery patterns

The analysis indicated that **shipping mode was an important factor associated with late-delivery risk**, suggesting that delivery performance varied across shipping methods.

---

## Feature Engineering & Selection

After categorical variables were encoded, I performed correlation analysis to examine relationships between the available features and late delivery risk.

I also used:

**`SelectKBest` with the `f_classif` scoring method**

to identify features with stronger relationships to the target variable.

Feature selection helped reduce unnecessary noise and create a more focused modelling dataset.

---

## Machine Learning Models

Three classification models were developed and compared:

1. **Logistic Regression**
2. **Random Forest Classifier**
3. **Decision Tree Classifier**

The models were evaluated using:

- Accuracy
- Precision
- Recall

For this business problem, **recall was particularly important** because missing an order that will actually arrive late can prevent the business from taking corrective action before the customer is affected.

---

## Model Performance

| Model | Accuracy | Precision | Recall |
|---|---:|---:|---:|
| Logistic Regression | 69.38% | 79.82% | 58.80% |
| Random Forest | 70.64% | 75.17% | **69.07%** |
| Decision Tree | 70.66% | 77.11% | 65.82% |

---

## Recommended Model

### Random Forest Classifier

Although the Decision Tree achieved marginally higher overall accuracy, the **Random Forest Classifier** provided the strongest balance between precision and recall.

Random Forest achieved approximately:

- **70.6% Accuracy**
- **75.2% Precision**
- **69.1% Recall**

The higher recall means the model successfully identifies approximately **7 out of every 10 actual late deliveries**.

For a supply chain operation, this is particularly valuable because identifying potentially delayed orders early allows teams to intervene before the issue reaches the customer.

---

## Business Recommendations

The analysis suggests that a late-delivery prediction model could be used to:

- Flag high-risk orders for priority handling
- Notify customers proactively about potential delays
- Review shipping-mode selection for high-risk orders
- Allocate operational resources to orders requiring intervention
- Support delivery-performance monitoring
- Improve overall customer experience

The model should be used as a **decision-support tool** alongside operational judgment.

---

## Skills Demonstrated

This project demonstrates practical experience in:

- Python for data analytics
- Data cleaning and preprocessing
- Exploratory data analysis
- Data visualization
- Feature engineering
- Categorical encoding
- Correlation analysis
- Feature selection
- Classification modelling
- Model evaluation
- Business problem solving
- Translating analytical results into business recommendations

---

## Repository Contents

### `SupplyChain_Analysis.ipynb`

Contains the full Python analysis, including:

- Data preparation
- Data cleaning
- Exploratory analysis
- Visualizations
- Feature engineering
- Feature selection
- Machine learning models
- Model comparison
- Conclusions and recommendations

### `README.md`

Provides a concise overview of the business problem, methodology, results, and business implications.

---

## How to View the Project

Open `SupplyChain_Analysis.ipynb` to view the complete Python analysis, including data cleaning, exploratory analysis, feature engineering, machine learning models, model evaluation, and business recommendations.

The notebook was developed using Python, Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn.

## Author

**Richard Ibrahim**

Data & Business Analytics Portfolio

[GitHub Profile](https://github.com/reechardibrahim147)
