# 🚚 Swift-Route-Logistic-Dashboard



A multi-page Power BI dashboard for end-to-end logistics operations monitoring — covering orders, drivers, hubs, and vehicles.

---

## 📊 Dashboard Overview

The report consists of **4 pages**, each focusing on a different operational dimension:

  Page  Focus 

 - Page 1 – Overview : High-level KPIs and cross-hub performance 
 - Page 2 – Drivers : Per-driver delivery stats and profiles 
 - Page 3 – Hubs : Hub capacity, processing times, and on-time rates 
 - Page 4 – Vehicles : Fleet status, breakdown analysis, and order distribution 

---

## 🗂️ Data Model

The dataset contains the following tables:

- **Orders** – Order ID, order date, actual delivery date, delivery status, delay reason, CSAT score, hub name, driver ID
- **Drivers** – Driver ID, driver name, hire date, years of experience, performance rating
- **Hubs** – Hub name, hub capacity, hub processing time (hours)
- **Date Table** – Calendar table used for time intelligence

### Key Fields

 Field Description 

- `Is Delayed` : Boolean flag — whether a delivery was delayed 
- `Is On Time` : Boolean flag — whether a delivery met the scheduled time 
- `Avg Delivery Time (hrs)` : Average time from order to delivery 
- `CSAT %` : Customer satisfaction score percentage 
- `On Time Delivered Rate` : % of orders delivered on time 
- `Delayed Delivery Rate` : % of orders delivered late 

---

## 📈 Key Metrics (April 2024 )

 Metric Value 

- Total Orders : 1,156 
- On Time Delivered Rate : 80.50% 
- CSAT %  84.2% 
- Avg Delivery Time  35.8 hrs 

> previous month (PM). April 2024 showed slight declines in CSAT (-6.4%) and on-time rate (-0.4%) vs. March.

---

## 🏢 Hub Performance

Six distribution hubs are tracked across Texas:

- Houston Hub
- Dallas Main Hub
- Austin Hub
- San Antonio Hub
- Fort Worth Hub
- El Paso Hub

**March 2024 On-Time Delivered Rates:**

 Hub Rate

- Houston Hub : 83.39% 
- Dallas Main Hub : 82.94% 
- El Paso Hub : 82.69% 
- Fort Worth Hub : 81.68% 
- San Antonio Hub  79.75% 
- Austin Hub : 70.27%
- 
**Hub Processing Time (avg hours):**
Austin Hub leads at ~41 hrs; San Antonio Hub is most efficient at ~24 hrs.

---

## 🧑‍✈️ Driver Performance

The **Drivers page** provides an individual driver breakdown including:

- Total deliveries per month
- Delayed delivery rate ranking
- Years of experience vs. performance rating scatter plot
- Driver card (name, hire date, YOE, star rating)

**Top Delayed Delivery Rates (April 2024):**

 Driver  Delayed Rate 
 
- Christopher Miller : 42.1% 
- Sarah Lopez : 41.2% 
- Joseph Williams : 40.0% 
- Karen Smith : 33.3% 
- John Moore : 31.3% 

---

## 🚐 Vehicle Fleet

**April 2024 Fleet Status:**
- 33 vehicles Active (73.33%)
- 12 vehicles In Maintenance (26.67%)

**Top Vehicle Models by Orders:**

| Model | Orders |
|-------|--------|
| Mercedes Sprinter | 35 |
| International DuraStar | 34 |
| Ford Transit | 29 |
| Freightliner M2 | 27 |
| Ram ProMaster | 20 |

**Vehicle Types:** Vans dominate at ~60.64%, followed by Trucks (24.57%) and Pickups/Box Trucks.

**Top Breakdown Count by Model:**
Freightliner leads with 153 recorded breakdowns, followed by Mercedes Sprinter (92) and Ford Transit (68).

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** – Report development
- **DAX** – Measures and calculated columns
- **Power Query (M)** – Data transformation
- **Data source** – Tabular data model with Orders, Drivers, Hubs, and Date tables

---

## 📁 File Structure

```
swift-route-logistics/
│
├── SwiftRouteLogistics.pbix    # Main Power BI report file
├── README.md                   # Project documentation
└── data/                       # (Optional) Source data files
    ├── orders.csv
    ├── drivers.csv
    └── hubs.csv
```

---

## 🚀 Getting Started

1. Clone or download this repository.
2. Open `SwiftRouteLogistics.pbix` in **Power BI Desktop**.
3. If using local CSV data, update the data source path via **Transform Data → Data Source Settings**.
4. Use the **Year** and **Month** slicers on each page to filter by time period.
5. Use the **DriverName** filter on the Drivers page to view individual profiles.

---

## 📌 Notes

- Dashboard is filtered by **Year** and **Month** on all pages.
- The Drivers page supports cross-filtering by driver name.
- Hub processing time heatmap shows day-of-week variation (Mon–Sun).
- Vehicle age and breakdown scatter plot helps identify high-risk fleet units.

---

## 📄 License

This project is for educational/portfolio purposes. Data is simulated and does not represent real logistics operations.
