# DAY 2 — Data Cleaning + SQL Database Design

## Setup & Preparation

- [X] Pull latest code from GitHub.

- [X] Open project in VS Code/Jupyter Notebook.

- [X] Verify all raw CSV files are present.

- [X] Create folders if not already present:
      data/processed/, sql/, docs/

---

## Data Cleaning

### NAV History Cleaning (`nav_history.csv`)

- [X] Load dataset using Pandas.

- [X] Print .shape for dataset.

- [X] Print .dtypes for dataset.

- [X] Print .head() for dataset.

- [X] Convert date column to datetime.

- [X] Sort data by amfi_code and date.

- [X] Remove duplicate rows.

- [X] Forward fill missing NAV values.

- [X] Validate NAV > 0.

- [X] Check for missing values.

- [X] Save cleaned CSV.

---

### Investor Transactions Cleaning (`investor_transactions.csv`)

- [X] Load dataset.

- [X] Standardize transaction_type values.

- [X] Convert date columns to datetime.

- [X] Validate amount > 0.

- [X] Validate KYC status values.

- [X] Handle missing values.

- [X] Remove duplicates.

- [X] Save cleaned CSV.

---

### Scheme Performance Cleaning (`scheme_performance.csv`)

- [X] Load dataset.

- [X] Convert return columns to numeric.

- [X] Check for anomalies in returns.

- [X] Validate expense_ratio range (0.1% - 2.5%).

- [X] Flag suspicious rows.

- [X] Handle missing values.

- [X] Save cleaned CSV.

---

## Database Design

### Star Schema Design

- [X] Design dim_fund table.

- [x] Design dim_date table.

- [x] Design fact_nav table.

- [x] Design fact_transactions table.

- [x] Design fact_performance table.

- [x] Design fact_aum table.

---

## SQL Schema

- [X] Create schema.sql file.

- [X] Write CREATE TABLE statements.

- [X] Define Primary Keys.

- [X] Define Foreign Keys.

- [X] Review schema relationships.

---

## SQLite Database Loading

- [X] Create SQLite database (bluestock_mf.db).

- [x] Create SQLAlchemy engine.

- [X] Load cleaned datasets using df.to_sql().

- [X] Verify row counts for every table.

- [X] Ensure DB rows match CSV rows.

---

## Analytical SQL Queries

- [X] Create queries.sql file.

- [X] Write query: Top 5 funds by AUM.

- [X] Write query: Average NAV per month.

- [X] Write query: SIP YoY growth.

- [X] Write query: Transactions by state.

- [X] Write query: Funds with expense ratio < 1%.

- [X] Write 5 additional analytical queries.

---

## Documentation

- [X] Create data_dictionary.md.

- [X] Document all column names.

- [X] Document data types.

- [X] Document business definitions.

- [X] Document source references.

---

## Validation & Quality Check

- [X] Verify all cleaned CSVs are generated.

- [X] Verify schema.sql works correctly.

- [X] Verify all SQL queries execute successfully.

- [X] Verify database loads successfully.

---

## Git

- [X] Commit changes:
      "Day 2: Cleaned data + SQLite DB loaded"

- [X] Push changes to GitHub.

---

## Deliverables

- [X] 10 cleaned CSVs completed.

- [X] bluestock_mf.db completed.

- [X] schema.sql completed.

- [X] queries.sql completed.

- [X] data_dictionary.md completed.

- [X] GitHub push completed.