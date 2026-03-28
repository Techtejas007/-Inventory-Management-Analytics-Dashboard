# 📦 Inventory Management Analytics Dashboard

> A focused Power BI KPI dashboard that monitors supply-demand gaps, stock shortages, profit/loss metrics, and daily availability — helping operations and supply chain teams stay ahead of inventory risks.

---

## 📌 Problem Statement

Inventory management teams in retail and distribution face constant challenges:
- Stock-outs due to demand exceeding supply
- Overstock situations that lead to dead capital
- Lack of real-time visibility into daily availability vs. demand
- Difficulty quantifying the financial impact of supply shortages

This dashboard surfaces those KPIs instantly, enabling proactive inventory decisions.

---

## 🖥️ Dashboard

| Page | Description |
|------|-------------|
| **Inventory Overview** | 6 KPI cards covering availability, demand, shortage, loss, profit, and daily loss |

---

## 🔍 Key KPI Cards

| Metric | Purpose |
|--------|---------|
| **Average Availability Per Day** | Baseline stock available for fulfillment |
| **Average Demand Per Day** | Customer demand signal to compare against supply |
| **Total Supply Shortage** | Cumulative gap between demand and supply |
| **Total Loss** | Revenue/value lost due to unfulfilled demand or wastage |
| **Total Profit** | Net profit after accounting for losses |
| **Average Loss Per Day** | Daily financial burn from inventory gaps |

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| **Power BI Desktop** | KPI card layout and report design |
| **DAX** | Calculated measures for averages, totals, and shortage logic |
| **Power Query (M)** | Data transformation and date-level aggregations |

---

## 📊 Key DAX Measures

```dax
Average Availability Per Day = AVERAGEX('Inventory', 'Inventory'[Available Stock])

Total Supply Shortage = SUMX('Inventory', MAX('Inventory'[Demand] - 'Inventory'[Supply], 0))

Average Loss Per Day = DIVIDE([Total Loss], DISTINCTCOUNT('Inventory'[Date]))
```

---

## 💡 Business Impact

- Gives **operations managers** a daily snapshot of stock health without digging into raw data
- Enables **procurement teams** to trigger reorder points based on shortage trends
- Helps **finance teams** quantify the cost of supply chain failures
- Supports **demand planning** by comparing average demand vs. average availability over time

---

## 📁 File

| File | Description |
|------|-------------|
| `Inventory_Project.pbix` | Power BI report file |

---

## 🚀 How to Use

1. Download `Inventory_Project.pbix`
2. Open in **Power BI Desktop**
3. Review KPI cards for a quick health check of your inventory
4. Connect your own data source by replacing the dataset in Power Query

---

## 👤 Author

**Tejas Bafna** — Data Analyst | Power BI Developer  
📧 tejasbafna311@gmail.com · [LinkedIn](www.linkedin.com/in/tejas-bafna) · 
