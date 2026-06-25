# Data Dictionary - Mutual Fund Analytics Project

## Overview

This document describes the structure, data types, business meanings, and source references of all datasets used in the Mutual Fund Analytics Project.

---

# 1. dim_fund

**Description:** Contains master information about mutual fund schemes.

| Column Name        | Data Type | Business Definition                                                    |
| ------------------ | --------- | ---------------------------------------------------------------------- |
| amfi_code          | INTEGER   | Unique identifier assigned by AMFI to each mutual fund scheme.         |
| fund_house         | TEXT      | Name of the asset management company (AMC).                            |
| scheme_name        | TEXT      | Name of the mutual fund scheme.                                        |
| category           | TEXT      | Broad category of the scheme (Equity, Debt, Hybrid, etc.).             |
| sub_category       | TEXT      | Detailed classification within the category.                           |
| plan               | TEXT      | Indicates whether the scheme is Direct or Regular.                     |
| launch_date        | DATE      | Date on which the scheme was launched.                                 |
| benchmark          | TEXT      | Benchmark index used for performance comparison.                       |
| expense_ratio_pct  | REAL      | Annual expense ratio charged by the fund (%).                          |
| exit_load_pct      | REAL      | Charges applied when units are redeemed before a specified period (%). |
| min_sip_amount     | REAL      | Minimum amount required to start a SIP.                                |
| min_lumpsum_amount | REAL      | Minimum one-time investment amount.                                    |
| fund_manager       | TEXT      | Name of the fund manager responsible for managing the scheme.          |
| risk_category      | TEXT      | Risk classification assigned to the scheme.                            |
| sebi_category_code | TEXT      | SEBI classification code for the scheme.                               |

**Source File:** `01_fund_master.csv`

---

# 2. fact_nav

**Description:** Stores historical Net Asset Value (NAV) records for mutual fund schemes.

| Column Name | Data Type | Business Definition                               |
| ----------- | --------- | ------------------------------------------------- |
| amfi_code   | INTEGER   | Unique scheme identifier.                         |
| date        | DATE      | NAV reporting date.                               |
| nav         | REAL      | Net Asset Value of the scheme on a specific date. |

**Source File:** `02_nav_history.csv`

---

# 3. fact_transactions

**Description:** Stores investor transaction details.

| Column Name        | Data Type | Business Definition                                     |
| ------------------ | --------- | ------------------------------------------------------- |
| investor_id        | TEXT      | Unique identifier of the investor.                      |
| amfi_code          | INTEGER   | Scheme identifier.                                      |
| date               | DATE      | Transaction date.                                       |
| transaction_type   | TEXT      | Purchase, Redemption, SIP, etc.                         |
| amount_inr         | REAL      | Transaction amount in Indian Rupees.                    |
| state              | TEXT      | State of the investor.                                  |
| city               | TEXT      | City of the investor.                                   |
| city_tier          | TEXT      | Tier classification of the city (Tier 1, Tier 2, etc.). |
| age_group          | TEXT      | Age bracket of the investor.                            |
| gender             | TEXT      | Gender of the investor.                                 |
| annual_income_lakh | REAL      | Investor annual income in lakhs.                        |
| payment_mode       | TEXT      | Mode of payment used.                                   |
| kyc_status         | TEXT      | Indicates whether KYC is completed.                     |

**Source File:** `08_investor_transactions.csv`

---

# 4. fact_performance

**Description:** Contains scheme performance and risk metrics.

| Column Name        | Data Type | Business Definition                                |
| ------------------ | --------- | -------------------------------------------------- |
| amfi_code          | INTEGER   | Scheme identifier.                                 |
| return_1yr_pct     | REAL      | Annual return over the last 1 year (%).            |
| return_3yr_pct     | REAL      | Annualized return over the last 3 years (%).       |
| return_5yr_pct     | REAL      | Annualized return over the last 5 years (%).       |
| benchmark_3yr_pct  | REAL      | 3-year benchmark return (%).                       |
| alpha              | REAL      | Risk-adjusted excess return generated by the fund. |
| beta               | REAL      | Volatility of the fund relative to the benchmark.  |
| sharpe_ratio       | REAL      | Risk-adjusted return metric.                       |
| sortino_ratio      | REAL      | Downside risk-adjusted return metric.              |
| std_dev_ann_pct    | REAL      | Annualized standard deviation of returns.          |
| max_drawdown_pct   | REAL      | Maximum observed loss from peak to trough (%).     |
| aum_crore          | REAL      | Assets Under Management in crores.                 |
| expense_ratio_pct  | REAL      | Annual expense ratio (%).                          |
| morningstar_rating | INTEGER   | Morningstar rating assigned to the scheme.         |
| risk_grade         | TEXT      | Overall risk classification.                       |

**Source File:** `07_scheme_performance.csv`

---

# 5. fact_aum

**Description:** Stores AUM information at the fund house level.

| Column Name    | Data Type | Business Definition                             |
| -------------- | --------- | ----------------------------------------------- |
| fund_house     | TEXT      | Name of the asset management company.           |
| aum_lakh_crore | REAL      | Assets Under Management measured in lakh crore. |
| aum_crore      | REAL      | Assets Under Management measured in crore.      |
| num_schemes    | INTEGER   | Number of schemes managed by the AMC.           |

**Source File:** `03_aum_by_fund_house.csv`

---

# 6. fact_sip_inflows

**Description:** Contains monthly SIP inflow statistics.

| Column Name               | Data Type | Business Definition                              |
| ------------------------- | --------- | ------------------------------------------------ |
| month                     | TEXT      | Reporting month in YYYY-MM format.               |
| sip_inflow_crore          | REAL      | Total SIP inflow during the month (₹ crore).     |
| active_sip_accounts_crore | REAL      | Number of active SIP accounts (crore).           |
| new_sip_accounts_lakh     | REAL      | Number of newly opened SIP accounts (lakh).      |
| sip_aum_lakh_crore        | REAL      | SIP assets under management (lakh crore).        |
| yoy_growth_pct            | REAL      | Year-over-Year growth percentage of SIP inflows. |

**Source File:** `04_monthly_sip_inflows.csv`

---

# Source References

| Dataset                   | Source                                            |
| ------------------------- | ------------------------------------------------- |
| Mutual Fund Scheme Data   | AMFI (Association of Mutual Funds in India)       |
| NAV Data                  | MFAPI / AMFI Historical NAV Data                  |
| SIP Statistics            | AMFI Monthly Reports                              |
| AUM Data                  | AMFI Industry Reports                             |
| Benchmark Data            | NSE/BSE Benchmark Indices                         |
| Investor Transaction Data | Synthetic Dataset Generated for Analytics Project |

---
