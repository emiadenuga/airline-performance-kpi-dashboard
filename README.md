# Airline Performance KPI Dashboard (On-Time, Delays, Cancellations)

## Overview
This project builds an executive-facing KPI dashboard to monitor airline operational performance using U.S. DOT / BTS On-Time Performance data. The dashboard enables stakeholders to track reliability trends, identify underperforming carriers/airports/routes, and prioritize operational improvements.

---

## Business Context
Airline leadership needs a consistent view of operational reliability to understand:
- On-time performance trends over time
- Delay and cancellation risk by carrier, airport, and route
- Severe delay hotspots and seasonal patterns

The objective is to create a KPI reporting layer that supports fast decision-making.

---

## Key Questions
- Which carriers have the highest delay and cancellation rates?
- Which airports/routes are most operationally risky?
- How does on-time performance change by month/season?
- Where are severe delays most concentrated?

---

## Dataset
Source: U.S. DOT / Bureau of Transportation Statistics (BTS) On-Time Performance.
- Portal: https://www.transtats.bts.gov/ontime/
- Data is commonly downloaded month-by-month and combined for a full year.

> Note: Raw source files are not included here. See `/data/raw/README.md` for download notes.

---

## KPI Definitions
- **On-time rate:** % of flights arriving within 15 minutes of scheduled time
- **Delay rate:** % of flights with arrival delay > 15 minutes
- **Cancellation rate:** % of flights marked cancelled
- **Avg delay minutes:** average arrival delay minutes (excluding cancellations)
- **Severe delay rate:** % of flights with delay > 30 (or 60) minutes

(Adjust thresholds in analysis if needed; document changes in `docs/executive_summary.md`.)

---

## Project Workflow

### 1) Data Preparation
Notebook: `notebooks/01_data_preparation.ipynb`
- Standardizes dates and key fields
- Handles cancellations/diversions consistently
- Engineers flags (delayed, severe delay) and route keys
- Outputs: `/data/processed/airline_performance_clean.csv`

### 2) KPI Analysis
Notebook: `notebooks/02_kpi_analysis.ipynb`
- Computes KPI snapshots and trends
- Breaks down performance by carrier/airport/route
- Identifies risk segments and seasonality
- Saves key charts to `/visuals`

### 3) Dashboard Metrics Export
Notebook: `notebooks/03_dashboard_metrics_export.ipynb`
- Produces aggregated tables for BI (monthly KPIs, carrier KPIs, route KPIs)
- Validates totals and KPI math
- Exports dashboard-ready files (CSV or tables)

### 4) SQL (Optional)
File: `sql/kpi_queries.sql`
- Example aggregation queries used for validation and repeatability

---

## Dashboard
Link: see `dashboard/dashboard_link.md`  
Preview images: `/visuals`

Suggested dashboard sections:
- KPI cards (On-time %, Delay %, Cancellation %, Avg delay)
- Trend line (monthly on-time performance)
- Carrier comparison
- Airport/route risk views

---

## Results Summary (Update with your findings)
- [Add 3–5 bullet insights here once analysis is complete]

---

## Tools
- SQL
- Python (pandas, matplotlib)
- Tableau or Power BI

---

## Contact
Emioluwa Adenuga  
LinkedIn: [add link]  
Email: [add email]

