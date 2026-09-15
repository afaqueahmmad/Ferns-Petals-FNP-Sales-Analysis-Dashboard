# Ferns-Petals-FNP-Sales-Analysis-Dashboard
An end-to-end Excel-based Business Intelligence project analyzing sales, customer, and delivery performance for Ferns & Petals — a gifting company operating across occasions like Diwali, Raksha Bandhan, Holi, Valentine's Day, Birthdays, and Anniversaries.

---

##  Project Overview

This project simulates a real-world analyst workflow: raw, fragmented data was ingested, consolidated into a single master table, modeled, and visualized into an interactive one-page dashboard to answer key business questions around revenue, customer behavior, and delivery performance.

**Type:** Business Intelligence / Data Analytics (Excel)
**Tools:** Excel, Power Query, XLOOKUP, Pivot Tables & Charts, Slicers

---

##  Business Problem

FNP needed a unified view to answer:
- What is the overall revenue and order volume?
- How long does it take for orders to be delivered on average?
- How do sales fluctuate month-to-month across 2023?
- Which products and categories generate the most revenue?
- How much are customers spending on average?
- Which cities place the highest number of orders?
- Does order quantity impact delivery time?
- How does revenue compare across occasions?
- Which products are most popular for specific occasions?

The raw data was split across multiple unlinked files/sheets — not analysis-ready out of the box.

---

##  Data Preparation & Modeling

### 1. Automated Data Ingestion — Power Query (`From Folder`)
Used Excel's **Get Data → From Folder** to pull in all source files as a single connected, refreshable query — instead of manually opening and copy-pasting each file. This makes the pipeline scalable: adding a new data file to the folder and refreshing the query updates the entire dataset automatically.

### 2. Data Consolidation — XLOOKUP-based Master Table
- Set the **Orders sheet as the master/fact table**, following standard data-modeling practice (Orders is the transactional table all other data relates to).
- Used **XLOOKUP** to pull in relevant fields (product details, category, customer info, delivery dates) from other sheets into the Orders master, matched on common keys (Order ID, Product ID).
- This produced a single, flattened source of truth — effectively replicating a SQL `JOIN` / Power BI merged query, done natively in Excel.

> This step reflects a common real-world analyst task: business data rarely arrives clean and merged — building the join logic yourself is part of the job.

---

##  Dashboard Components

| Component | Description |
|---|---|
| **KPI Cards** | Orders Placed (1,000), Total Revenue (₹35,20,984), Avg Order-Delivery Time (5.53 days), Avg Customer Spending (₹3,520.98) |
| **Revenue by Occasion** | Bar chart comparing Anniversary, Raksha Bandhan, Holi, Birthday, Valentine's Day, Diwali |
| **Revenue by Category** | Bar chart ranking Colors, Soft Toys, Sweets, Cake, Raksha Bandhan, Plants, Mugs |
| **Top 10 Revenue by Hour** | Line chart of order-time revenue, peaking in the evening (6–8 PM) |
| **Revenue by Month** | Monthly trend line highlighting seasonal spikes |
| **Top 5 Revenue-Generating Products** | Bar chart: Magnam Set, Quia Gift, Dolores Gift, Harum Pack, Deserunt Box |
| **Top 10 Cities by Order Volume** | Bar chart led by Imphal, Dhanbad, Kavali, Haridwar |
| **Interactive Slicers** | Order_Date, Delivery_Date (monthly), and Occasion — filters all visuals dynamically |

**Techniques used:** Pivot Tables, Pivot Charts, cross-linked slicers (report connections), conditional formatting for KPI cards, single-screen dashboard layout.

---

##  Key Insights

- **Anniversary** and **Raksha Bandhan** are the top revenue-generating occasions, together driving a large share of total sales.
- **Colors** is the dominant category (~₹10L revenue) — nearly double the next-highest category, Soft Toys.
- **Evening hours (6 PM–8 PM)** show the highest order revenue, useful for timing promotions or staffing customer support.
- **February and August** show sharp revenue spikes, aligned with Valentine's Day and Raksha Bandhan — confirming strong seasonal demand.
- **Imphal, Dhanbad, and Kavali** lead in order volume — smaller/non-metro cities outperforming expectations, useful for regional marketing/logistics decisions.
- **Average delivery time of 5.53 days** provides a baseline to track logistics performance over time.

---

##  Skills Demonstrated

`Excel (Advanced)` `Power Query (Get & Transform)` `XLOOKUP` `Data Modeling` `Pivot Tables & Pivot Charts` `Interactive Slicers` `KPI Design` `Data Cleaning & Consolidation` `Business Insight Generation`
