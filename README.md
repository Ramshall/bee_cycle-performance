# bee cycle-performance (Sales & Customer Analytics)

## Project Overview
This project presents a comprehensive analysis of sales, **product**, and customer data from "**Beecycle**" using Microsoft Power BI. The **main goal is to provide actionable insights and create interactive dashboards to visualize** business performance, customer profiling, and product sales trends.

**The project consists of three distinct dashboards, each focusing on key aspects:**
### **Overview(Sales & Profit): Track key sales and profitability metrics year-over-year**
![image](https://github.com/user-attachments/assets/570cbbfe-ce2a-495b-9f28-e08274122d1c)
### **Customers: Analyzes customer demographics and purchasing behavior**
![image](https://github.com/user-attachments/assets/0aef88eb-a1a4-4e04-8cb0-451fd45a6316)
### **Produtct: Identifies top-selling products and quantity sales trends**
![image](https://github.com/user-attachments/assets/9003c9f6-54c8-4076-bb55-bdec8264ed75)

---

## Repo Content
* Power BI File: Muhammad Ramadhani - Web Dashboard.pbix
* File Report with .pdf: Dashboard Beecycle Performance.pdf

**Note:** This project primarily focuses on data visualization and analysis using Power BI. The raw data processing (EDA) aspect is handled within Power Query Editor or DAX in the `.pbix` file, rather than separate scripts or notebooks.

---
## Key Methodologies & DAX Examples
In the Power BI file, multiple DAX (Data Analysis Expressions) formulas were utilized to create various calculations for comparing metrics like sales, profit, and customer growth.

For example, to calculate the net profit from the previous year for Year-over-Year (YoY) comparisons:

```text
past_year_netprofit = 
CALCULATE(
    [current_year_total_net_profit],
    SAMEPERIODLASTYEAR('record_order_date'[Date])
)
```
```text Label for card
past_year_subtitle_text_np = 
FORMAT([yoy%_netprofit], "+0.0%;-0.0%;0.0%")
     & " vs. " &

     SELECTEDVALUE(record_order_date[Year])-1
```

This measure then helps generate dynamic subtitle text for cards, indicating the percentage difference against the prior year:

For a comprehensive review of all DAX measures and calculated columns used in this project, please open the .pbix file.

---

## Project Demo
This dashboard interactive depends on slicer or filer, To see and understand, you can check a short video demo on this:
These dashboards are highly interactive, designed to respond to slicers and filters for dynamic data exploration. To see the full interactivity and functionality, please watch a short video demo:
* [Demo Dashboard](https://drive.google.com/file/d/15Hoh3n6lUfvlPKF8i8tC2QZErxo7khVo/view?usp=sharing)

---

## Tools
* Power BI
* Key concept: Power Querym DAX, and Data Modelling

  
