# Netflix-powerBi-Dashboard
PowerBi project analyzing netflix movies and tv shows using DAX ,Power Query and interactive Dashboards
# 🎬 Netflix Movies & TV Shows Analysis (Power BI Dashboard)

Project Overview
This Power BI project provides a detailed analysis of the *Netflix Titles Dataset* — exploring trends, insights, and comparisons between *Movies* and *TV Shows* available on the platform.  

The goal of this project is to visualize content distribution, duration, release patterns, and other key metrics to understand how Netflix structures its global content library.

---

## 🧠 Objectives
•⁠  ⁠Analyze the distribution of Movies vs. TV Shows on Netflix  
•⁠  ⁠Understand which countries produce the most Netflix content  
•⁠  ⁠Evaluate release trends by year and genre  
•⁠  ⁠Compare average and median movie durations  
•⁠  ⁠Provide clean and interactive dashboards for data-driven insights  

---

## 🗂️ Dataset Information
•⁠  ⁠*Dataset:* Netflix Titles Dataset  
•⁠  ⁠*Source:* [Kaggle – Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)
•⁠  ⁠*Columns Used:*
  - Type (Movie/TV Show)
  - Title
  - Director, Cast
  - Country
  - Date Added, Release Year
  - Rating, Duration
  - Genre (Listed In)
  - Description

---

## ⚙️ Data Cleaning and Transformation
Performed in *Power BI Power Query Editor*:

- Removed null and duplicate records  
- Extracted numeric duration (e.g., “90 min” → `90`)  
- Split “Duration” column into numeric value and type (minutes/seasons)  
- Converted “Date Added” to proper date format  
- Added calculated columns like `DurationMinutes` for Movies  
- Used DAX measures for metrics like:

``DAX
Avg Movie Duration =
AVERAGEX(
    FILTER('NetflixTitles', 'NetflixTitles'[type] = "Movie" && NOT(ISBLANK('NetflixTitles'[DurationMinutes]))),
    'NetflixTitles'[DurationMinutes]
)

-Dashboards Overview
1. Overall Dashboard
Key KPIs and visuals:
Total Titles, Movies, TV Shows
Country-wise distribution
Content added per year trend
Top 10 genres and ratings

 2. Movies Dashboard
Focused on movie insights:
Average & median movie duration
Movies by country and release year
Top genres and directors

3. TV Shows Dashboard
Focused on TV show analytics:
Total shows and seasons
Country-wise show count
Trends by release year and rating

DAX Measures Used
Some important measures used in this report


Tools & Technologies
Power BI Desktop
Power Query
DAX (Data Analysis Expressions)
Microsoft Excel / CSV Data Source


How to Use
Download the Power BI file: Netflix_Dashboard.pbix
Open it in Power BI Desktop
Interact with the filters and slicers to explore data


Connect with me:
LinkedIn - https://www.linkedin.com/in/yaswanth-raj-dokku/







