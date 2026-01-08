# Making vs. Buying Decision Analysis – Power BI

## 📌 Project Overview
This project is an end-to-end **Power BI decision-support dashboard** designed to analyze **Make vs. Buy strategies**, supplier selection, and cost optimization under different production volume scenarios.

It simulates real-world procurement and manufacturing decisions by combining supplier quotes, internal manufacturing capacity, non-recurring expenses, and scenario-based analysis.

---

## 🎯 Business Objectives
- Identify the **lowest-cost supplier** by part and production volume  
- Compare **internal manufacturing (Make)** vs **external sourcing (Buy)**  
- Calculate **full cost**, including non-recurring expenses  
- Enable **what-if scenario planning** using dynamic parameters  
- Support data-driven strategic decisions  

---

## 📊 Dashboard Pages

### 1️⃣ Supplier Selection
- Supplier comparison based on:
  - Unit cost
  - Production volume
  - Non-recurring expenses
- Full cost breakdown per supplier
- Dynamic filtering by:
  - Part number
  - Volume

---

### 2️⃣ Scenario Planner
- Interactive **What-If Parameter** to control production volume
- Automatic recalculation of:
  - Full cost
  - Lowest-cost supplier
- Trend analysis across different volume ranges
- Designed for scenario-based decision making

---

### 3️⃣ Making vs. Buying Analysis
- Make vs Buy recommendation per part
- Cost avoidance calculation
- Manufacturing capacity and machine constraints
- Capital investment requirements for Make scenarios
- Supplier comparison for Buy scenarios

---

## 🧮 DAX Concepts & Logic

### ✔ What-If Parameters
- Used to dynamically control production volume
- Enables real-time scenario planning and sensitivity analysis

### ✔ MINX Function
- Used to identify the **lowest-cost supplier** dynamically
- Evaluates cost measures across suppliers for each scenario

### ✔ Key Measures
- Full Cost  
- Buy Scenario Full Cost  
- Make Scenario Full Cost  
- Cost Avoidance  

### 🔍 Example Logic (Simplified)
```DAX
Full Cost (All) "Buy" = MINX(FILTER(Quotes, Quotes[Volume] <= MIN('Scenario Volumes(All)'[Scenario Volume])), (Quotes[Unit_Cost] * MIN('Scenario Volumes(All)'[Scenario Volume])) + Quotes[Non_recurring_expenses])
```
## 🛠 Tools & Technologies

- Power BI Desktop

- DAX (MINX, Measures, What-If Parameters)

- Data Modeling (Star Schema)

- Scenario & Cost Analysis

### 🚀 How to Use

1. Download the .pbix file

2. Open it in Power BI Desktop

3. Use the scenario volume slider to simulate different production levels

4. Review supplier ranking and Make vs Buy recommendations

### 📌 Use Cases

- Procurement and sourcing optimization

- Manufacturing and cost analysis

- Strategic planning and PMO analysis

- Portfolio and interview demonstration

### 📬 Contact

If you would like to discuss this project, provide feedback, or explore real-world applications, feel free to connect with me on LinkedIn.
