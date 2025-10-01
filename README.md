# 📊 Sales Performance Dashboard (Power BI)

This repository showcases a **Sales Dashboard Project** developed using Power BI.  
It demonstrates how to transform raw transactional data into actionable insights through **data cleaning, modeling, and visualization**.  

---

## 🔑 Key Focus Areas
- **Data cleaning & preprocessing** in Power Query  
- **Data modeling** using a Star Schema strategy  
- **Building measures in DAX** for profitability and performance analysis  
- **Interactive dashboards & visuals** for executives to enhance decision-making  

---

## 📂 Repository Structure  

- 📂 **PowerBI-Sales-Performance-Dashboard**
  - 📄 **README.md** → Project documentation (this file)  
  - 📊 **Sales Dashboard Final.pdf** → Final dashboard visuals  
  - 🖼️ **Notes.png** → Power Query process snapshot  
  - 🖼️ **Data Modelling.png** → Data modeling diagram  
    
---

## 🛠️ Tools & Technologies
- **Power BI Desktop** → Dashboarding & reporting  
- **Power Query** → Data cleaning & transformation  
- **DAX (Data Analysis Expressions)** → Custom measures & KPIs  
- **Star Schema** → Data modeling best practices  

---

## 📊 Project Workflow

### 1. Data Cleaning (Power Query)
- Merged multiple tables (*Sales, Customers, Products, Territories, Returns*) into a unified dataset  
- Standardized column names & applied consistent data types  
- Created calculated columns:  
- Removed duplicates & handled missing values  
- Applied **business-friendly naming conventions** for usability  
<img width="952" height="359" alt="Data Transformation" src="https://github.com/user-attachments/assets/091485c7-de78-45a4-89a4-0c886882c88d" />
Snapshot of the **data cleaning and transformation** steps in Power Query, including merging tables, handling missing values, and applying calculated columns.

---

### 2. Data Modeling
- Built a **Star Schema** with clear relationships  
- **Fact Table**: Sales (Order transactions)  
- **Dimension Tables**: Calendar, Products, Customers, Territory, Returns  
- Established **1-to-many relationships** between fact & dimensions for optimized reporting  
<img width="850" height="335" alt="Data Modeling" src="https://github.com/user-attachments/assets/072a129c-2049-467f-9238-9dfff374e0f8" />
Visualization of the **Star Schema** data model with fact and dimension tables, ensuring optimized reporting and relationships.

### 3. Visualization & Measures (DAX)
- Developed key measures in **DAX** to drive insights:

- `G MarginPYTD = CALCULATE([Total GM], DATESYTD(SAMEPERIODLASTYEAR('Calendar Table'[Date])))`  
- ```DAX
  Growth Format = 
      VAR _variance = [Growth]
      Return
          Format(_variance,"#%") & " " & IF(_variance > 0, "▲", "▼")
 
- Key visuals included:  
  - **Overall Sales Performance** – Revenue, Profit, Margins, Return rates  
  - **Regional Performance** – Sales by City & Country (Kenya, Uganda, Tanzania)  
  - **Product Mix Analysis** – Revenue & Volume contribution by categories  
  - **Top Customers** – Contribution to revenue and profit  
  - **Trend Analysis** – Monthly/Seasonal trends in revenue and volume
[Sales Dashboard Final.pdf](https://github.com/user-attachments/files/22632081/Sales.Dashboard.Final.pdf)

### 📈 Key Insights & Recommendations
- **Expand Geographically** – Strong traction in Kenya (Nairobi, Mombasa, Eldoret, Nakuru) and early momentum in Uganda (Kampala, Gulu) and Tanzania (Arusha, Dodoma) highlight opportunities for deeper market penetration.  
- **Sustain Profitability through Cost Discipline** – Gross profit grew by 52% (KES 3.97M) due to cost management. Continued margin protection will be crucial for scaling.  
- **Leverage Customer Concentration** – Top 10 customers contributed ~KES 9.3M revenue. Building stronger key-account relationships will enhance retention and loyalty.  
- **Diversify Beyond Fish Products** – Fish remains 70% of volume, but diversifying into high-margin categories (like dairy meal, drought pellet, maxi meal) will mitigate dependency risk and stabilize growth.  

✅ This project demonstrates applied skills in **Business Intelligence (BI)**, **Data Analytics**, and **Visualization**, designed as a portfolio-ready case study.
