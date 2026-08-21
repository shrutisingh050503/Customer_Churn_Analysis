# Customer_Churn_Analysis

Project Overview

This project analyzes customer churn to understand customer behavior, identify factors associated with churn, and derive actionable insights from customer, subscription, and support data.

The analysis was performed using Python, Pandas, NumPy, Matplotlib, Seaborn, and SQL/SQLite in Jupyter Notebook.

The project combines customer information with subscription and customer-support data to study churn from multiple perspectives.

Objectives
Calculate the overall customer churn rate.
Analyze churn across different customer segments.
Compare churn by plan type and state.
Analyze customer subscription and contract information.
Calculate customer tenure.
Analyze monthly churn trends.
Create a churn risk category using churn scores.
Analyze customer complaints and escalations.
Study the relationship between support escalations and customer churn.
Perform data encoding and correlation analysis.
Generate visualizations to communicate findings.

Dataset Structure

The project works with three SQLite tables:

db_customer

Contains customer-level information:

customerid
name
country
state
gender
dob
interests
pincode

db_subscription

Contains subscription-related information:

customerid
subscription_start_date
subscription_type
renewal_date
plan_type
contract_type
cancellation_date
cancellation_reason
monthly_charges
cltv
churn_score

db_support

Contains customer-support information:

customerid
complaint_date
escalations
csat_score
col_1
comment

These three tables were explored and combined for the churn analysis.

Tools & Technologies
Python
Jupyter Notebook
Pandas
NumPy
Matplotlib
Seaborn
SQLite
SQL

Project Workflow
1. Data Extraction

The project uses SQLite to connect to the customer churn database and inspect the available tables and columns.

SQL was used to explore and aggregate data before performing further analysis in Pandas.

2. Data Cleaning & Preparation

The data was prepared for analysis by:

Converting date columns to datetime format.
Checking dataframe structure and data types.
Handling missing values.
Combining customer, subscription, and support information.
Creating analysis-ready columns.

The subscription date fields were converted using pd.to_datetime().

3. Feature Engineering

Several new variables were created to support the analysis:

churn_flag
tenure_days
escalation
churn_risk
cancellation_month
complaint_count

The churn_flag identifies customers based on whether they have a cancellation date.

Customer tenure was calculated using the subscription start date and cancellation date, or the current date for customers who had not cancelled.

Key Analysis
Overall Churn Rate

The overall churn rate calculated in the project is:

28.57%

The churn rate was calculated using the mean of the binary churn_flag.

Monthly Churn Trend

A monthly churn trend was created by extracting the month from cancellation_date and counting churned customers for each cancellation month.

📦 Churn by Plan Type

The project analyzes churn across different subscription plans:

Basic
Standard
Premium

Plan type was also treated as an ordered categorical variable during encoding

Churn by State

Churn was analyzed geographically by calculating the average churn_flag for each state. This helps identify states with relatively higher or lower churn levels.

⚠️ Churn Risk Classification

Customers were classified into three churn-risk categories using their churn_score:

Churn Score	Risk Level
< 50	Low
50–69	Medium
≥ 70	High

The project creates the churn_risk feature using these thresholds.

Customer Support Analysis

Customer-support information was incorporated into the analysis through:

Complaint dates
Complaint counts
Escalations
CSAT scores

The project calculates an average of approximately 0.43 complaints per user.

Escalation vs Churn

The project investigates whether customer-support escalations are associated with churn.

The calculated correlation between escalation and churn_flag is:

0.77

This indicates a strong positive association in this dataset.

Note: Correlation indicates association, not causation.

Visualizations

The project uses visualizations to communicate:

Monthly churn trends
Churn by state
Churn by plan type
Customer churn risk
Other customer and subscription patterns

Matplotlib is used for the visualization stage of the analysis.

Key Findings

Based on the analysis performed in the notebook:

The overall customer churn rate is 28.57%.
Customers are segmented into low, medium, and high churn-risk groups using churn scores.
Churn is analyzed across both geographical and subscription dimensions.
Customer-support interactions are incorporated through complaints, escalations, and CSAT.
The analysis found a 0.77 correlation between escalations and churn, suggesting that escalated support interactions are strongly associated with churn in this dataset.
Customer tenure was engineered to understand the length of customer relationships.

Business Insights

The analysis can help a business:

Identify customers who may require retention efforts.
Monitor high-risk customers using churn scores.
Investigate regions with higher churn.
Evaluate differences between subscription plans.
Pay closer attention to customers with escalated support interactions.
Use customer-support data as an additional signal when evaluating churn risk.

Project Structure
customer-churn-analysis/
│
├── customer_churn.ipynb
├── customer_churn.db
├── README.md
└── requirements.txt

How to Run the Project
Clone or download this repository.
Install the required Python libraries.
Open the Jupyter Notebook.
Make sure the SQLite database is available in the expected location.
Run the notebook cells sequentially.
Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

Project Type

Data Analysis / Customer Churn Analysis

This project demonstrates practical skills in:

SQL → Data Extraction → Data Cleaning → Feature Engineering → Exploratory Data Analysis → Visualization → Correlation Analysis → Business Insights

