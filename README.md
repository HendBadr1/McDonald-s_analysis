# McDonald's Menu Analytics Dashboard

An interactive Power BI dashboard analyzing McDonald's menu pricing and nutritional data, built end-to-end using Power Query (ETL), DAX, and Power BI Desktop.

---

## 📁 Project Contents

| File | Description |
|---|---|
| `McDonald_s.pbix` | Main Power BI file (data model + dashboard). |
| `dashboard.mp4` | Screen recording demonstrating the dashboard's layout and interactivity. |

---

## 🗂️ Data Source

A single core table named:
```
mcdonalds_menu_20260827_202242(kaggle)
```

### Key columns used in the analysis:
- `category` — food item category (e.g., Burgers, Drinks, Desserts...).
- `calories` — calorie count.
- `protein_g` — protein content in grams.
- `iron_mg` — iron content in milligrams.
- `price_usd` — current price in USD.
- `price_history` — historical price record across years (year / price / change percentage).
- `ava_price` (DAX measure) — average price, shown on a Card visual.

---

## 🧹 Data Preparation Steps (ETL – Power Query)

1. Imported raw data and set correct column data types (Text / Number).
2. Set final data types (Whole Number / Decimal Number) for each resulting column.
3. Verified the full row count (250 items) after cleanup to ensure no data was lost during transformation.

---

## 📊 Dashboard Visuals (Single Page)

| Visual | Metric Displayed |
|---|---|
| Pie Chart | Total calories (`calories`) by `category` |
| Bar Chart | Total price (`price_usd`) by `category` |
| Donut Chart | Total protein (`protein_g`) by `category` |
| Pie Chart (second) | Total iron (`iron_mg`) by `category` |
| Line Chart | Price trend (`price_usd`) over the years (`price_history`) |
| Table | Full item details by `category` |
| Card | Overall average price (`ava_price`) |

---
 Tools Used

- **Power BI Desktop** — data modeling and dashboard design.
- **Power Query Editor** — data cleaning and unpacking (ETL).
- **DAX** — measure calculations (e.g., average price).

---

How to Run

1. Open `McDonald_s.pbix` using **Power BI Desktop** (latest version recommended).
2. If prompted, click **Refresh** from the Home tab to reload the data.
3. To preview the dashboard in action without opening the file, watch `dashboard.mp4`.

---

## 📌 Notes

- All visuals are laid out on a **single page** combining a nutritional and pricing overview of the menu.
