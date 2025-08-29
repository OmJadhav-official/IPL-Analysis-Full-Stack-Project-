# 🏏 IPL Analysis & Dashboard  
**Author**: Om Jadhav  
**Tools**: Power BI, Excel, DAX

---

## 📌 Overview  
This project presents a full-stack data analysis of the Indian Premier League (IPL). It includes data cleaning, relationship modeling, custom DAX measures, and an interactive dashboard built in Power BI. The goal is to transform raw ball-by-ball and match-level data into actionable insights for fans, analysts, and decision-makers.

---

## 🔍 Problem Statement  
The IPL dataset was fragmented across multiple granular tables and lacked pre-calculated performance metrics. Key indicators like strike rate, economy rate, and cap-holder stats were missing, making it difficult to derive insights or build visualizations directly.

---

## 🛠️ Solution  
- Cleaned and standardized raw data using Excel 
- Modeled one-to-many relationships between match and delivery datasets  
- Engineered custom DAX measures for batsman strike rate, bowler economy, bowler strike rate, and dynamic cap-holder KPIs  
- Designed an interactive Power BI dashboard with slicers, KPI cards, and performance charts

---

## ✅ Outcome  
The final dashboard delivers a comprehensive analytical view of IPL 2023, highlighting top performers, match outcomes, and strategic decisions. It showcases technical depth in DAX, relationship modeling, and visual storytelling—making it a recruiter-ready portfolio piece.

---

## 📊 Dashboard Preview  
![IPL 2023 Dashboard Preview](dashboard_image.png)  
*Interactive Power BI dashboard showcasing key metrics, top players, and team performance.*

---

## 🧠 Key DAX Measures
```DAX
Batsman Strike Rate = 
(SUM(deliveries[batsman_runs]) / COUNT(deliveries[ball])) * 100

Bowler Economy = 
VAR over_ = COUNT(deliveries[ball]) / 6
RETURN SUM(deliveries[total_runs]) / over_

Bowler Strike Rate = 
COUNT(deliveries[ball]) / SUM(deliveries[is_wicket])

Orange Cap Holder Runs = 
CALCULATE(SUM(deliveries[batsman_runs])) & " Runs"

Purple Cap Holder Wickets = 
CALCULATE(SUM(deliveries[is_wicket])) & " Wickets"
```
---

## 🏆 Achievements

### 🔍 Problem  
The IPL 2023 dataset posed several analytical challenges typical of large-scale sports data: fragmented ball-by-ball and match-level tables, lack of pre-calculated performance metrics, and the need for dynamic, role-specific insights across players and teams. The raw data also lacked clarity in strike rates, economy rates, and cap-holder identification, making it unsuitable for direct visualization or decision-making.

### 🛠️ Solution  
A robust Power BI data model established one-to-many relationships between match and delivery datasets. Custom DAX measures calculated advanced KPIs including batsman strike rate, bowler economy, bowler strike rate, and dynamic cap-holder stats. Modular visuals—KPI cards, leaderboards, pie charts, and filters—enabled real-time performance tracking and comparative analysis.

### ✅ Result  
The final dashboard delivers a comprehensive analytical view of IPL 2023, transforming raw data into actionable insights for fans, analysts, and decision-makers. It highlights top performers, strategic toss decisions, and match outcomes with precision, while showcasing technical depth in data modeling, DAX logic, and visual storytelling. The project demonstrates a scalable, recruiter-ready analytics solution with real-world impact.
