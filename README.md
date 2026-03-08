# b2b-product-demand-analysis
Excel based product demand and revenue analysis for a B2B sotware company using Power Pivot,DAX measures, and an interactive dashboard covering 2018-2019 order data.
# B2B Product Demand & Revenue Analysis

Excel-based product demand and revenue analysis for a B2B software company 
using Power Pivot, DAX measures, and an interactive dashboard covering 
2018-2019 order data.

---

## Business Context

A B2B software company that sells productivity tools and business intelligence 
solutions to enterprise clients across the United States operates a 
multi-warehouse distribution model for physical product deliveries including 
hardware devices, installation kits, and training materials.

Leadership observed the following concerns:
- Significant month-over-month revenue volatility
- Inconsistent demand patterns across warehouses and regions
- Concerns about inventory planning and warehouse utilization
- Questions around product performance and overall portfolio health
- Uncertainty about geographic expansion priorities

---

## Project Objective

To conduct a comprehensive product demand analysis that answers three 
core questions:
1. **What is happening?** — Trends across time, products, warehouses and geography
2. **Why is it happening?** — Root causes of demand volatility and performance gaps
3. **What should we do?** — Actionable recommendations for leadership

---

## Tools & Techniques Used

| Tool | Purpose |
|------|---------|
| Microsoft Excel | Primary analysis and dashboard tool |
| Power Pivot | Data Model and Star Schema architecture |
| DAX | 14 custom KPI measures including YoY calculations |
| Power Query | Data loading and transformation |
| PivotTables & Charts | Analysis and visualisation |
| Camera Tool | Dynamic KPI cards on dashboard |

---

## Data Overview

- **Period:** 2018 - 2019
- **Warehouses:** 4 (Cedar Park, Berkeley, Montcalm, Oakland Mills)
- **Products:** 20+
- **Fields:** Category, Product, Warehouse, ZIP Code, Date, Time, 
  Order Demand, Value, Revenue

---

## Data Model Architecture

Built using a **Star Schema** in Power Pivot:

- **Fact Table (Table1):** All transaction records
- **Dimension Table (Calendar):** Date intelligence table with Year, 
  Month, Day of Week, MMM-YYYY, and Date Hierarchy
- **Relationship:** Table1[Date] → Calendar[Date]

---

## DAX Measures Created

**Base Measures**
- Total Demand
- Total Revenue
- Order Count
- Avg Order Size

**Time Intelligence**
- PY Demand (Previous Year)


**KPI Measures with YoY Indicators**
- Total Demand YoY
- Total Revenue YoY
- Top Product by Demand + YoY
- Top Product by Revenue + YoY
- Top Warehouse by Revenue + YoY
- Top Warehouse by Demand Count + YoY

---

## Key Findings

### 1. Cedar Park Dominates the Business
Cedar Park generates **75% of all revenue ($440.80B)** from just 6,764 
orders — an average order size of 184,289 units. This reveals a small 
number of large enterprise clients driving the majority of revenue, 
creating significant concentration risk.

### 2. Two Distinct Customer Segments
| | Cedar Park | Berkeley |
|--|--|--|
| Customer Type | Large enterprise | Small-medium businesses |
| Top Product | TBOX | VideoRight |
| Avg Order Size | 184,289 units | 9,566 units |
| Order Count | 6,764 | 36,874 |

### 3. TBOX is the Top Product
TBOX leads in both revenue ($68.96B) and demand but is nearly 
absent at Berkeley — a major cross-sell opportunity.

### 4. No Confirmed Seasonal Pattern
October 2018 recorded 277.57M in demand versus 42.73M in October 
2019 — a **549% difference** — making seasonal forecasting unreliable 
with only two years of data.

### 5. Monday & Night Ordering Dominate
Monday is the strongest day for demand. Night-time orders are largest 
in volume suggesting automated bulk procurement by enterprise clients.

---

## Dashboard

The interactive Excel dashboard includes:
- **6 KPI Cards** with YoY indicators (Total Revenue, Total Demand, 
  Top Product by Revenue, Top Product by Demand, Top Warehouse by 
  Revenue, Top Warehouse by Demand Count)
- **Monthly Revenue Trend** line chart
- **Warehouse Performance** bar chart
- **Category Performance** bar chart
- **Top 5 Products** by Revenue
- **Bottom 5 Products** by Revenue
- **Day of Week Demand** bar chart
- **Year and Category Slicers** for interactivity

---

## Project Files

| File | Description |
|------|-------------|
| `Consumer-Product_Demand.xlsx` | Main Excel file with Data Model, analysis and dashboard |
| `Executive_Intelligence_Brief.docx` | Concise report written for non-technical leadership |

---

## Skills Demonstrated

- Data modelling (Star Schema)
- DAX formula writing
- Time intelligence calculations
- KPI design and measurement
- Dashboard design and layout
- Business insight generation
- Executive communication and storytelling with data

---

## Limitations

- Only two years of data — seasonal patterns cannot be confirmed
- No Customer ID — individual client analysis not possible
- No cost data — profitability analysis not possible
- October 2018 anomaly remains unexplained
- Time column reliability uncertain — The time data shows 
  night-time ordering dominating demand volumes. However for a company 
  delivering physical hardware, installation kits and training materials, 
  large orders being placed after 9pm is operationally unusual. The Time 
  column likely reflects when orders were *recorded or processed* by the 
  system rather than when customers actually placed them, making 
  time-of-day conclusions unreliable.

---

## Author

**Ozioma Okoyenta**  
Data Analyst  
[GitHub Profile](https://github.com/ozioma-o)

---

*This project was completed as part of a structured data analytics 
learning programme.*
