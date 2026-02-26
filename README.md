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
