
# 📊 DAX Depo – Power BI Project (PR 3)

## 📌 Project Brief
This project is based on the official **PR.3 DAX Depo** assignment shared by the Business Analyst Manager.
The goal of the project is to build a **backend data model** and perform **advanced analytical calculations using DAX in Power BI**, while avoiding external visuals.

All results are displayed **only using Matrix visuals**, as clearly mentioned in the project instructions.

---

## 🧾 Business Requirement Summary
- Build advanced DAX calculations on **Sales and Returns model**
- Use DAX instead of visual-level calculations
- Focus on **filter context, time intelligence, and iterators**
- Use **Matrix visual only** to present results

---
**##** 🔗  **Data Model (Tables & Links)**

- Below are the key tables used in this project. Click the table names to explore their purpose and structure.
 
  -[DAX_Depo_Sample_Datasets.xlsx](./DAX_Depo_Sample_Datasets.xlsx)

## 🗂 Dataset Tables Used

As shown in the provided document and model screenshot, the following tables are used:

### 🔹 Fact Tables
- **Sales_Fact**
  - Sales transactions
  - Contains ProductID, CustomerID, DateKey, RegionID, Cost, Quantity

- **Returns_Fact**
  - Returned item details
  - Linked with Sales_Fact using SalesID

### 🔹 Dimension Tables
- **Customer_Dim**
  - CustomerID, FirstName, LastName
  - Calculated Column: *Customer Full Name*

- **Product_Dim**
  - ProductID, ProductName, Category, Cost

- **Date_Dim**
  - Date, Month, MonthName, Quarter, Year
  - Used for all time-based calculations

- **Region_Dim**
  - RegionID, RegionName

---

## 🔗 Data Model & Relationships
The data model follows a **star schema** design:
- One-to-many relationships between dimension tables and fact tables
- Date_Dim is connected to both Sales_Fact and Returns_Fact
- Proper relationship direction maintained for filter flow

---

## 🧮 DAX Implementation (As per Assignment)

### ✅ Calculated Columns
- **Profit** → SalesAmount − Cost
- **Return Flag** → Returned / Not Returned
- **Customer Full Name** → FirstName & LastName combined

### ✅ Measures Created
- Total Sales
- Total Cost
- Total Profit
- Return Rate (% of items returned)
- Average Sale per Transaction

### ✅ Filter Context & Functions
- `ALL()`
- `FILTER()`
- `CALCULATE()`

### ✅ Time Intelligence (Matrix-based)
- `TOTALYTD()`
- `SAMEPERIODLASTYEAR()`
- `DATESINPERIOD()`
- Running Total using `DATESBETWEEN()`

### ✅ Additional DAX Usage
- Conditional logic using `IF()` and `SWITCH()`
- Aggregations using `SUMX()` and `AVERAGEX()`

---

## 📊 Matrix Visual Outputs

As per instructions, **only Matrix visuals** are used.

### 🔹 Matrix – Sales, Returns & Metrics by Product

<img width="861" height="514" alt="Screenshot 2025-12-29 131433" src="https://github.com/user-attachments/assets/e4fce625-dc9e-4509-b6e5-52405bf8a78d" />


### 🔹 Matrix – Time Intelligence & Running Total
- Sales YTD
- Last Year Sales
- Running Total

---

## 🧩 Region-wise Analysis
Matrix comparison created to analyze:
- Total Sales by Region
- High Sales using filter context

---

## 🖼 Data Model Screenshot

<img width="1146" height="842" alt="Screenshot 2025-12-22 223350" src="https://github.com/user-attachments/assets/5badbb26-8b32-4380-b9ff-f02e936be632" />

---

## 📁 Project Files
- **POWER BI Project-3.pbix**
- **README.md**

---

## 📌 Output Rules Followed
✔ Matrix visual only  
✔ Grouped by Region, Month, Product Category  
✔ No charts or other visuals used  

---

## 👤 Author
**Janki Dholariya**  
Power BI | DAX | Data Analytics  

---
