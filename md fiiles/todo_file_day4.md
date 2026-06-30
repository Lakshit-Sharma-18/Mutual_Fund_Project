# 📊 Fund Performance Analytics - TODO List

## 🎯 Objective
Perform advanced performance analytics on all mutual fund schemes and generate comparative performance metrics.

---

## 1. Daily Return Analysis

- [x] Compute daily returns for all 40 schemes.
- [X] Use the formula:
      daily_return = (NAV_t / NAV_t-1) - 1

- [X] Validate whether the return distribution looks reasonable.
- [X] Perform exploratory analysis on daily returns.

---

## 2. CAGR (Compound Annual Growth Rate) Analysis

- [X] Compute CAGR for:
  - [X] 1 Year CAGR
  - [X] 3 Year CAGR
  - [X] 5 Year CAGR

- [X] Use the formula:

      CAGR = (NAV_end / NAV_start)^(1/n) - 1

- [X] Create a comparison table for all mutual funds.

---

## 3. Sharpe Ratio Analysis

- [X] Calculate Sharpe Ratio for all funds.

- [X] Use the formula:

      Sharpe Ratio = (Rp - Rf) / Std(Rp) × √252

Where:
- Rp = Portfolio Return
- Rf = Risk Free Rate (6.5%)
- Std(Rp) = Standard Deviation of Returns

- [X] Use Risk Free Rate (Rf) = 6.5%.
- [X] Rank all 40 funds based on Sharpe Ratio.

---

## 4. Sortino Ratio Analysis

- [X] Calculate Sortino Ratio for all funds.

- [X] Use the same formula as Sharpe Ratio.

- [X] Use only downside deviation:

      Downside Deviation = Std(Negative Returns)

- [X] Rank all funds based on Sortino Ratio.

---

## 5. Alpha & Beta Calculation

- [X] Calculate Alpha and Beta for each fund.
- [X] Use OLS Regression.
- [X] Use Nifty 100 returns as benchmark.
- [X] Use:  

      scipy.stats.linregress()

- [X] Compute Alpha:

      Alpha = Intercept × 252

- [X] Store results in a separate dataframe.

---

## 6. Maximum Drawdown Analysis

- [X] Compute Maximum Drawdown for all funds.

- [X] Use the formula:

      Max Drawdown = min(NAV / Running_Max - 1)

- [X] Identify:
  - [X] Worst drawdown value
  - [X] Drawdown start date
  - [X] Drawdown end date

---

## 7. Fund Scorecard Creation

Create a composite score (0-100).

### Weightage

- [X] 30% → 3 Year Return Rank
- [X] 25% → Sharpe Ratio Rank
- [X] 20% → Alpha Rank
- [X] 15% → Expense Ratio Rank (Inverse)
- [X] 10% → Maximum Drawdown Rank (Inverse)

- [X] Calculate final score for all funds.
- [X] Rank all funds based on composite score.

---

## 8. Benchmark Comparison

- [X] Select Top 5 performing funds.
- [x] Compare against:
  - [x] Nifty 50
  - [x] Nifty 100

- [x] Plot benchmark comparison chart for last 3 years.

- [x] Calculate Tracking Error:

      Tracking Error = Std(Fund Return - Benchmark Return) × √252

---

## 📦 Deliverables

- [X] Create `Performance_Analytics.ipynb`
- [X] Export `fund_scorecard.csv`
- [X] Export `alpha_beta.csv`
- [X] Export Benchmark Comparison Chart as PNG

---

## ✅ Completion Tracker

- [X] Daily Returns Completed
- [X] CAGR Analysis Completed
- [X] Sharpe Ratio Completed
- [X] Sortino Ratio Completed
- [X] Alpha & Beta Completed
- [X] Maximum Drawdown Completed
- [X] Fund Scorecard Completed
- [X] Benchmark Comparison Completed
- [X] Deliverables Exported
- [X] Final Submission Ready