# Movie-Data-Analysis
Netflix Analysis
# 🎬 Netflix Data Analysis Dashboard (SQL + Excel)

## 🔍 Project Overview

This project analyzes Netflix dataset to uncover insights about content distribution, trends, and audience preferences using SQL and Excel.

---

## 🛠️ Tools & Technologies

* SQL (MySQL / PostgreSQL)
* Microsoft Excel
* Pivot Tables & Charts

---

## 📁 Dataset

Dataset includes:

* Show ID
* Type (Movie/TV Show)
* Title
* Director
* Cast
* Country
* Date Added
* Release Year
* Rating
* Duration
* Genre

---

## 🎯 Objectives

* Analyze Movies vs TV Shows distribution
* Identify most popular genres
* Find top contributing countries
* Analyze yearly content trends
* Understand rating distribution

---

## 🧮 SQL Analysis

### 1️⃣ Count Movies vs TV Shows

```sql id="n1"
SELECT type, COUNT(*) AS total
FROM netflix
GROUP BY type;
```

### 2️⃣ Top 10 Countries

```sql id="n2"
SELECT country, COUNT(*) AS total
FROM netflix
GROUP BY country
ORDER BY total DESC
LIMIT 10;
```

### 3️⃣ Most Common Genres

```sql id="n3"
SELECT listed_in AS genre, COUNT(*) AS total
FROM netflix
GROUP BY listed_in
ORDER BY total DESC;
```

### 4️⃣ Content Added Per Year

```sql id="n4"
SELECT YEAR(date_added) AS year, COUNT(*) AS total
FROM netflix
GROUP BY year
ORDER BY year;
```

### 5️⃣ Most Frequent Ratings

```sql id="n5"
SELECT rating, COUNT(*) AS total
FROM netflix
GROUP BY rating
ORDER BY total DESC;
```

---

## 📈 Excel Dashboard

The dashboard includes:

* 🎬 Movies vs TV Shows (Pie Chart)
* 🌍 Country-wise Content (Bar Chart)
* 📊 Genre Distribution
* 📅 Yearly Trends Line Chart
* ⭐ Ratings Analysis
* 📌 KPI Cards (Total Titles, Top Genre, Top Country)

---

## 💡 Key Insights

* Movies dominate Netflix content
* Certain countries contribute significantly more content
* Drama & International content are most popular
* Rapid growth after 2015
* Majority content falls under TV-MA rating

---

## 📂 Project Structure

* `data/` → Netflix dataset
* `sql/` → SQL queries
* `excel/` → Dashboard file
* `README.md` → Documentation

---

## 🚀 How to Run

1. Import dataset into SQL database
2. Run queries
3. Export results
4. Build Excel dashboard

---

## 📌 Conclusion

This project highlights how SQL and Excel can be used to extract insights from large entertainment datasets.

---

⭐ Star this repo if you found it useful!
