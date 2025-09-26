# Data--analysis-dashboard
# 🏏 Virat Kohli Career Statistics Analysis Dashboard

This interactive dashboard provides a comprehensive analysis of **Virat Kohli’s cricket career** from **2008 to 2025**, across all formats — **ODI**, **Test**, and **T20I**. Built using **Power BI**, it offers deep visual insights into his run trends, centuries, boundaries, and more.

---

## 📊 Key Features

### ✅ Top KPIs:
- **Innings Played:** 616
- **Total Runs:** 27,580
- **Strike Rate:** 91
- **Batting Average:** 50

### 🎯 Filters:
- **Year Range Slider** (2008–2025)
- **Format Selector** (ODI, Test, T20I)

### 📈 Visualizations:
- **Runs by Year (Bar Chart)**  
- **Boundaries (Donut Chart)** — 4s and 6s with percentage split  
- **Centuries and Half-Centuries (Area Chart)** — 50s and 100s trend  
- **KPI Tiles** — with clear numbers and responsive layout  

---

## 🗃️ Data Structure

The dataset used consists of match-level and player-level information. Example schema below:

### Sample Data Fields (CSV or Hive Table):

| Column Name     | Description                        |
|-----------------|------------------------------------|
| `Year`          | Match year                         |
| `Match_Type`    | ODI / Test / T20I                  |
| `Runs_Scored`   | Runs scored in the match           |
| `Balls_Faced`   | Balls faced by player              |
| `Fours`         | Number of boundaries (4s)          |
| `Sixes`         | Number of sixes (6s)               |
| `Fifties`       | Number of 50s in a year            |
| `Hundreds`      | Number of 100s in a year           |
| `Strike_Rate`   | Strike rate for the year/format    |
| `Average`       | Batting average                    |
| `Innings`       | Number of innings played           |

---


---

## 🛠️ Tools & Technologies Used

- **Power BI** for dashboard and data modeling  
- **DAX** for calculated metrics (e.g., strike rate, aggregates)  
- **Excel / CSV** as data source  
- *(Optional)* **Apache Hive + HDFS** for large-scale cricket data analysis  

If Hive is used:
- Query historical player data using **HiveQL**
- Export result as CSV or use Power BI Hive connector

---

## 🚀 How to Use the Dashboard

1. Open the `.pbix` file in Power BI Desktop
2. Use the **Year slider** to explore specific time periods
3. Select **format tiles (ODI, Test, T20I)** to filter visuals
4. Hover over charts to see detailed tooltips

---

## 📌 Insights You Can Extract

- Performance peaks and dips across years
- Career strike rate and average evolution
- Format-wise consistency
- Boundary hitting frequency
- Ton progression over time

---

## 📈 Sample DAX Measures

```DAX
Total Runs = SUM('Stats'[Runs_Scored])

Strike Rate = 
DIVIDE(
    SUM('Stats'[Runs_Scored]) * 100,
    SUM('Stats'[Balls_Faced])
)

Batting Average = 
DIVIDE(
    SUM('Stats'[Runs_Scored]),
    COUNT('Stats'[Innings])
)


---




