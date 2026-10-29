# Customer Churn Analysis using Python & SQL

## Project Overview

Customer churn is an important business challenge because losing existing customers can affect revenue and long-term business growth.

This project focuses on analyzing customer subscription data to understand churn patterns, identify customer segments with higher churn rates, and explore factors associated with customer retention.

Using Python, SQL, and exploratory data analysis (EDA), I worked with customer, subscription, and customer-support datasets to derive meaningful business insights.

## Business Objectives

- Calculate overall customer churn and retention rates.
- Identify subscription plans with higher customer churn.
- Analyze churn patterns across customer locations and acquisition channels.
- Understand the relationship between customer-support escalations and churn.
- Calculate average revenue per user and monthly charges associated with churned customers.
- Identify potential areas where customer retention strategies could be improved.

## Tools & Technologies

- **Python:** Data analysis and feature engineering
- **Pandas & NumPy:** Data manipulation and cleaning
- **Matplotlib & Seaborn:** Data visualization
- **SQLite & SQL:** Database connection and data extraction
- **Jupyter Notebook:** Analysis environment

## Project Workflow

1. **SQL Data Extraction:** Connected to an SQLite database and extracted three tables: customer, subscription, and support.

2. **Data Cleaning:** Handled missing values, removed irrelevant columns, standardized gender categories, and converted date columns into appropriate datetime formats.

3. **Data Integration:** Combined customer, subscription, and support information using customer IDs.

4. **Feature Engineering:** Created new features such as churn flag, customer tenure, and churn-risk categories.

5. **Exploratory Data Analysis:** Examined churn across subscription plans, subscription sources, and states.

6. **Business Metrics:** Calculated churn rate, retention rate, ARPU, average tenure, revenue at risk, and support escalation rate.

7. **Data Visualization:** Used Matplotlib and Seaborn to explore trends, distributions, and relationships between variables.

## Key Business Insights

The analysis produced the following results from the available sample of 21 customer records:

| Business Metric | Result |
|---|---:|
| Customer Churn Rate | 28.57% |
| Customer Retention Rate | 71.43% |
| Average Revenue Per User | 18.85 |
| Average Customer Tenure | 1,512 days |
| Monthly Charges of Churned Customers | 73.94 |
| Support Escalation Rate | 19.05% |

### 1. Churn by Subscription Plan

- Basic Plan recorded the highest churn rate at 60%.
- Standard Plan recorded a churn rate of 22.22%.
- Premium Plan recorded the lowest churn rate at 14.29%.

**Business implication:** The Basic Plan may require further investigation into pricing, service quality, and customer satisfaction.

### 2. Churn by Subscription Source

- Referral: 83.33%
- Paid: 16.67%
- Organic: 0%

**Business implication:** Referral customers show a notably higher churn rate in this sample. The business should investigate the quality and expectations of customers acquired through referrals.

### 3. Customer Support Analysis

The notebook reports a correlation of 0.77 between support escalations and churn.

**Business implication:** Support escalations may be worth investigating as a potential customer-retention signal. This relationship requires validation using correctly encoded data and a larger sample.

### 4. Revenue Analysis

Monthly charges associated with churned customers total 73.94.

**Business implication:** Retaining customers who are at risk of cancellation could help protect recurring subscription revenue.

## Skills Demonstrated

- SQL database connectivity and data extraction
- Data cleaning and preprocessing
- Missing-value handling
- Data type conversion and standardization
- Data merging and integration
- Feature engineering
- Exploratory data analysis
- Statistical correlation analysis
- Business KPI calculation
- Data visualization
- Business insight generation

## Project Limitations

- The available dataset contains only 21 customer records.
- Findings are exploratory and should not be generalized to a larger customer population.
- The correlation analysis requires validation.
- This project focuses on descriptive analysis and does not currently include a trained machine learning churn-prediction model.

## Conclusion

This project demonstrates how Python and SQL can be used together to transform raw customer data into meaningful business insights. The analysis highlights customer segments with higher observed churn, subscription-source patterns, and customer-support indicators that can guide further retention analysis.

## Repository Structure

```text
customer-churn-analysis-python-sql/
│
├── README.md
├── customer_churn_analysis.ipynb
├── data/
│   └── exported_churn_data.csv
├── images/
│   ├── churn_by_plan.png
│   ├── churn_by_state.png
│   └── correlation_heatmap.png
└── requirements.txt
```

## How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries.
3. Open the Jupyter Notebook.
4. Ensure the SQLite database is available at the expected path.
5. Run the notebook cells sequentially.

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---

**Author:** Data Analytics Portfolio Project  
**Focus:** Customer Churn | Python | SQL | Exploratory Data Analysis
