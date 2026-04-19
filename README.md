# 📊 Supply Chain & Inventory Optimization Dashboard

## 🚀 Project Overview
An interactive, enterprise-grade Power BI dashboard designed to help supply chain managers and procurement teams monitor inventory health, track supplier performance, and minimize stockout risks. This project moves beyond static reporting by integrating dynamic **"What-If" parameters**, allowing stakeholders to simulate demand spikes and supplier delays in real-time.

---

## 📸 Dashboard Preview
(<<img width="1920" height="1020" alt="Screenshot 2026-04-19 114755" src="https://github.com/user-attachments/assets/81fc26b0-240c-4103-9ac2-45e1e7df0a5b" /><img width="1920" height="1020" alt="Screenshot 2026-04-19 114822" src="https://github.com/user-attachments/assets/1eaaa060-eb9d-404d-b7c0-66f9bfcc7dbd" /><img width="1920" height="1020" alt="Screenshot 2026-04-19 114838" src="https://github.com/user-attachments/assets/059a3404-bdc3-4b87-a7e8-eb4d86d5369f" />


>)

---

## 📉 The Business Problem
Supply chain operations constantly struggle to balance two competing financial forces:
1. **Holding Costs:** Tying up too much capital in excess inventory.
2. **Stockout Risks:** Losing revenue and customer trust due to running out of product.

## 💡 The Solution
This dashboard provides a data-driven solution to this problem by establishing clear Reorder Points (ROP), calculating optimal Safety Stock, and identifying high-risk bottlenecks in the supplier network. 

### Key Features
* **Executive KPI Tracking:** Instant visibility into aggregate metrics including Inventory Turnover, Days of Inventory on Hand (DOH), Fill Rate %, and On-Time Delivery %.
* **Risk Prioritization:** Visualizes the "Critical Few" products—the top 15 items with the highest stockout rates—enabling immediate purchasing action.
* **Fulfillment Heatmapping:** A matrix-based heatmap tracking On-Time Delivery performance across various warehouse locations by month to pinpoint regional bottlenecks.
* **Dynamic Scenario Simulation (What-If Forecasting):** Integrated parameter sliders allow operations teams to simulate demand spikes (up to +50%) or supplier delays. The data model dynamically recalculates Reorder Points and Safety Stock to prescribe necessary inventory adjustments *before* a crisis occurs.

---

## 🛠️ Technical Architecture & Data Model

### Tech Stack
* **Data Visualization & Analytics:** Power BI
* **Data Transformation:** Power Query
* **Dataset Generation:** Python (Pandas, NumPy) for synthetic historical transactional data.

### Data Modeling (Star Schema)
The underlying data model was engineered using a traditional **Star Schema** to ensure optimal DAX query performance and scalability.
* **Fact Table:** `Inventory_Fact_Table` (Transactional inventory movements, closing stock, demand).
* **Dimension Tables:** `Product_Table`, `Location_Table`.
* **Date Table:** Custom DAX-generated calendar table for time-intelligence reporting.

### Advanced DAX Formulations
This project heavily utilizes Data Analysis Expressions (DAX) to drive the analytics engine. Key implementations include:
* **Ratio Calculations:** `DIVIDE()` functions with zero-error handling for Turnover and Fill Rates.
* **Dynamic Thresholds:** `CALCULATE()` and `FILTER()` contexts to isolate Top N high-risk products.
* **Parameter Binding:** Linking disconnected tables to core measures to drive the What-If simulation engine (e.g., `Simulated ROP = (Simulated Daily Demand * Simulated Lead Time) + Simulated Safety Stock`).

---

## 🤝 Let's Connect
Feel free to reach out if you want to discuss this project, data architecture, or BI development!

* **LinkedIn:** *(www.linkedin.com/in/
kunal-k-73762431a
Vanity URL name
)*
