# Transforming Raw Hospital Data into Actionable Insights  

![dashboard](https://github.com/AbdurRoqeeb/Transforming-Raw-Hospital-Data-into-Actionable-Insights-with-Microsoft-Excel-Power-Query/blob/main/dashboard.png?raw=true)

## Table of Contents
- [Overview](#overview)  
- [Project Goals](#project-goals)  
- [Data Preparation](#data-preparation)  
  - Step 1: Isolate Data Entities  
  - Step 2: Clean Patient Names  
  - Step 3: Add Length of Stay  
- [Building Dimension Tables](#building-dimension-tables)  
  - Step 4: Create Dimension Tables  
  - Step 5: Add Derived Columns  
- [Building the Fact Table](#building-the-fact-table)  
  - Step 6: Create Fact Table  
  - Step 7: Create Date Table  
- [Data Modeling](#data-modeling)  
  - Step 8: Build Data Model with Relationships  
- [Conclusion & Next Steps](#conclusion--next-steps)  
- [Technologies Used](#technologies-used)  


---

## Overview
This project demonstrates how a raw hospital dataset can be transformed into a structured, analytical-ready data model using **Microsoft Excel** and **Power Query** :contentReference[oaicite:2]{index=2}. The end result is a star schema model enhancing data clarity and enabling actionable insights — even within Excel!

---

## Project Goals
- Clean and normalize raw hospital data  
- Model data into fact and dimension tables  
- Support decision-making for hospital administrators, policymakers, and analysts  
- Lay groundwork for scalable dashboards with tools like Power BI :contentReference[oaicite:3]{index=3}

---

## Data Preparation

### Step 1: Isolate Data Entities  
- Duplicate the original worksheet into four copies.  
- Separate out entities: **Patients**, **Doctors**, **Insurance Providers**, preparing for dimension table creation :contentReference[oaicite:4]{index=4}.

### Step 2: Clean Patient Names  
- Normalize names by capitalizing each word.  
- Remove titles (e.g., Mr, Mrs, Dr) for consistency and deduplication :contentReference[oaicite:5]{index=5}.

### Step 3: Add **Length of Stay**  
- Compute by subtracting **Admission Date** from **Discharge Date**.  
- A key metric for evaluating healthcare efficiency :contentReference[oaicite:6]{index=6}.

---

## Building Dimension Tables

### Step 4: Create Dimension Tables  
- Construct separate sheets for:
  - **Patients**  
  - **Doctors**  
  - **Insurance Providers**  
- Assign unique IDs to each record for use in the fact table :contentReference[oaicite:7]{index=7}.
![dim table 1](https://github.com/AbdurRoqeeb/Transforming-Raw-Hospital-Data-into-Actionable-Insights-with-Microsoft-Excel-Power-Query/blob/main/assets/Screenshot%202025-08-20%20021247.png?raw=true)
![dim table 2](https://github.com/AbdurRoqeeb/Transforming-Raw-Hospital-Data-into-Actionable-Insights-with-Microsoft-Excel-Power-Query/blob/main/assets/Screenshot%202025-08-20%20021304.png?raw=true)


### Step 5: Add Derived Columns  
- In **Patients** table, add an **Age Group** column using a DAX-like function via Power Query.  
- Enables demographic segmentation analysis :contentReference[oaicite:8]{index=8}.
![age group dax](https://github.com/AbdurRoqeeb/Transforming-Raw-Hospital-Data-into-Actionable-Insights-with-Microsoft-Excel-Power-Query/blob/main/assets/age_group_dax.png?raw=true)
  

---

## Building the Fact Table

### Step 6: Create Fact Table  
- Use the main worksheet as the **Fact Table**.  
- Link to dimension entities using the assigned unique IDs.  
- Remove redundant columns already stored in dimension tables :contentReference[oaicite:9]{index=9}.
![fact table](https://github.com/AbdurRoqeeb/Transforming-Raw-Hospital-Data-into-Actionable-Insights-with-Microsoft-Excel-Power-Query/blob/main/assets/Screenshot%202025-08-20%20021417.png?raw=true)

### Step 7: Create Date Table  
- Generate a **Date Table** (not detailed in article but implied) to support temporal analytics.
![date table](https://github.com/AbdurRoqeeb/Transforming-Raw-Hospital-Data-into-Actionable-Insights-with-Microsoft-Excel-Power-Query/blob/main/assets/Screenshot%202025-08-20%20021355.png?raw=true)

---

## Data Modeling

### Step 8: Build the Data Model  
- Load all tables into Excel’s data model.  
- Define relationships:
  - Fact ↔ Patient Dimension  
  - Fact ↔ Doctor Dimension  
  - Fact ↔ Insurance Dimension  
  - Fact ↔ Date Table  
- Ensure referential integrity via unique IDs — forming a star schema :contentReference[oaicite:10]{index=10}.
![star schema](https://github.com/AbdurRoqeeb/Transforming-Raw-Hospital-Data-into-Actionable-Insights-with-Microsoft-Excel-Power-Query/blob/main/assets/Screenshot%202025-08-20%20020945.png?raw=true)

---

## Conclusion & Next Steps
This project showcases how a messy hospital dataset can be transformed into a clean, structured data model using Excel and Power Query :contentReference[oaicite:11]{index=11}. With the data organized into a star schema, it becomes far easier to analyze and visualize.

**Next steps could include:**
- Transitioning to **Power BI** for interactive dashboards and real-time updates  
- Automating data refreshes  
- Implementing more advanced metrics and KPIs  
- Sharing reports with stakeholders in accessible formats :contentReference[oaicite:12]{index=12}

---

## Technologies Used
- **Microsoft Excel**  
- **Power Query** for data transformation • ETL • star schema modeling :contentReference[oaicite:13]{index=13}
