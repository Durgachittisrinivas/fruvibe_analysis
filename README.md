# Fruvibe Market & Operations Analytics

**Fruvibe** is a fresh fruit platter delivery startup piloted in **East London (Mar–Jul 2025)**.  
This project simulates how data analytics supported Fruvibe’s business strategy — from customer research and pricing sensitivity to operational improvements.

---

## 📂 Repository Structure


---

## 📊 Datasets

### 1. Orders (Mar–Jul 2025)
**File:** `data/raw/fruvibe_orders_eastlondon.csv`  
**890 rows (orders)** with columns:
- `OrderDate` (2025-03-16 to 2025-07-07)  
- `PostcodeDistrict`, `AreaGroup`  
- `OrderType` (Subscription / OneTime)  
- `Plans` (Essence £32.95, Elevate £39.75, Everjoy £18.99)  
- `Product` (subscription plan or 1 of 6 Platters @ £6.65)  
- `Revenue` (per order)  
- `DeliverySlot` (Morning / Evening)  
- `OnTime`, `Fulfilled`  

---

### 2. Customer Survey
**File:** `data/raw/fruvibe_survey_eastlondon.csv`  
**276 respondents** with demographics, product preferences, subscription interest, and delivery window preference.  

---

### 3. Geo Lookup
**File:** `data/raw/fruvibe_geo_postcodes.csv`  
Maps postcode → Latitude/Longitude for Power BI geo maps.  

---

## 🚀 Analysis Roadmap
1. **Data Cleaning** → Check quality, create new features (age groups, loyalty, delivery KPIs).  
2. **Exploratory Analysis** → Demand hotspots, product mix, subscription interest, pilot impact.  
3. **Dashboards** (Power BI) → 5+ dashboards: Customer Insights, Pricing, Geo Map, Operations, Exec Summary.  
4. **Report** → Business insights + recommendations (e.g., evening deliveries improved OnTime%).  

---
  
