#  Customer Churn Analysis

##  Project Overview

This project focuses on analyzing **customer churn** to understand why customers leave a service, which customers are at higher risk of churn, and how customer churn can impact business revenue and customer lifetime value.

The project uses customer, subscription, and support data stored across multiple relational tables. The data was extracted from a **SQLite database** and analyzed using Python. The overall workflow covers **SQL data extraction, data cleaning, feature engineering, exploratory data analysis (EDA), data visualization, KPI analysis, and business recommendations**.

---

##  Business Objective

The main objective of this project was to help identify:

* Customers who are at higher risk of churn
* Subscription plans and contracts with higher churn
* Geographic areas with higher churn
* The relationship between customer support activity and churn
* Revenue affected by customer churn
* Customer Lifetime Value (CLTV) at risk
* Potential strategies to improve customer retention

The analysis was designed to turn raw customer data into **actionable business insights**.

---

##  Tools & Technologies

The project was completed using:

| Tool / Library | Purpose                                      |
| -------------- | -------------------------------------------- |
| **Python**     | Main programming language                    |
| **SQLite3**    | Database connection and SQL data extraction  |
| **Pandas**     | Data manipulation and analysis               |
| **NumPy**      | Numerical operations and feature engineering |
| **Matplotlib** | Data visualization                           |
| **Seaborn**    | Statistical and categorical visualizations   |

The project report specifically identifies NumPy, Pandas, SQLite3, Matplotlib, and Seaborn as the main Python/SQL technologies used.

---

##  Dataset Structure

The project uses three main relational tables from the `customer_churn` database:

### 1. `db_customer`

Contains customer demographic information such as:

* Customer ID
* Name
* Country
* State
* Gender
* Date of Birth
* Interests
* Pincode

### 2. `db_subscription`

Contains subscription-related information such as:

* Customer ID
* Subscription start date
* Subscription type
* Renewal date
* Plan type
* Contract type
* Cancellation date
* Cancellation reason
* Monthly charges
* CLTV
* Churn score

### 3. `db_support`

Contains customer support information such as:

* Customer ID
* Complaint date
* Escalations
* CSAT score
* Comments

The database structure and fields are documented in the project report.

---

##  Project Workflow

The project followed an end-to-end data analytics workflow:

```text
SQLite Database
      ↓
SQL Data Extraction
      ↓
Data Import into Python
      ↓
Data Cleaning & Quality Checks
      ↓
Feature Engineering
      ↓
Exploratory Data Analysis
      ↓
KPI Analysis
      ↓
Data Visualization
      ↓
Business Insights
      ↓
Recommendations
```

---

##  Data Cleaning

The data preparation stage included:

* Checking data types
* Renaming columns where required
* Selecting relevant columns
* Performing quality checks
* Handling missing/null values
* Preparing data for analysis

Pandas and NumPy were used extensively during the cleaning and transformation process.

---

##  Feature Engineering

New calculated fields and transformations were created to support the analysis.

The project included:

* Creating calculated columns
* Data transformation
* Filtering relevant records
* Preparing data for churn and revenue analysis
* Creating analytical features for customer segmentation

Feature engineering was an important step in converting raw database information into analysis-ready data.

---

##  Exploratory Data Analysis

Exploratory Data Analysis was performed using:

* Aggregations
* GroupBy operations
* Pivot tables
* Customer segmentation
* Subscription analysis
* Churn analysis
* Revenue analysis
* Support activity analysis

Visualizations were created using **Matplotlib and Seaborn** to identify important patterns and trends.

---

##  Key KPIs

The analysis focused on several important business KPIs, including:

* Churn Rate
* Retention Rate
* Churn by Plan Type
* Churn by State
* ARPU
* Average Tenure
* Revenue at Risk
* Escalation Rate
* Average Complaints per Customer
* Relationship between escalations and churn

The report defines churn rate as:

```text
Churn Rate = Churned Customers / Total Customers
```

and retention rate as:

```text
Retention Rate = 1 - Churn Rate
```

Other KPIs included ARPU, average tenure, revenue at risk, escalation rate, and complaint-related metrics.

---

##  Key Findings

The analysis produced several important findings:

###  Overall Churn

* **Overall Churn Rate:** 28.6%
* **Retention Rate:** 71.4%

###  Contract Analysis

Monthly-contract customers showed significantly higher churn than annual-contract customers:

| Contract Type | Churn Rate |
| ------------- | ---------: |
| Monthly       |  **55.6%** |
| Annual        |   **8.3%** |

This represents a major difference in retention between the two contract types.

###  Revenue Impact

The analysis identified:

* Approximately **18% revenue loss** associated with churn
* Revenue loss due to churn of approximately **74**
* Approximately **2,047 CLTV lost**
* **$73.94/month MRR leakage** was highlighted for at-risk customers in the portfolio summary

The report also highlighted CLTV erosion among at-risk customers.

###  Geographic Analysis

**Karnataka** was identified as the state with the highest churn concentration.

###  Time-Based Analysis

**September 2024** had the highest churn activity in the analysis.

###  Customer Tenure

The reported average customer tenure was approximately:

**1,451 days**

These findings helped identify areas where the business could focus its retention efforts.

---

##  Business Insights

One of the most important insights from the project was the significant difference between **monthly and annual contract churn**.

Customers on monthly contracts had a much higher churn rate compared with annual-contract customers. This suggests that encouraging suitable customers to move toward longer-term contracts could be an important retention strategy.

The analysis also showed the importance of combining:

* Subscription information
* Customer information
* Support interactions
* Churn risk
* Revenue metrics
* Customer Lifetime Value

to get a more complete picture of customer behavior.

---

##  Project Highlights

This project demonstrates an end-to-end analytics workflow:

**Raw Data → SQL → Python → Cleaning → Feature Engineering → EDA → Visualization → KPIs → Business Insights**

It also demonstrates how multiple relational data sources can be combined to analyze:

* Customer behavior
* Subscription patterns
* Support activity
* Churn risk
* Revenue impact
* Customer Lifetime Value

The project report describes this as an end-to-end churn analytics pipeline for an OTT-style platform, including risk segmentation, MRR leakage, CLTV erosion, and retention strategy.

---

##  Suggested Repository Structure

```text
customer-churn-analysis/
│
├── data/
│   └── customer_churn.db
│
├── notebooks/
│   └── customer_churn_analysis.ipynb
│
├── visualizations/
│   ├── churn_analysis.png
│   ├── contract_analysis.png
│   └── revenue_analysis.png
│
├── report/
│   └── churn_analysis_report.pdf
│
├── README.md
└── requirements.txt
```

> Adjust the folder and file names according to the actual files in your GitHub repository.

---

##  How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/customer-churn-analysis.git
```

### 2. Navigate to the Project Folder

```bash
cd customer-churn-analysis
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

> `sqlite3` is included with standard Python installations, so it normally does not need to be installed separately.

### 4. Open the Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
customer_churn_analysis.ipynb
```

### 5. Run the Notebook

Run the cells sequentially to:

1. Connect to the SQLite database
2. Extract the tables
3. Clean the data
4. Perform feature engineering
5. Analyze churn
6. Generate visualizations
7. Calculate KPIs
8. Review business insights

---

##  Results Summary

| Metric                 |             Result |
| ---------------------- | -----------------: |
| Overall Churn Rate     |          **28.6%** |
| Retention Rate         |          **71.4%** |
| Monthly Contract Churn |          **55.6%** |
| Annual Contract Churn  |           **8.3%** |
| Average Tenure         |     **1,451 days** |
| Revenue Loss           |            **~74** |
| Revenue Loss %         |            **18%** |
| CLTV Lost              |         **~2,047** |
| Highest Churn State    |      **Karnataka** |
| Highest Churn Period   | **September 2024** |

The values above are taken from the project's analysis report.

---

##  What I Learned

Through this project, I practiced:

* Connecting SQL databases with Python
* Writing SQL queries
* Importing SQL data into Pandas
* Data cleaning
* Handling missing values
* Data type management
* Feature engineering
* Filtering and transformation
* GroupBy analysis
* Pivot tables
* KPI calculation
* Exploratory Data Analysis
* Data visualization
* Business-oriented data analysis
* Converting analytical results into recommendations

The project was designed around these core learning objectives.

---


##  Author

**Adnan Qureshi**

This project was created as part of my learning journey in **Data Analytics**, with a focus on Python, SQL, data cleaning, exploratory analysis, visualization, and business insights.

---

## ⭐ Project Takeaway

> **The goal of this project was not just to analyze data, but to turn customer data into meaningful business insights that can support better retention decisions.**

---

