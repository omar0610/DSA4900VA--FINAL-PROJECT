# DSA4900VA Final Project: Matcha Haven Revenue Forecasting Dashboard

[![Power BI Live Dashboard](https://img.shields.io/badge/View-Live%20Dashboard-brightgreen?style=for-the-badge&logo=power-bi)](https://app.powerbi.com/view?r=eyJrIjoiZTgzYzNmNjMtZDM2MS00YzIzLThmMTAtNDQ0ZmU3NDAyNTI1IiwidCI6IjE2ZDgzZWU2LTI1NGEtNDY5ZC1hNmNjLTU0ZTJjYTIzMTNlNyIsImMiOjh9)

## 📊 Project Overview
This repository contains the full analytical pipeline for my DSA4900VA final project at United States International University Africa. The project uses Matcha Haven café as a real world case study to build a complete business intelligence and forecasting system that connects RStudio predictive modeling with an interactive five page Power BI dashboard.

The dashboard provides a multi perspective view of the business, including revenue trends, inventory stability, employee productivity, customer behaviour patterns, and twelve week revenue forecasts for October to December 2025.

**Core Innovation**  
Transforms raw daily sales logs (about 17577 rows) into a complete decision support solution:
- Five page Power BI dashboard  
- Revenue forecasting using Random Forest, ARIMA, ETS, and hybrid models  
- Real time DAX measures for slicing insights by date, order type, employee, category, and payment method  
- Full operational intelligence across sales, inventory, staffing, customers, and upcoming performance  

**Business Impact**  
Helps Matcha Haven:
- Anticipate weekend demand (Saturday and Sunday peaks)  
- Track waste and category level stock movement  
- Measure employee efficiency by shift and payment method  
- Understand customer preferences and spending  
- Plan for Q4 2025 using stable and credible forecasts  

---

## 🚀 Quick Start

### Prerequisites
- R and RStudio (with packages: readxl, dplyr, tidyr, lubridate, forecast, ggplot2, knitr)
- Power BI Desktop
- Git (optional)

### Setup and Run

1. **Clone the Repository**
git clone https: https://github.com/omar0610/DSA4900VA-FINAL-PROJECT

2. **Run Forecasting in RStudio**
- Open `MatchaHaven1 Improved model.Rmd`
- Knit to generate forecasts, regression tables, and visual outputs
- Export the twelve week forecast to CSV for Power BI

3. **Open the Power BI Dashboard**
- Use the live link above or open `MatchaHaven1.pbix`
- Refresh data and explore the slicers:
  - Date
  - Name
  - Order Type
  - Payment Method
  - Category

---

## 📁 Project Structure

DSA4900VA-FINAL-PROJECT/
├── MatchaHaven1 Improved model.Rmd
├── MatchaHaven Baseline Model.Rmd
├── MatchaHaven1.xlsx
├── Matcha Forecasting Report.xlsx
├── MatchaHaven1.pbix
├── theme.json
└── README.md

---

## 📊 Dashboard Pages and Key Insights

### **Page 1: Sales and Revenue**
Shows full revenue performance from April to September 2025.

**Key Visuals**
- Revenue Growth Over Time (daily line chart)
- Revenue by Category (Mojitos, Matcha, Specialty Matcha, Tea and Hot Drinks, Cold Coffee, Cakes, Desserts, Extras)
- Revenue by Item Name (top performing drinks)
- Order Type Distribution (dine in, takeaway, delivery)
- Payment Method Breakdown (MPesa, cash, card)

**KPIs**
- Total Revenue: KSh 12.723M  
- Total Transactions: 17.577K  
- Average Daily Revenue: KSh 69.524K  

---

### **Page 2: Inventory**
Shows stock behaviour, waste patterns, and average inventory stability.

**Key Visuals**
- Top five wasted items  
- Average Closing Stock by Category  
- Average Opening Stock by Category  
- Total Sales vs Total Purchases (trend line)

**Inventory Table Includes**
- Average Opening Stock  
- Average Closing Stock  
- Reorder Point  
- Target Stock  
- Average Daily Sales  
- Net Stock Movement  

---

### **Page 3: Employee Performance**
Analyzes staff productivity across shifts, hours, and payment methods.

**Key Visuals**
- Employee profile list  
- Shift Based Employee Productivity (stacked bar chart)  
- Monthly Performance Trend (line area chart)  
- Sales by Employee (split by payment method)  
- Orders Handled per Employee  
- Average Sale Value per Employee  
- Average Sales Per Employee Per Day  
- Average Transactions Per Employee Per Day  

**Top Performer**  
- Walter with about KSh 4.293M revenue

---

### **Page 4: Customer Trends**
Shows how customers behave, what they buy, and when they spend.

**Key Visuals**
- Percentage of Sales by Shift Hours  
- Average Spending Per Order Type  
- Customer Spending Summary  
  - Average: KSh 723.84  
  - Minimum: KSh 80  
  - Maximum: KSh 4500  
  - Median: KSh 500  
- Payment Preferences (donut chart)
- Sales by Day of Week  
- Top five best selling drinks  
- Top five best selling food items  

---

### **Page 5: Forecasting and Regression Analysis (Q4 2025)**
Merges RStudio model outputs with BI visuals.

**Key Visuals**
- Historical Revenue and Random Forest Forecast for Oct 1 to Dec 23 2025  
- Forecast KPIs  
  - Daily Average: about KSh 69538  
  - Weekly Average: about KSh 449321  
  - Total for the 12 Week Period  
- Model Comparison Table (RMSE, MAE, MAPE)

**Forecast Summary**
- Twelve week projected revenue: about **KSh 5.9M**  
- Models strongly agree with correlations above 0.9  
- Random Forest selected as the best performing model  

---

## 📈 Results and Insights
- Q4 projection: about KSh 5.9M  
- Weekend revenue remains the highest  
- Delivery and takeaway dominate order types  
- Classic Mojito leads drinks  
- Lotus Milkcake leads food items  
- Forecast stability ranges from 9 percent to 16 percent  

---

## 🤝 Contributing
- Fork the project and submit pull requests  
- Suggest improvements through GitHub Issues  
- Contact: oanis@usiu.ac.ke  

---

## 📄 License
MIT License—use freely for non-commercial SME analytics. © 2025 Omar Anis A. Mohamud (USIU-Africa DSA4900VA).

---

*Powered by RStudio & Power BI for USIU-Africa. Star if helpful! 🌟*
