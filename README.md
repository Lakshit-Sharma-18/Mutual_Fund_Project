# Mutual Fund Analytics Project

## 📌 Project Overview

This project focuses on analyzing mutual fund datasets to derive meaningful insights regarding fund performance, investor behavior, SIP inflows, portfolio holdings, and benchmark indices.

The project uses Python, Pandas, APIs, and Jupyter Notebook for data ingestion, validation, and exploratory analysis.

---

## 🎯 Objectives

- Load and explore mutual fund datasets.
- Fetch live NAV data using MFAPI.
- Perform initial data quality checks.
- Validate dataset consistency using AMFI codes.
- Prepare datasets for further analysis and dashboard development.

---

## 🛠️ Technologies Used

- Python
- Pandas
- Requests
- Jupyter Notebook
- VS Code
- Git & GitHub

---

## 📂 Project Structure

```text
Mutual_Fund_Project/
│
├── dashboard/
├── data/
│   ├── raw/
│   └── processed/
│
├── md files/
│   ├── MUTUAL_FUND_NOTES.md
│   ├── summary.md
│   └── todo.md
│
├── notebooks/
│   ├── data_ingestion.ipynb
│   ├── live_nav_fetch.py
│   └── requirements.txt
│
├── reports/
├── sql/
└── README.md
```

---

## ✅ Work Completed (Day 1)

### 1. Project Setup

- Created the required folder structure.
- Set up the development environment in VS Code.
- Installed required Python libraries.

### 2. Data Ingestion

- Loaded all provided CSV datasets using Pandas.
- Explored dataset dimensions using `.shape`.
- Inspected data types using `.dtypes`.
- Viewed sample records using `.head()`.
- Explored dataset columns.

### 3. Live NAV Fetch using API

Integrated MFAPI to fetch live NAV data for selected mutual fund schemes.

### Funds Fetched

- HDFC Top 100 Direct
- SBI Bluechip Fund
- ICICI Prudential Bluechip Fund
- Nippon India Large Cap Fund
- Axis Bluechip Fund
- Kotak Bluechip Fund

### API Workflow

- Sent API requests using the Requests library.
- Parsed JSON responses.
- Converted API responses into Pandas DataFrames.
- Saved fetched data as CSV files.

---

## 📊 Dataset Exploration

Performed exploratory analysis on the `fund_master` dataset:

- Identified unique fund houses.
- Identified unique categories.
- Identified unique sub-categories.
- Identified unique risk categories.
- Explored AMFI scheme codes.

---

## 🔍 Data Validation

- Validated AMFI scheme codes between `fund_master` and `nav_history`.
- Confirmed dataset consistency.

---

## 📈 Data Quality Assessment

Performed initial data quality checks:

- Checked datasets for missing values.
- Checked datasets for duplicate records.
- Identified missing values in the `yoy_growth_pct` column of the SIP inflow dataset.
- No major duplicate issues were found.

---

## 📚 Key Learnings

During this phase, the following concepts were learned:

- Working with REST APIs.
- Parsing JSON data.
- Data ingestion using Pandas.
- Data validation techniques.
- Mutual fund concepts such as:
  - NAV (Net Asset Value)
  - AMFI Codes
  - Fund Houses
  - Risk Categories

---

## 🚀 Next Steps

- Data Cleaning
- Exploratory Data Analysis (EDA)
- SQL Analysis
- Data Visualization
- Dashboard Development using Power BI

---

## 👨‍💻 Author

**Lakshit Sharma**
