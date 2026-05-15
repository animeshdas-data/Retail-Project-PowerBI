# Retail Sales Analytics Dashboard — Power BI

Hi! I'm a fresher data analyst and this is one of my first Power BI projects. I built this retail sales dashboard to practice data modeling, DAX measures, and report design. I'm sharing it here so others can learn from it or use it as a starting point.

---

## 📌 About This Project

I created this dashboard to analyze retail sales data. The report helps answer questions like:
- How much revenue and profit did we generate?
- How are we performing compared to last year?
- Which categories, brands, and stores are doing well?
- How many days does delivery take on average?

Everything is interactive — you can filter by year, month, quarter, category, brand, and store.

---

## 🗂️ Data Model

I used two tables in this project:

| Table | Description |
|---|---|
| `RETAIL_SALES` | The main table — contains all order-level sales data |
| `DateTable` | A custom date table I created for time-based analysis |

I connected them by linking `Order_Date` in `RETAIL_SALES` to `Date` in `DateTable`.

### Columns in RETAIL_SALES

| Column | Description |
|---|---|
| Order_ID | Unique ID for each order |
| Order_Date | When the order was placed |
| SKU | Product code |
| Product | Product name |
| Category | Product category |
| Sub_Category | Product sub-category |
| Brand | Brand name |
| Fulfilment | How the order was fulfilled |
| Quantity | Number of units sold |
| Currency | Currency of the transaction |
| Sale_Price | Price at which it was sold |
| Mrp | Maximum retail price |
| Cost_Price | Cost to the seller |
| promotion-ids | Any promotions applied |
| Customer_ID | Customer identifier |
| Store_ID | Which store handled the order |
| Delivery_Date | When it was delivered |
| Delivery_Days | How many days delivery took |

---

## 📐 DAX Measures I Created

This was the part I learned the most from! Here are all the measures I wrote:

**Revenue & Profit**
- `Total_Revenue` — multiplies Sale_Price by Quantity for every row and sums it up
- `Total_Profit` — subtracts Cost_Price from Sale_Price, multiplies by Quantity, and sums it
- `Revenue YTD` — running total of revenue from the start of the year

**Year-over-Year Comparison**
- `Revenue Last Year` — revenue from the same period in the previous year
- `Profit Last Year` — profit from the same period in the previous year
- `Revenue Growth%` — how much revenue grew compared to last year (as a percentage)
- `Profit Growth%` — how much profit grew compared to last year (as a percentage)

**Operational**
- `Avg_Delivery_Days` — average number of days taken to deliver an order

---

## 📊 What's on the Dashboard

I designed a single-page report with 16 visuals:

**KPI Cards** — show the most important numbers at a glance
- Total Revenue
- Total Profit
- Average Delivery Days
- Revenue Growth %
- Profit Growth %

**Charts**
- Line chart — Revenue vs Last Year, month by month
- Line chart — Average Delivery Days over months
- Bar chart — Revenue & Profit Growth % by Category
- Bar chart — Total Profit by Brand
- Bar chart — Revenue, Profit & Growth by Store

**Slicers (so you can filter everything)**
- Year, Quarter, Month, Category, Brand, Store ID

---

## 🚀 How to Use This

1. Download the `Retail_Project_PowerBI.pbit` file
2. Open it in **Power BI Desktop** (free to download from Microsoft)
3. Connect your own retail sales data that matches the column structure above
4. Hit refresh — the report will populate with your data!

> This is a `.pbit` template file, which means it has no data in it. You need to connect your own data source to use it.

---

## 🛠️ What I Used

- **Power BI Desktop** — for building the report and data model
- **DAX** — for writing the measures
- **Power Query** — for data transformation

---

## 🌱 What I Learned

- How to build a proper data model with fact and dimension tables
- How to write DAX measures including time intelligence functions like `TOTALYTD` and `SAMEPERIODLASTYEAR`
- How to design a clean, interactive dashboard with slicers and KPI cards

---

## 📁 Files in This Repo

```
├── Retail_Project_PowerBI.pbit   # The Power BI template
└── README.md                     # This file
```
## 📁 Files Screenshot / Demo
-[Dashboard Preview].(https://github.com/animeshdas-data/Retail-Project-PowerBI/blob/main/Retail%20Sales%20Project%20Snap.jpg)
---

*This is one of my beginner projects. Feedback and suggestions are always welcome! 😊*
