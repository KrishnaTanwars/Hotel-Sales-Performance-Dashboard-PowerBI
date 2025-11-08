# 🏨 Hotel Sales Performance Dashboard (Power BI)

An interactive Power BI project that analyzes **hotel sales performance** using 5 relational datasets.  
It tracks **bookings, revenue, occupancy rates, cancellations, and customer satisfaction**, helping hotel management make better business decisions through data visualization and insights.

---

## 📊 Project Overview

The **Hotel Sales Performance Dashboard** provides a centralized view of hotel operations across different cities and categories (Luxury & Business).  
It enables decision-makers to identify trends, optimize occupancy, and understand customer behavior using an easy-to-navigate Power BI dashboard.

---

## 🎯 Objectives

- Build a **data model** combining bookings, hotels, rooms, and dates  
- Track **key KPIs** such as occupancy rate, total revenue, and cancellation rate  
- Analyze **customer satisfaction** and booking patterns  
- Enable **dynamic filtering and drill-through** by city, category, and room type  

---

## 🧰 Tools & Techniques Used

- **Power BI**
- **Power Query**
- **DAX (Data Analysis Expressions)**
- **Data Modeling (Star Schema)**
- **Drill-through and Interactive Visuals**

---

## 🧩 Data Sources

The project uses **five interlinked CSV files** forming a star schema model:

1. **dim_date** – calendar details (date, week no, day type)
2. **dim_hotels** – hotel information (name, city, category)
3. **dim_rooms** – room details (type, class)
4. **fact_bookings** – detailed booking transactions
5. **fact_aggregated_bookings** – aggregated booking and capacity data

---

## 📈 Key Insights & KPIs

- **Total Revenue** and **Revenue Realized**
- **Occupancy Rate (%)**
- **Successful Bookings vs Capacity**
- **Cancellation and No-show Trends**
- **Average Customer Ratings**
- **City-wise and Category-wise Revenue Performance**

---

## 🧮 DAX Measures Used

```DAX
Occupancy % = DIVIDE(SUM(fact_aggregated_bookings[successful_bookings]), SUM(fact_aggregated_bookings[capacity]))
Revenue Realized = SUM(fact_bookings[revenue_realized])
Cancellation Rate = 
    DIVIDE(
        CALCULATE(COUNTROWS(fact_bookings), fact_bookings[booking_status] = "Cancelled"),
        COUNTROWS(fact_bookings)
    )
Average Rating = AVERAGE(fact_bookings[ratings_given])
```
---

# 💡 Dashboard Features

- Dynamic filters for **City**, **Category**, and **Room Type**  
- **KPIs cards** with conditional formatting  
- **Trend lines** and comparison visuals  
- **Drill-down** by city or week  
- **Intuitive layout** with clear visual storytelling  

---

## 🖼️ Project Screenshots

| **Dashboard Page**     | **Description** |
|-------------------------|-----------------|
| **Main Page**           | Overview of all KPIs and performance metrics |
| **Bookings Analysis**   | Trends in successful, cancelled, and no-show bookings |
| **Revenue Breakdown**   | Total and realized revenue by city and category |
| **Customer Insights**   | Ratings and satisfaction metrics |

---

## 🔗 Project Links

- 🎥 **Demo Video:** [YouTube Presentation](https://youtu.be/5j9hTuH9cYI)   
- 💻 **Live Power BI Dashboard:** [View Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMjJlMTZhNzktYjVlZC00OGM4LTg3NDEtMWQyNTU5ZjE0N2EzIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)  
- 💼 **LinkedIn Post:** [LinkedIn Project Post](https://www.linkedin.com/posts/krishnatanwars_hotel-sales-dashboard-in-power-bi-bi-project-activity-7392901726531510272-Ebj5?utm_source=share&utm_medium=member_desktop&rcm=ACoAADYd6qIB8ad7Dw_i1eRhB3iXtglA1SKFQX0)  

---

## 🌱 Learning Outcomes

Through this project, I learned:

- Building **data models** with multiple relationships  
- Writing **DAX measures** for complex KPIs  
- Applying **data cleaning and transformation** in Power Query  
- Designing **professional and user-friendly dashboards**

---
