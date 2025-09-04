# FruVibe Analytics — Sales, Marketing & Operational Insights  

A complete, end-to-end **data analytics case study** using Python + Power BI.  
This project simulates FruVibe’s pilot in East London (Mar–Jul 2025) to answer:  
**What should we sell, to whom, at what price, and how do we deliver on time?**

<p align="center">
  <img src="screenshots/executive_summary.png" alt="Executive Summary Dashboard" width="900">
</p>

---

![Made with Python](https://img.shields.io/badge/Made%20with-Python-blue)
![Power BI](https://img.shields.io/badge/Visualized%20in-Power%20BI-yellow)

---

##  TL;DR Results
- **890 orders**, **£13.06K revenue**, **31% subscription share**  
- **On-Time = 92.5%**, **Fulfillment = 99.8%**  
- **Top area:** IG3 (highest orders & revenue)  
- **Top one-time product:** Immunity Booster Platter  
- **Best subscription plan AOV:** Elevate (£39.75 vs one-time £6.65)  

---

##  Business Problem
FruVibe needed to validate its **subscription model and operations** during a pilot in East London.  
The key business questions were:
1. Which products and plans generate the most revenue?  
2. Who are the most valuable customer segments?  
3. How reliable are morning vs. evening deliveries?  
4. What operational bottlenecks exist?  

---

##  Objectives
- Clean and prepare raw order & survey data.  
- Build dashboards for **Sales, Marketing, and Operations**.  
- Translate data into **business recommendations**.  

---

##  Tools & Methods
- **Python (Pandas, NumPy, Matplotlib)** → Data cleaning & processing  
- **Power BI** → Data modeling & dashboards  
- **Excel** → Data validation & quick checks  
- **GitHub** → Version control & portfolio hosting  

---

##  Key Insights
- Subscriptions = **31% of orders but ~70% of revenue** → critical for growth  
- Immunity Booster Platter = **#1 one-time product**  
- Evening deliveries = fewer orders but **higher reliability (96%)**  
- 60% of customers scored **High loyalty** in survey → strong retention potential  
- RM6 flagged with **lowest On-Time % (82.6%)** → delivery risk zone  

---

##  Dashboards (Power BI)

| Page | Screenshot |
|------|------------|
| **Executive Summary** | ![Executive Summary Dashboard](screenshots/executive_summary.png) |
| **Operations Dashboard** | ![Operations Dashboard](screenshots/operations.png) |
| **Customer Insights** | ![Customer Insights Dashboard](screenshots/customer_insights.png) |
| **Product & Pricing** | ![Product & Pricing Dashboard](screenshots/product_pricing.png) |
| **Geo Insights** | ![Geo Insights Dashboard](screenshots/geo_insights.png) |

➡ Full interactive dashboard available in Power BI Service (https://app.powerbi.com/groups/me/reports/fa809d76-cb5c-4f23-8f06-a50875bc0327/5f502cda05e12c019dea?experience=power-bi).

➡ `.pbix` file included in `dashboards/`.

---

##  📂Repository Structure

---

##  Data Preparation
- **Orders dataset**  
   Parsed dates, standardized text  
   Engineered features: `IsSubscription`, `IsEvening`, `IsOnTime`, `Month`, `PrePostPilot`  
- **Survey dataset**  
   Age grouping, loyalty scoring, subscription intent  
- Outputs saved to `data/processed/`:  
   `orders_clean.csv`  
  `survey_clean.csv`  

---

##  DAX Measures (examples)
```DAX
Total Orders = COUNTROWS(orders_clean)
Total Revenue = SUM(orders_clean[Revenue])
OnTime % = DIVIDE([OnTime Orders], [Total Orders])
Fulfillment % = DIVIDE([Fulfilled Orders], [Total Orders])
Subscription % = DIVIDE([Subscription Orders], [Total Orders])
AOV (Morning) = DIVIDE([Revenue (Morning)], [Morning Orders])
AOV (Evening) = DIVIDE([Revenue (Evening)], [Evening Orders])
