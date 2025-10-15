# DSA4900VA Final Project: Matcha Haven Revenue Forecasting Dashboard

[![Power BI Live Dashboard](https://img.shields.io/badge/View-Live%20Dashboard-brightgreen?style=for-the-badge&logo=power-bi)](https://app.powerbi.com/view?r=eyJrIjoiZTgzYzNmNjMtZDM2MS00YzIzLThmMTAtNDQ0ZmU3NDAyNTI1IiwidCI6IjE2ZDgzZWU2LTI1NGEtNDY5ZC1hNmNjLTU0ZTJjYTIzMTNlNyIsImMiOjh9)

## 📊 Project Overview
This repository holds the complete code, data samples, and deliverables for my DSA4900VA final project at United States International University – Africa (USIU-Africa). The project builds a decision-support system for SMEs in Kenya's service sector, using Matcha Haven café as a case study. It integrates predictive modeling in RStudio (via RMarkdown) with interactive Power BI dashboards to forecast revenue, track KPIs, and deliver insights on sales, staffing, and customer trends.

**Core Innovation**: Turns manual sales records (~17,577 rows) into 12-week forecasts (Oct-Dec 2025: KSh 5.56M total, avg KSh 463K/week) using ARIMA/ETS ensembles, visualized in a 4-page Power BI dashboard with DAX measures for real-time slicing (e.g., by OrderType or DayOfWeek).

**Impact**: Helps Matcha Haven proactively manage weekends (Sat/Sun ~KSh 80K/day peaks) and mid-week dips, targeting 5-10% profitability boost. Broader: Affordable analytics template for Nairobi SMEs.

**Tech Stack**:
- **RStudio**: Forecasting (forecast package), reports (RMarkdown).
- **Power BI**: Dashboards with DAX (e.g., [Revenue Growth] = DIVIDE([Total] - PREVIOUSMONTH([Total]), [Total])).
- **Data**: Manual Excel logs; cleaned CSV for import.

## 🚀 Quick Start
### Prerequisites
- R/RStudio (v4.0+; install packages: `install.packages(c("readxl", "dplyr", "tidyr", "lubridate", "forecast", "ggplot2", "knitr"))`).
- Power BI Desktop (free; Pro for sharing the live dashboard).
- Git (optional).

### Setup & Run
1. **Clone the Repo**: git clone https://github.com/omar0610/DSA4900VA-FINAL-PROJECT.git
cd DSA4900VA-FINAL-PROJECT


2. **Run R Forecasting**:
- Open `MatchaHaven1 Improved model.Rmd` in RStudio.
- Knit (Ctrl+Shift+K) to HTML/PDF: Outputs forecasts, plots, and regression.
- Key Result: 12-week ensemble (ARIMA/ETS avg); export CSV for Power BI.

3. **Launch Power BI Dashboard**:
- Open the published link: [Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiZTgzYzNmNjMtZDM2MS00YzIzLThmMTAtNDQ0ZmU3NDAyNTI1IiwidCI6IjE2ZDgzZWU2LTI1NGEtNDY5ZC1hNmNjLTU0ZTJjYTIzMTNlNyIsImMiOjh9).
- Or load local .pbix: Refresh data > Interact with slicers (e.g., filter by Date/OrderType).
- Pages:
  - **Sales & Revenue**: Trends, category bars, order pies (DAX: [Total Revenue] = SUM(TotalAmount)).
  - **Employee Performance**: Shift productivity, sales/employee (DAX: [Avg Sales/Day] = DIVIDE(SUM(Sales), DISTINCTCOUNT(Date))).
  - **Customer Trends**: Top items, spending summaries (DAX: [Growth %] = [Total] / CALCULATE([Total], PREVIOUSMONTH(Date))).
  - **Forecasting & Regression**: R-embedded lines/bars for Q4 (e.g., weekly KSh 463K avg).

4. **Generate Reports**:
- Knit `MatchaHaven Baseline Model.Rmd` for lm baseline comparison.
- Export to Word/PDF via RStudio.

## 📁 Key Files & Structure
DSA4900VA-FINAL-PROJECT/
├── MatchaHaven1 Improved model.Rmd     # Main RMarkdown: ARIMA/ETS forecasts + regression
├── MatchaHaven Baseline Model.Rmd      # Baseline linear model
├── MatchaHaven1.xlsx                   # Raw manual data (17,577 rows)
├── Matcha Forecasting Report.xlsx      # Excel summary of KPIs/forecasts
├── MatchaHaven1.pbix                   # Power BI report file
├── theme.json                          # Power BI custom theme (Matcha greens)
└── README.md                           # This file


## 📈 Results & Insights
- **Forecast**: Q4 KSh 5.56M total (weekly avg KSh 463K); Sat/Sun peaks ~KSh 80K/day.
- **Insights**: Delivery/Takeaway 76% orders (KSh 8K avg); top item (Classic Mojito) KSh 949K; DAX trends show 2-3% WoW growth.
- **Model Perf**: Ensemble RMSE 13K (93% better than baseline lm, MAPE <16%).
- **Dashboard Highlights**: DAX enables what-ifs (e.g., [YoY Growth] = DIVIDE([Total] - SAMEPERIODLASTYEAR([Total]), SAMEPERIODLASTYEAR([Total]))); slicers for DayOfWeek/OrderType.

See report for visuals (e.g., forecast line with intervals, weekly bars).

## 🤝 Contributing
- Fork the repo and submit PRs for improvements (e.g., add holiday regressors).
- Issues: Report bugs or suggest DAX tweaks.
- Contact: oanis@usiu.ac.ke

## 📄 License
MIT License—use freely for non-commercial SME analytics. © 2025 Omar Anis A. Mohamud (USIU-Africa DSA4900VA).

---

*Powered by RStudio & Power BI for USIU-Africa. Star if helpful! 🌟*
