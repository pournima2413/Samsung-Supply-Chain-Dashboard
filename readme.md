# 📊 Samsung Supply Chain Analytics Dashboard

> Transforming 5 supply chain domains into one connected Power BI intelligence report — from raw data to boardroom-ready insights.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat-square&logo=microsoftexcel&logoColor=white)
![Type](https://img.shields.io/badge/Type-Business%20Intelligence-2563EB?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-14B8A6?style=flat-square)

---

## 📌 What This Project Does

Most supply chain reports show **one thing at a time** — a sales chart here, a delivery report there.

This dashboard connects **all five supply chain layers in one place:**


Sales → Procurement → Production → Inventory → Shipment


The result: a business intelligence report that lets decision-makers spot problems
across the entire supply chain — not just in one department.

---

## 🎯 Business Problem Solved

| Challenge | Business Impact | Dashboard Response |
|---|---|---|
| Delivery delays | Lost customers, SLA breaches | Shipment page tracks on-time % by carrier |
| Inventory imbalance | Stockouts or overstock costs | Inventory page flags understock & overstock |
| Supplier inefficiency | Higher costs, longer lead times | Supplier page ranks lead time and cost |
| Revenue concentration | Over-reliance on few products | Sales page shows Pareto breakdown |
| Low defect visibility | Hidden quality issues | Production page monitors defect rate by facility |

---

## 📈 Key Numbers at a Glance

| Metric | Value | Insight |
|---|---|---|
| Total Revenue | ~$4.5 Billion | Strong top-line performance |
| Total Profit | ~$1 Billion | Healthy margin overall |
| On-Time Delivery | ~50% | Critical gap — biggest area for improvement |
| Defect Rate | ~1.3% | Low — quality control is working |
| Dashboard Pages | 7 | One per business domain + executive summary |

> **The most important finding:** On-time delivery at ~50% is the single biggest operational risk in this supply chain. Fixing carrier selection and shipment routing could unlock significant customer satisfaction and cost savings.

---

## 🧠 Data Model — Star Schema


                         ┌──────────────┐
                         │  Dim Date    │
                         └──────┬───────┘
                                │
┌──────────────┐    ┌───────────▼──────────┐    ┌──────────────┐
│ Dim Customer │────│     Fact Sales       │────│ Dim Product  │
└──────────────┘    └───────────┬──────────┘    └──────────────┘
                                │
              ┌─────────────────┼─────────────────┐
              │                 │                 │
   ┌──────────▼──────┐ ┌────────▼───────┐ ┌──────▼──────────┐
   │ Fact Inventory  │ │ Fact Shipment  │ │ Fact Procurement│
   └─────────────────┘ └────────────────┘ └─────────────────┘
              │
   ┌──────────▼──────┐    ┌──────────────┐
   │ Fact Production │    │ Dim Supplier │
   └─────────────────┘    └──────────────┘
                               │
                    ┌──────────▼──────────┐
                    │    Dim Facility     │
                    └─────────────────────┘


**Why Star Schema?**
Clean, denormalized structure that makes DAX calculations fast and report filters
responsive — critical when working with millions of rows across 5 fact tables.

---

## 📊 Dashboard Pages — What Each One Answers

### 🏠 Home
Navigation hub. One-click access to any dashboard section.

---

### 📊 Executive Summary
**Business question:** *"How is the overall business performing right now?"*

| KPI | Value | Status |
|---|---|---|
| Revenue | ~$4.5B | ✅ On track |
| Profit | ~$1B | ✅ Healthy |
| Supplier delays | Elevated | ⚠️ Monitor |
| Inventory accuracy | Imbalanced | ⚠️ Action needed |
| On-time delivery | ~50% | 🔴 Critical |

---

### 🤝 Supplier & Procurement
**Business question:** *"Which suppliers are costing us the most time and money?"*

- Lead time varies significantly across suppliers — top offenders identified
- Procurement cost fluctuations suggest inconsistent contract terms
- Discount rates are eroding profit margins on high-volume orders

---

### 🏭 Production
**Business question:** *"Where are our quality and output risks?"*

- Defect rate of ~1.3% is well controlled at the aggregate level
- Two facilities account for disproportionate share of defects — targeted fix needed
- Production volume shows seasonal patterns useful for capacity planning

---

### 📦 Inventory
**Business question:** *"Do we have the right stock in the right place?"*

- High-demand SKUs flagged for understock risk
- Low-demand categories carrying excess inventory — increasing holding cost
- Regional imbalance identified — redistribution opportunity exists

---

### 🚚 Shipment & Delivery
**Business question:** *"Why are half our deliveries late — and who is responsible?"*

- On-time delivery at ~50% is the most critical metric in this report
- Carrier analysis shows 2-3 carriers responsible for majority of delays
- Shipping cost per route varies — optimization potential identified

---

### 📈 Sales Performance
**Business question:** *"Where does our revenue actually come from?"*

- Top 20% of products generate ~80% of revenue (Pareto confirmed)
- Discount strategy on high-volume products is reducing net profitability
- Seasonal peaks visible — useful for procurement and inventory planning

---

## 🛠️ Tools & Skills Demonstrated

| Tool | How It Was Used |
|---|---|
| **Power BI** | Multi-page dashboard, DAX measures, drill-throughs, slicers |
| **SQL** | Data extraction, joins, aggregations for model preparation |
| **Python (Pandas, NumPy)** | Data cleaning, null handling, feature engineering |
| **Excel** | Initial data profiling and validation |
| **Star Schema Design** | Fact + dimension table modelling for BI performance |
| **DAX** | KPI calculations, time intelligence, conditional formatting |

---

## 💡 What I Built and Learned


✅  Designed a Star Schema from scratch across 5 fact tables
✅  Built 7 connected dashboard pages with cross-filtering
✅  Wrote DAX measures for revenue, profit, lead time, and delivery KPIs
✅  Identified on-time delivery at ~50% as the #1 operational risk
✅  Applied Pareto analysis to surface revenue concentration insight
✅  Connected procurement, production, inventory, and sales in one model


---

## ▶️ How to Open

bash
# Step 1 — Clone or download the repository
git clone https://github.com/pournima2413/Samsung-Supply-Chain-Dashboard

# Step 2 — Open the dashboard
# Launch Power BI Desktop (free: https://powerbi.microsoft.com/desktop)
# Open Samsung.pbix

# Step 3 — Explore
# Use the Home page to navigate
# Use slicers to filter by date, region, supplier, or product category


## 📁 Project Structure


Samsung-Supply-Chain-Dashboard/
│
├── Samsung.pbix              ← Main Power BI dashboard file
│
├── data/
│   └── supply_chain_data.csv ← Raw dataset
│
├── images/
│   ├── home.png
│   ├── executive.png
│   ├── supplier.png
│   ├── production.png
│   ├── inventory.png
│   ├── shipment.png
│   └── sales.png
│
├── sql/
│   └── queries.sql           ← Data preparation queries
│
└── README.md


---

## 🔗 Connect

**Pournima Kamble** — MS Computer Science @ Cleveland State University (2026)
Seeking Data Analyst & Data Engineer roles · Available June 2026

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/pournimakamble)
[![GitHub](https://img.shields.io/badge/GitHub-pournima2413-333?style=flat-square&logo=github&logoColor=white)](https://github.com/pournima2413)
[![Email](https://img.shields.io/badge/Email-pournima2413@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:pournima2413@gmail.com)
