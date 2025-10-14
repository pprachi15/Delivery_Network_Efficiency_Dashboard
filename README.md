# 🚚📦 Delivery Network Efficiency Dashboard 
A full-scale **Amazon-inspired logistics dashboard** built in Tableau to analyze delivery network performance across carriers, warehouses, and routes.  
The dashboard visualizes **cost efficiency, delivery time, and reliability** — giving end-to-end insights into operational bottlenecks.

## [Dashboard link](https://public.tableau.com/views/DeliveryNetworkEfficiency/DeliveryNetworkEfficiencyDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

<img width="1854" height="833" alt="image" src="https://github.com/user-attachments/assets/f9a8d7c1-d4b9-47fb-80da-9d7f99d98fe0" />

---

## 🚀 Project Overview

This Tableau project helps answer key business questions:
- Which **carriers** are most **cost-efficient** per mile and kilogram?
- Which **warehouses** have the **longest transit times**?
- How has **delivery speed** changed month over month?
- Where do **on-time rate** and **loss ratio** conflict?

Built with synthetic data (~2,000 shipments) to simulate an Amazon-like last-mile delivery network.

---

## 🧱 Dataset

**File:** `logistics_shipments_dataset.csv`  
**[Kaggle Link](https://www.kaggle.com/datasets/shahriarkabir/us-logistics-performance-dataset?resource=download&select=logistics_shipments_dataset.csv)** <br> 
**Records:** 2,000+ rows (synthetic)  
**Fields:**
| Column | Description |
|--------|--------------|
| Shipment ID | Unique shipment identifier |
| Shipment Date | Dispatch date |
| Delivery Date | Date of delivery completion |
| Origin Warehouse | Warehouse dispatch location |
| Destination | Delivery destination city |
| Carrier | Delivery provider (Amazon Logistics, UPS, FedEx, DHL, USPS, OnTrac, LaserShip) |
| Status | Shipment state (Delivered, In Transit, Lost) |
| Distance miles | Total distance per shipment |
| Weight kg | Shipment weight |
| Cost | Total shipment cost |

> 🧠 *Dataset is synthetic and used for learning & analytics demonstration.*

---

## 📊 KPIs Displayed

| KPI | Formula | Description |
|------|----------|-------------|
| **Total Shipments** | `COUNTD([Shipment ID])` | Distinct shipments processed |
| **Avg Transit Days** | `AVG([Transit Days])` | Average delivery duration |
| **Avg Cost/Mile** | `SUM([Cost]) / SUM([Distance miles])` | Cost efficiency per distance |
| **Avg Cost/Kg** | `SUM([Cost]) / SUM([Weight kg])` | Cost per weight efficiency |

🧠 Insights Derived
--
🏢 Warehouse_BOS shows the slowest average delivery (4.5 days) → optimization needed. <br>
🚚 FedEx and UPS lead in cost per mile efficiency. <br>
📦 Amazon Logistics handles the largest share of shipments. <br>
🔥 SEA and MIA warehouses have the highest loss ratios (3–5%). <br>
📈 Delivery speed improved in Q3, slight drop in holiday months. <br>
