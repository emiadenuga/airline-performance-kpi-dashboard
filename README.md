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
- Which airlines have the highest delay and cancellation rates?
- Which routes are most operationally risky?
- How has on-time performance changed over time?
- Are delays seasonal or systemic?
- Which carriers maintain consistent reliability?
- Where should leadership focus operational improvements first?

---

## Dataset
Source: U.S. DOT / Bureau of Transportation Statistics (BTS) On-Time Performance.
- Portal: https://www.transtats.bts.gov/ontime/
- Data is commonly downloaded month-by-month and combined for a full year.

> Note: Raw source files are not included here. See `/data/raw/README.md` for download notes.

---

## KPI Definitions
- **Total Flights:** Count of scheduled flights
- **Delay rate:** % of flights with arrival delay > 15 minutes
- **Cancellation rate:** % of flights marked cancelled
- **Avg delay minutes:** average arrival delay minutes (excluding cancellations)
- **Severe delay rate:** % of flights with delay > 30 (or 60) minutes

---

## Project Workflow

### 1) Data Preparation
Notebook: `notebooks/01_data_preparation.ipynb`
- Standardizes dates and key fields
- Handles cancellations/diversions consistently
- Engineers flags (delayed, severe delay) and route keys
- Outputs: `/data/processed/daily_kpi.csv`

### 2) KPI Analysis
Notebook: `notebooks/02_kpi_analysis.ipynb`
- Computes KPI snapshots and trends
- Breaks down performance by carrier/airport/route
- Identifies risk segments and seasonality

### 3) Dashboard Metrics Export
Notebook: `notebooks/03_dashboard_metrics_export.ipynb`
- Produces aggregated tables for BI (monthly KPIs, carrier KPIs, route KPIs)
- Validates totals and KPI math
- Exports dashboard-ready files (CSV)

---

## Dashboard
Link: see `dashboard/dashboard_link.md`  

---

## Results Summary
Across approximately 6.8 million flights:

- ~20% of flights arrived more than 15 minutes late.
- Cancellation rates remained relatively low (~1.3%), though winter months showed elevated disruption.
- Carrier-level analysis revealed meaningful performance variation.
- Specific routes and origin airports drive disproportionate delay concentration.
- Seasonal patterns suggest operational strain during peak demand and adverse weather periods.

---

## Tools
- Python (pandas, matplotlib)
- Excel
- Tableau
  
---

## Skills Demonstrated

- Data cleaning and validation
- Volume-weighted KPI construction
- Time-series trend analysis
- Comparative performance analysis
- Dashboard dataset preparation
- Business-focused data storytelling

---

## Contact
Emioluwa Adenuga  
LinkedIn: [https://www.linkedin.com/in/emioluwaadenuga]  
Email: [ettisa4641@gmail.com]

