# Enterprise Sales Performance & Target Tracking Dashboard

## 📊 Project Overview
An end-to-end Business Intelligence solution designed to analyze corporate sales data, track regional targets, monitor salesperson performance, and conduct deep customer behavioral analysis. This project simulates an enterprise-level dashboard that translates raw transaction histories into actionable executive insights.

## 🛠️ Tech Stack & Tools
* **Power BI Desktop** (Data Visualization & Dashboarding)
* **Power Query** (ETL - Data Extraction, Transformation, and Loading)
* **DAX (Data Analysis Expressions)** (Advanced Calculations & Time Intelligence)
* **Data Modeling** (Star Schema Architecture)
* **Excel** (Initial Data Inspection)

## 📐 Data Architecture (Star Schema)
The project utilizes a robust **Star Schema** data model optimized for performance and analytical granularity. It connects a central Fact table with multiple Dimension tables:
* **Fact Tables:** `SalesData`, `TargetT`
* **Dimension Tables:** `Calendar` (Date Dimension), `ItemsT` (Products), `SalesmanT`, `CustomerDBT`, `RouteT`, `JP_T`

---

## 🖥️ Dashboard Pages & Features

### 1. Home / Navigation Hub
An intuitive, modern dark-themed landing page with a responsive sidebar menu allowing users to navigate smoothly between different reporting layers.

### 2. KPIs Summary
* High-level executive cards tracking **YTD Sales** ($1.38bn, representing 23.1% YoY growth).
* Comparative metrics for **MTD vs. Last Month** and volume analysis (**QTY MTD**).
* Trend lines visualizing daily sales trajectories to spot operational peaks and drops.

### 3. Sales Overview
* Deep dive into sales distribution segmented by **Region**, **Category**, **Channel**, and **Brand**.
* Top 10 Salesman Leaderboard.
* Matrix summarizing regional variance analysis against last year's performance.

### 4. Region vs. Target & Salesman vs. Target
* Performance tracking tables utilizing conditional formatting (Green/Red indicators) to highlight achievement rates.
* Analysis of **MoM Growth %**, **Average Order Value (AOV)**, and **Drop Size** per salesman.

### 5. Customer Analysis & Sales Report
* Cohort analysis for **27,176 Active Customers** managing **137,380 Total Orders**.
* Visualizations breaking down sales by routes and customer channels to uncover hidden supply chain opportunities.

---

## 📈 Key DAX Formulas Implemented
The dashboard relies heavily on advanced DAX to handle complex time-intelligence, including:
* **YTD Sales & Target Achievements:** Dynamically calculating year-to-date figures against set budgets.
* **YoY / MoM Growth Variances:** Formulating relative variances against `YAGO` (Year Ago) and `MAGO` (Month Ago) baselines.
* **Operational KPIs:** Dynamic averages for order sizing and active customer frequencies.

## 🚀 How to View the Project
1. Clone this repository.
2. Open the `.pbix` file using **Power BI Desktop**.
3. (Optional) If a published link is available, click the **Live Demo** link at the top of the repository.
4. 
