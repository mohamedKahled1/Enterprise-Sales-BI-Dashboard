# 🛒 Enterprise Sales Performance & Dynamic Target Analytics

## 📌 Project Overview
This is an end-to-end Enterprise Business Intelligence and Data Engineering project analyzing sales performance, dynamic multi-region targets, and salesperson efficiency. The project simulates a high-scale corporate environment, handling complex transactional matrices directly connected to a relational database server.

The project demonstrates a complete corporate data analytics lifecycle:
1. **SQL & Data Engineering:** Schema extraction, entity relationship creation, primary/foreign key mapping, and granularity alignment.
2. **Power Query (ETL):** Advanced data cleaning, custom transformations, and automated data loading.
3. **Power BI & DAX:** Engineering a robust, high-performance relational model and delivering an executive-grade 7-page interactive dashboard with dynamic UX navigation.

---

## 🛠️ Data Architecture & Engineering Pipeline

### 1. Relational Engineering & SQL Layer
Before visualization, optimized relational database principles were simulated and applied to the core tables to ensure data integrity, eliminate redundancy, and structure the data for advanced business metrics:
* **Relational Schema Mapping:** Analyzed entity structures to connect central transactional fact tables (`SalesData`, `TargetT`) with dimensional tables (`Calendar`, `ItemsT`, `SalesmanT`, `CustomerDBT`, `RouteT`) using strict **One-to-Many ($1 \rightarrow *)$** relationships[cite: 1].
* **Key Enforcement:** Configured direct relational bindings between Primary Keys (`CustomerID`, `SalesmanNo`, `ItemID`, `RouteID`)[cite: 1] and their corresponding Foreign Keys in the transaction ledger.
* **Granularity Alignment:** Resolved cross-functional filtering conflicts by bridging the gap between high-level periodic targets (`TargetT`) and dynamic, daily transactional inputs (`SalesData`)[cite: 1].
* **Performance Tuning:** Organized the analytical schema to optimize cross-filtering paths, eliminate ambiguous relationships, and ensure lightning-fast visual rendering.

### 2. Advanced Power Query ETL Layer
The relational data streams were processed through Power Query to execute rigorous data transformation steps:
* **Schema Standardization:** Cleaned, formatted, and typed mixed transactional fields, ensuring exact alignment across text, numeric, and currency attributes.
* **Custom Date Dimension:** Developed an enterprise calendar dimension supporting specialized corporate time-intelligence (Weeks, Active Days, Working Days, and fiscal periods)[cite: 1].
* **Null & Exception Handling:** Implemented robust filtering logic to eliminate structural data gaps and maintain 100% data auditing precision.

---

## 📐 Analytics & DAX Calculations
A centralized measure repository was authored to compute critical corporate KPIs and period-over-period variance metrics using advanced **DAX**:

* **Total YTD Sales:**
  $$Total\ YTD\ Sales = TOTALYTD(SUM(SalesData[ConvertedQty] * SalesData[UnitPrice]), 'Calendar'[Date])$$
* **Target Achievement %:** Tracks how effectively a region or salesperson fulfilled corporate goals:
  $$Target\ Achievement\ \% = DIVIDE(SUM(SalesData[LineTotal]), SUM(TargetT[Target]), 0)$$
* **Sales Variance vs Target:** Measures financial deviations against corporate budgets:
  $$Sales\ Variance\ vs\ Target = [Gross\ Sales] - SUM(TargetT[Target])$$
* **Average Order Value (AOV):** Monitors transactional sizing efficiency:
  $$Average\ Order\ Value\ (AOV) = DIVIDE(SUM(SalesData[LineTotal]), DISTINCTCOUNT(SalesData[OrderID]), 0)$$

---

## 📈 Advanced Financial Auditing & Key Business Insights

* **Financial Revenue Integrity:** Successfully monitored and audited **1.38 Billion EGP in YTD Net Revenue**, registering a massive **23.1% Year-Over-Year (YoY) revenue acceleration rate** compared to the previous fiscal cycle (`YAGO` baseline).
* **High-Volume Transactional Scale:** Engineered data streams to aggregate and validate multi-layer transactional data covering **137,380 Corporate Orders**[cite: 1] executed by a footprint of **27,176 Active Retail/Wholesale Customers**[cite: 1] across complex geographic boundaries.
* **Target Achievement & Variance Analysis:** Developed a dynamic variance matrix showing that the enterprise achieved an aggressive **145% overall target fulfillment rate**[cite: 1], while seamlessly tracking micro-level drops (e.g., pinpointing branches stuck at 0% achievement versus segments surging past 100%+ targets)[cite: 1] to optimize inventory and supply chain distribution.
* **Salesforce Velocity & Order Sizing:** Conducted deep-dive efficiency auditing on individual salesperson performance, correlating **MoM & YTD Growth rates**[cite: 1] with logistics efficiency metrics—specifically capturing an **Average Order Value (AOV) of 11,203 EGP**[cite: 1] and measuring precise **Drop Sizes**[cite: 1] to reduce operational overhead.

---

## 📊 Dashboard & Report Preview

### 1. Interactive Navigation Hub (Home)
![Home Screen](images/SalesData1_page-0001.jpg)

### 2. Executive KPIs Summary Page
![KPIs Summary](images/SalesData1_page-0002.jpg)

### 3. Enterprise Sales Overview Page
![Sales Overview](images/SalesData1_page-0003.jpg)

### 4. Branch Performance Matrix (Region vs. Target)
![Region vs Target](images/SalesData1_page-0004.jpg)

### 5. Salesforce Tracking Matrix (Salesman vs. Target)
![Salesman vs Target](images/SalesData1_page-0005.jpg)

### 6. Customer Behavioral & Cohort Analysis
![Customer Analysis](images/SalesData1_page-0006.jpg)

### 7. Granular Customer Sales Audit Report
![Customer Sales Report](images/SalesData1_page-0007.jpg)

---

## 🚀 Corporate Value
This enterprise solution serves as a unified single source of truth for sales directors. By bridging the gap between data engineering structures and visual analytics, it empowers stakeholders to minimize audit times, track field performance instantaneously, and optimize sales targets dynamically.
