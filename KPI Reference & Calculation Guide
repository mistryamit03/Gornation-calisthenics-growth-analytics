# 📊 KPI Reference & Calculation Guide  
*Part of the GORNATION Callisthenics Growth Analytics Project*  

This document outlines the **key metrics and calculated fields** used across the Marketing, Inventory, Customer, and Fulfillment dashboards.  
Each KPI includes its **formula**, **purpose**, and **business interpretation** — bridging data logic and business value.

---

## 🧩 1. Marketing Funnel & ROI KPIs

| KPI | Formula | Description & Business Value |
|------|----------|------------------------------|
| **Impressions** | `SUM(Impressions)` | Total number of ad impressions served across all campaigns. Indicates reach and awareness. |
| **Clicks** | `SUM(Clicks)` | Number of times users clicked ads — measures engagement effectiveness. |
| **Add to Cart** | `SUM(Adds_To_Cart)` | Count of users who added items to cart — reflects mid-funnel conversion. |
| **Purchases** | `COUNT_DISTINCT(Order_ID)` | Completed orders — bottom-funnel conversions. |
| **Conversion Rate (CR)** | `(Purchases / Clicks) * 100` | % of users who purchased after clicking — key indicator of ad-to-sale efficiency. |
| **Click-Through Rate (CTR)** | `(Clicks / Impressions) * 100` | % of impressions resulting in clicks — measures ad creative performance. |
| **Ad Spend** | `SUM(Ad_Spend)` | Total marketing spend across all paid channels. |
| **Revenue** | `SUM(Revenue)` | Total sales value generated. |
| **ROAS (Return on Ad Spend)** | `Revenue / Ad_Spend` | Measures revenue per €1 spent — core marketing efficiency metric. |
| **Profit ROAS** | `Profit / Ad_Spend` | Evaluates real profitability of paid campaigns — beyond top-line revenue. |
| **CAC (Customer Acquisition Cost)** | `SUM(Ad_Spend) / COUNT_DISTINCT(New_Customers)` | Cost to acquire one new customer via paid channels. |
| **Drop-Off % (Funnel)** | `((Stage_N - Stage_N+1) / Stage_N) * 100` | Identifies percentage loss between funnel stages (e.g., Clicks → Add to Cart). |

📈 *Example Insight:*  
TikTok campaigns produced the highest Profit ROAS (1.6), while Google Ads required optimization due to higher CAC and lower conversion rates.

---

## 🏬 2. Inventory & Sales Forecast KPIs

| KPI | Formula | Description & Business Value |
|------|----------|------------------------------|
| **Stock Level** | `SUM(Stock_Level)` | Current quantity of available units per product or category. |
| **Reorder Point** | `SUM(Reorder_Point)` | Minimum threshold for triggering restock. |
| **Days of Inventory** | `(Stock_Level / Avg_Monthly_Sales) * 30` | Estimated number of days current stock will last — identifies products at risk. |
| **Revenue at Risk** | `SUM(Revenue) WHERE Stock_Level < Reorder_Point` | Simulated value of potential lost sales due to stockouts. |
| **Out-of-Stock Rate** | `COUNT(Product WHERE Stock_Level = 0) / COUNT(Product)` | Measures how often items are unavailable for sale. |

📦 *Example Insight:*  
Resistance Bands and Liquid Chalk were nearing reorder points, indicating **€8,000 revenue at risk** due to understocking.

---

## 🧍‍♂️ 3. Customer Segments & Retention KPIs

| KPI | Formula | Description & Business Value |
|------|----------|------------------------------|
| **New Customers** | `COUNT_DISTINCT(Customer_ID WHERE Customer_Type = "New")` | First-time buyers; measures acquisition success. |
| **Returning Customers** | `COUNT_DISTINCT(Customer_ID WHERE Customer_Type = "Returning")` | Repeat buyers; signals brand loyalty. |
| **Repeat Purchase Rate (RPR)** | `Returning_Customers / Total_Customers` | % of customers who purchased more than once. |
| **Customer Lifetime Value (LTV)** | `Revenue / Total_Customers` | Average value generated per customer; helps evaluate retention ROI. |
| **Churn Rate (Simulated)** | `(Lost_Customers / Total_Customers) * 100` | % of customers not returning after a set period — key for retention strategy. |

🧠 *Example Insight:*  
GORNATION’s simulated RPR of **0.92** highlights strong loyalty among repeat buyers, driven by brand engagement and community trust.

---

## 🚚 4. Fulfillment & Delivery KPIs

| KPI | Formula | Description & Business Value |
|------|----------|------------------------------|
| **Average Fulfillment Time (hrs)** | `AVG(Delivery_Time_Days * 24)` | Measures time between order placement and dispatch — key efficiency metric. |
| **On-Time Delivery %** | `(COUNT_IF(Delivery_Status = "On-Time") / COUNT(Order_ID)) * 100` | Tracks timely deliveries; reflects fulfillment reliability. |
| **Return Rate %** | `(COUNT_IF(Return_Flag = "Yes") / COUNT(Order_ID)) * 100` | Measures rate of product returns — quality, fit, or logistics issue indicator. |
| **Cost per Shipment** | `SUM(Shipping_Cost) / COUNT_DISTINCT(Customer_ID)` | Average cost to ship per customer — combines logistics efficiency and cost control. |
| **Profit Margin %** | `((Revenue - COGS - Shipping_Cost) / Revenue) * 100` | Measures net profit after product and delivery costs. |
| **Fulfillment Efficiency Index (Simulated)** | `(On_Time_Delivery% - Return_Rate%)` | Composite metric evaluating overall fulfillment health. |

🚀 *Example Insight:*  
On-time delivery rate improved from **78% to 92%** after optimizing handling times, but returns remained higher (11%) in non-EU markets due to customs and packaging friction.

---

## 📎 Reference
This documentation supports the dashboards featured in the `docs/` folder and the Looker Studio report:
- [Marketing & Fulfillment Dashboard (Live)](YOUR_DASHBOARD_LINK_HERE)

---

## 👤 Author
**Amit Mistry**  
Data Analyst | E-Commerce, Marketing & Fulfillment Analytics  
📍 Berlin, Germany | Open to relocating to Münster  
📧 [your.email@example.com] | [LinkedIn](your-linkedin-url)
