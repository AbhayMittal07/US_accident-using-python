# 📊 US Traffic Accidents Data Analysis (2016–2019)

This project analyzes a large-scale dataset of traffic accidents in the United States from 2016 to 2019. It explores patterns in accidents over time, geography, and weather conditions using powerful data visualization and analysis libraries like **Pandas**, **Seaborn**, and **Folium**.

---

## 📁 Dataset Overview

- **Total records:** 7,728,394  
- **Total columns:** 46  
- **Source:** US accidents dataset (real-world transportation data)  
- **Key fields include:**
  - `Severity`, `Start_Time`, `End_Time`
  - `Start_Lat`, `Start_Lng`, `End_Lat`, `End_Lng`
  - `City`, `State`, `Weather_Condition`, `Temperature(F)`
  - Boolean flags like `Junction`, `Traffic_Signal`, `Amenity`

---

## 📌 Key Steps & Insights

### 🧼 Data Cleaning

- Converted `Start_Time` to datetime.
- Calculated missing values:
  - Highest missing: `End_Lat`, `End_Lng` (~44%)
  - Weather-related fields like `Precipitation(in)` and `Wind_Chill(F)` also had significant missingness.
- Total unique accident cases (`ID`): 7,728,394

### 🌆 City-Level Accident Analysis

- Total unique cities: 13,679
- **Top 5 cities by number of accidents:**
  1. Miami – 186,917
  2. Houston – 169,609
  3. Los Angeles – 156,491
  4. Charlotte – 138,652
  5. Dallas – 130,939
- About **8.9% of cities** account for **1,000+ accidents**
- Over **1,000 cities** reported only **1 accident**

### ⏰ Time-Based Analysis

- Accidents peak during **7–9 AM** and **4–6 PM** (commute hours)
- Sunday vs Tuesday hourly comparisons showed varied trends
- Accident frequency by **month** shows higher density in winter
- Year-wise filtering (e.g., 2019) helps isolate seasonal trends

### 🗺️ Geo-Spatial Visualizations

- Used `Start_Lat` and `Start_Lng` for plotting locations
- Scatter plots show accident clusters
- Created a **heatmap** using `folium` on a 1% sample

---

## 📉 Visualizations & Tools Used

- `pandas`, `matplotlib`, `seaborn` for EDA
- `folium` for interactive map-based heatmaps
- Visualizations include:
  - Histograms (hour, day of week, month)
  - Pie chart (source distribution)
  - Bar plots (top cities by accident count)
  - Heatmap (accident location density)

---

## 💡 Notable Observations

- Significant **missing values** in location and weather fields
- **Miami** had the highest accident count
- **Rush hours** are most accident-prone
- **Winter months** see slightly more accidents

---

## 🛠️ Future Work

- Analyze impact of **weather conditions** on accident severity
- Apply **clustering/ML models** for predicting severity or accident likelihood
- Create interactive dashboards using **Plotly Dash** or **Streamlit**

---

## 📍 Sample Heatmap

> Folium's `HeatMap` plugin was used to create a geo-heatmap using a 1% random sample from the dataset.

