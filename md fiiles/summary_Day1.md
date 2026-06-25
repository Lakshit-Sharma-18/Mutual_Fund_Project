# Mutual Fund Analytics Project - Day 1

## Project Overview

This project focuses on analyzing mutual fund data to derive meaningful insights related to fund performance, investor behavior, SIP inflows, portfolio holdings, and market benchmarks. The project uses Python, Pandas, APIs, and Jupyter Notebook for data ingestion and exploratory analysis.

---

## Objectives

* Understand the structure of mutual fund datasets.
* Perform data ingestion and initial exploration.
* Fetch live NAV data using MFAPI.
* Validate data quality and dataset consistency.
* Build a strong foundation for further analysis and dashboard development.

---

## Work Completed - Day 1

### 1. Project Setup

* Created the required project folder structure.
* Initialized the project environment.
* Installed all necessary dependencies.

### 2. Data Ingestion

* Loaded all provided CSV datasets using Pandas.
* Explored dataset dimensions, column names, and data types.
* Inspected sample records using `.head()`.

### 3. Live NAV Fetch

* Fetched live NAV data for selected mutual fund schemes using MFAPI.
* Parsed JSON responses received from the API.
* Saved the NAV history as CSV files in the raw data folder.

Funds fetched:

* HDFC Top 100 Direct
* SBI Bluechip Fund
* ICICI Prudential Bluechip Fund
* Nippon India Large Cap Fund
* Axis Bluechip Fund
* Kotak Bluechip Fund

### 4. Fund Master Exploration

* Identified unique fund houses.
* Identified unique categories.
* Identified unique sub-categories.
* Identified unique risk categories.
* Explored the AMFI scheme code structure.

### 5. Data Validation

* Validated AMFI scheme codes between `fund_master` and `nav_history` datasets.
* Confirmed consistency between the datasets.

### 6. Data Quality Assessment

* Checked datasets for missing values.
* Checked datasets for duplicate records.
* Identified missing values in the `yoy_growth_pct` column of the SIP inflow dataset.
* No major duplicate issues were observed.

---

## Technologies Used

* Python
* Pandas
* Requests
* Jupyter Notebook
* VS Code
* Git & GitHub

---

## Folder Structure

```text
Mutual_Fund_Project/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── 01_data_ingestion.ipynb
│
├── reports/
├── sql/
├── md files/
│
├── live_nav_fetch.py
├── requirements.txt
└── README.md
```

---

## Conclusion

The initial data ingestion and exploration phase was successfully completed. The datasets were validated, API integration was implemented, and the project is now ready for data cleaning, exploratory data analysis, and dashboard development.
