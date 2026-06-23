# DAY 1 — Project Setup + Data Ingestion (ETL)

## Setup & Structure

- [X] Create project folder structure:
      data/raw, data/processed, notebooks/, sql/, dashboard/, reports/

- [X] Initialize Git repo.

- [X] Push repository to GitHub.

- [X] Install dependencies:
      pandas, numpy, matplotlib, seaborn, plotly,
      sqlalchemy, requests, scipy, jupyter

- [X] Create requirements.txt

## Data Ingestion

- [X] Load all 10 CSV datasets using Pandas.

- [X] Print .shape for each dataset.

- [X] Print .dtypes for each dataset.

- [X] Print .head() for each dataset.

- [X] Note anomalies in datasets.

## Live NAV Fetch

- [X] Fetch live NAV from mfapi.in for HDFC Top 100 Direct (125497).

- [X] Parse JSON response.

- [X] Save response as raw CSV.

- [X] Fetch NAV for SBI Bluechip (119551).

- [X] Fetch NAV for ICICI Bluechip (120503).

- [X] Fetch NAV for Nippon Large Cap (118632).

- [X] Fetch NAV for Axis Bluechip (119092).

- [X] Fetch NAV for Kotak Bluechip (120841).

## Fund Master Exploration

- [X] Print unique fund houses.

- [X] Print unique categories.

- [X] Print unique sub-categories.

- [X] Print unique risk grades.

- [X] Understand AMFI scheme code structure.

## Validation & Quality Check

- [X] Validate AMFI codes between fund_master and nav_history.

- [ ] Write short data quality summary.

## Git

- [ ] Commit changes:
      "Day 1: Data ingestion complete"

## Deliverables

- [X] data_ingestion.py completed.

- [X] live_nav_fetch.py completed.

- [X] requirements.txt completed.

- [ ] GitHub repository pushed with Day 1 commit.