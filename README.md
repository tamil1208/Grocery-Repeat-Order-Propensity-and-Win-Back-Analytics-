# Grocery Repeat Order Propensity & Win-Back Analytics

An end-to-end customer analytics project focused on understanding customer churn and retention behaviour, exploring customer lifetime patterns, and identifying opportunities for targeted win-back campaigns.

> **Project status:** The repository currently contains exploratory data analysis and customer survival analysis notebooks built around the IBM Telco Customer Churn dataset. The grocery repeat-order and win-back framing is the intended business use case; grocery-specific transaction features and a repeat-order propensity model are not yet present in the current notebooks.

---

## Project Overview

Customer retention is important for subscription businesses and grocery retailers alike. In grocery commerce, understanding when customers become inactive, which customer groups are more likely to leave, and when to re-engage them can help businesses improve repeat purchases and protect customer lifetime value.

This project explores customer-level behaviour using exploratory analysis and survival analysis. The analytical workflow provides a foundation for a future grocery-focused solution that can estimate repeat-order propensity, identify customers at risk of becoming inactive, and prioritize win-back campaigns.

## Business Problem

A grocery business wants to improve repeat purchases and reduce customer inactivity. However, it may not know:

- Which customer characteristics are associated with churn or reduced engagement?
- How does customer tenure relate to the likelihood of remaining active?
- Which customer segments may need earlier retention interventions?
- How can customer behaviour analysis inform targeted win-back campaigns?

**Goal:** Use customer analytics to understand retention patterns and develop a framework for prioritizing customers for repeat-purchase and win-back initiatives.

## Current Repository Contents

| File | Description |
|---|---|
| `Exploratory Data Analysis.ipynb` | Loads and explores customer data, reviews data quality, and performs initial churn analysis. |
| `Customers Survival Analysis.ipynb` | Introduces survival analysis and applies Kaplan–Meier and Cox proportional hazards methods. |
| `LICENSE` | MIT License. |

## Dataset

The notebooks currently use the **IBM Telco Customer Churn** dataset. It contains customer-level service, tenure, billing, and churn information.

Example fields include:

| Feature | Description |
|---|---|
| `customerID` | Unique customer identifier |
| `gender` | Customer gender |
| `SeniorCitizen` | Senior-citizen indicator |
| `Partner`, `Dependents` | Household-related attributes |
| `tenure` | Number of months with the service |
| `Contract` | Contract type |
| `MonthlyCharges` | Monthly customer charges |
| `TotalCharges` | Total charges over the customer relationship |
| `Churn` | Whether the customer has churned |

**Important:** These are telecom customer records, not grocery order histories. The current dataset does not include order dates, basket contents, product categories, order frequency, or days since last purchase. Therefore, it cannot directly calculate grocery repeat-order rates or train a valid grocery repeat-order propensity model.

For a genuine grocery implementation, replace or supplement the current dataset with order-level records containing a customer ID, order ID, order date, order value, product/category details, and customer activity history.

## Analysis Workflow

### 1. Data Loading and Preparation
- Load the customer dataset using Pandas.
- Inspect rows, columns, data types, and sample records.
- Check missing values and data consistency.
- Review identifiers and select relevant analytical features.

### 2. Exploratory Data Analysis
- Examine customer and service characteristics.
- Explore tenure, contract type, and billing patterns.
- Compare customer attributes across churn groups.
- Use visualizations to identify patterns and potential retention signals.

### 3. Customer Survival Analysis
Survival analysis helps investigate **time until an event occurs**. In this project, the event is customer churn and the observed duration is customer tenure.

Methods included in the notebook:
- **Kaplan–Meier estimator:** estimates the customer survival function over time.
- **Log-rank test:** compares survival distributions between customer groups.
- **Cox proportional hazards model:** evaluates how selected customer characteristics relate to churn hazard.

The survival-analysis notebook uses the `lifelines` library.

### 4. Business Interpretation
Translate observed patterns into retention questions:
- Which customer groups show shorter observed relationships?
- At what stages of tenure might retention outreach be useful?
- Which customer attributes are associated with higher churn hazard?
- What additional data is needed to design a grocery win-back strategy?

## Tools and Technologies

- **Python** – analytical programming
- **Pandas, NumPy** – data loading and manipulation
- **Matplotlib, Seaborn** – exploratory visualizations
- **SciPy, Statsmodels** – statistical analysis
- **Scikit-learn** – preprocessing utilities
- **Lifelines** – survival analysis
- **Jupyter Notebook** – interactive analysis environment

## Getting Started

### Prerequisites

Install Python 3.9 or later, then install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels scikit-learn lifelines jupyter
```

### Clone the repository

```bash
git clone https://github.com/tamil1208/Grocery-Repeat-Order-Propensity-and-Win-Back-Analytics-.git
cd Grocery-Repeat-Order-Propensity-and-Win-Back-Analytics-
```

### Run the notebooks

```bash
jupyter notebook
```

Open `Exploratory Data Analysis.ipynb` or `Customers Survival Analysis.ipynb` and update the dataset file path in the notebook to match your local environment.

## Proposed Grocery Analytics Extension

The following stages describe how this work can be extended into a grocery repeat-order and win-back solution. They are **planned extensions**, not completed capabilities in the current notebooks.

| Planned stage | Proposed analysis |
|---|---|
| Customer purchase behaviour | Calculate orders per customer, average order value, and purchase frequency. |
| Recency and inactivity | Measure days since last order and define inactivity windows appropriate to the business. |
| Repeat-order analysis | Identify customers who place another order within a defined observation period. |
| Propensity modelling | Build a classification model using only information available before the prediction date. |
| Customer segmentation | Group customers by recency, frequency, monetary value, and predicted risk. |
| Win-back prioritization | Rank inactive or at-risk customers by expected responsiveness and potential value. |
| Campaign measurement | Compare reactivation, repeat-purchase, revenue, and incremental lift across campaign and control groups. |

### Suggested Grocery Metrics

- **Repeat Purchase Rate:** percentage of eligible customers who place another order within a defined period.
- **Purchase Frequency:** average number of orders per customer in the selected period.
- **Average Order Value (AOV):** total order revenue divided by number of orders.
- **Days Since Last Order:** number of days from the analysis date to a customer's most recent order.
- **Customer Reactivation Rate:** percentage of previously inactive customers who place a new order after a win-back campaign.
- **Win-Back Revenue:** revenue generated by reactivated customers during the measurement window.

Metric definitions should use consistent eligibility rules, observation windows, and customer-level or order-level grains.

## Expected Business Value

A grocery-specific implementation could help a retention or product team:

- Identify customers who may be less likely to order again.
- Time personalized reminders and replenishment nudges.
- Prioritize win-back offers for high-value inactive customers.
- Reduce unnecessary discounts to customers likely to return organically.
- Measure campaign performance using repeat orders and incremental revenue.

These are intended business applications. No campaign lift, revenue improvement, or model-performance result is claimed by the current repository.

## Future Improvements

- Add a grocery transaction dataset with order-level timestamps.
- Build customer-level RFM and repeat-order features.
- Define a repeat-purchase target and prediction horizon.
- Train and evaluate classification models with a time-based validation split.
- Assess precision, recall, F1-score, ROC-AUC, PR-AUC, and calibration.
- Use explainability methods to understand key drivers.
- Build a Power BI or Streamlit dashboard for retention monitoring.
- Run controlled win-back campaign experiments to measure incremental impact.

## Author

**Tamilarasan**

- GitHub: [tamil1208](https://github.com/tamil1208)

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
