# ☕ Coffee Sales Analysis: Relational Data & Interactive Dashboard

## 📊 Executive Summary
This project transforms a multi-table relational dataset into a functional business intelligence tool. Using **Excel**, I performed data modeling to link customer demographics and product specifications with transaction logs, resulting in a dynamic dashboard that tracks global coffee sales, product popularity, and customer loyalty.

---

## 🛠️ Technical Skills Demonstrated
* **Advanced Lookups:** Dual implementation of `INDEX & MATCH` and `XLOOKUP` for complex, non-volatile data retrieval across multiple sheets.
* **Data Modeling:** Established relationships between `Orders`, `Customers`, and `Products` (similar to a SQL Join).
* **Data Cleaning:** * Standardized date formats and currency.
  * Handled missing data in customer contact fields.
  * Used `IF` logic to clean and categorize coffee roast types and sizes.
* **Aggregated Analysis:** Created summary tables for `Total Sales`, `Sales by Country`, and `Top 5 Customers`.
* **Dynamic Visualization:** Built an interactive dashboard with Slicers and Timelines.

---

## 📁 File Structure & Data Dictionary
The analysis is built upon a relational structure across the following data files:

| File / Sheet | Description | Key Fields |
| :--- | :--- | :--- |
| **Orders** | The central transaction table. | Order ID, Date, Customer ID, Product ID, Quantity. |
| **Customers** | Detailed customer profiles. | Name, Email, Country, Loyalty Card Status. |
| **Products** | Technical product catalog. | Coffee Type, Roast, Size, Unit Price, Profit. |
| **Analysis Sheets** | Aggregated pivot data. | TotalSales, SalesbyCountry, Top5Customers. |

---

## ⚙️ The Transformation Workflow

### 1. The "Join" Process
To create a master table for analysis, I used:
* **`INDEX MATCH`**: To pull `Customer Name` and `Country` into the Orders sheet (chosen for its flexibility with large datasets).
* **`XLOOKUP`**: To quickly map `Unit Price` and `Coffee Type` from the Products sheet to calculate line-item revenue.

### 2. Strategic Cleaning
I converted abbreviated data (e.g., "Rob" to "Robusta", "L" to "Large") to ensure that the final dashboard charts were professional and easy for a non-technical stakeholder to read.

### 3. Business Logic
I calculated **Total Revenue** by creating a calculated column:
`[Quantity] * [Unit Price]`
Then, I used Pivot Tables to isolate the top 5 customers by total spend to identify high-value loyalty targets.

---

## 📈 Dashboard Insights
* **Top Market:** The **United States** consistently leads in sales volume, followed by Ireland.
* **Product Preference:** **Arabica** and **Excelsa** are the highest-grossing coffee types.
* **Temporal Trends:** Sales show specific seasonal peaks, visible through the monthly timeline slicer.

---

## 🚀 How to Replicate
1. Download the `Dashboard.xlsx` and the `Clean_dataset.xlsx`.
2. Open the Dashboard file; the **Slicers** on the left allow you to filter by Roast Type, Size, and Loyalty status.
3. Review the **Analysis Sheets** to see the raw Pivot Table calculations that drive the visuals.

---

## 👨‍💻 Author
Dharmesh Makwana
