📊 Sales Performance Dashboard – United States

This project presents a comprehensive **Sales Performance Dashboard** for the United States, combining data cleaning in **Microsoft Excel** and data visualization using **Tableau**. The dataset is sourced from **Kaggle** and includes sales, profit, customer, and regional data.

## 📁 Project Overview

* **Objective:** Analyze and visualize U.S. sales data to derive insights on performance by product, state, segment, region, and time.
* **Tools Used:**

  * 💾 **Excel** – Data cleaning & transformation
  * 📈 **Tableau** – Interactive dashboard & visualization
  * 🗂 **Kaggle** – Source of dataset


## 🧹 Data Cleaning (Excel)

1. **Remove Duplicates**

* Used the **Remove Duplicates** option in the Excel **Data tab** to clean customer and order redundancies.

2. **Date Formatting**

* Applied `=TEXT(Order Date, "DD-MM-YYYY")` to ensure consistent date formatting for:

  * Order Date
  * Ship Date

3. **Derived Columns**

Created new calculated columns:

| Column Name          | Formula                                                                  |
| -------------------- | ------------------------------------------------------------------------ |
| Profit Margin        | `=Profit / Sales`                                                        |
| Cost Price           | `=Sales - Profit`                                                        |
| Sales Per Unit       | `=Sales / Quantity`                                                      |
| Profit Per Unit      | `=Profit / Quantity`                                                     |
| Profit Category      | `=IF([Profit Margin]>0.2,"High",IF([Profit Margin]>0.1,"Medium","Low"))` |
| Total Revenue Impact | `=Sales * Quantity`                                                      |

4. **Handling Nulls**

* Used `=COUNTBLANK(F:F)` to check for blank values in **Customer ID**
* Checked all columns: `=COUNTBLANK(A1:AA9995)`

5. **Data Types**

* Ensured:

  * Profit Margin & Discount are in **percentage format**
  * Sales, Cost Price, and Profit are in **currency/number format**

6. **Conditional Formatting**

* Applied color formatting to Profit Margin:

  * `< -1` → 🔴 Red
  * `-1 to 0` → 🟠 Orange
  * `> 0` → 🟢 Green

7. **Month-Year Extraction**

* Used `=TEXT(Order Date, "mmmm yyyy")` for monthly aggregation

8. **Pivot Tables Created**

* Sales & Profit by Region
* Sales & Profit by Segment
* Top 10 Products by Sales
* Sales by Category & Sub-category

---

## 📊 Tableau Dashboard Insights

### 📌 Key Metrics:

* **Sales:** 2,297,201
* **Profit:** 286,397
* **No. of Customers:** 9,994
* **Profit Margin:** 1,202

### 📈 Visualizations:

* **Quarter Selector** for time-based filtering
* **Sales by Month** line chart for trend analysis
* **Sales by Product** bar chart
* **Sales by State** map visualization
* **Customer Order Distribution** histogram
* **Sales by Segment** donut chart
* **Sales by Region** treemap

---

## 📂 Folder Structure

```
├── Final Dashboard.png       # Tableau dashboard image
├── Cleaned_Data.xlsx         # Cleaned and prepared dataset (optional to upload)
├── README.md                 # Project description
```

---

## ✅ How to Use

1. Clone the repository.
2. Review the `Final Dashboard.png` for insights.
3. Open the Excel sheet to review cleaning logic and pivot tables.
4. Use Tableau to explore or build additional visualizations.

---

## 📌 Dataset Source

* [Kaggle – Sales Data]

---

## 📧 Contact

For questions, feedback, or collaboration, feel free to reach out @purandhar2000@gmail.com

---
