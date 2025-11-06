# Bangalore-Restaurant-Dashboard
Interactive Power BI dashboard analyzing Zomato Bangalore restaurant data — includes insights on cuisines, ratings, cost, and delivery trends.


# 📊 Bangalore Restaurant Data Analysis Dashboard (Zomato Dataset)

This project presents an interactive **Power BI dashboard** built using the **Zomato Bangalore Restaurants Dataset** from Kaggle.  
It provides insights into restaurant distribution, cuisines, cost trends, ratings, and delivery availability across Bangalore.

---

## 🧠 Project Overview

The primary goal of this project is to analyze restaurant data and extract actionable insights, such as:
- Which areas in Bangalore have the highest restaurant density?
- What cuisines are most common?
- How do **average costs** correlate with **ratings**?
- What percentage of restaurants offer **home delivery**, **takeaway**, or **veg-only** options?

---

## 🧰 Tools and Technologies Used

| Tool / Language | Purpose |
|-----------------|----------|
| **Power BI** | Data visualization, dashboard creation, and DAX measures |
| **Python (Pandas)** | Data cleaning and preprocessing (optional) |
| **Excel/CSV** | Raw data format |
| **GitHub** | Version control and portfolio hosting |

---

## 🧮 Key DAX Measures

These measures were used to calculate insights within Power BI:

```DAX
Total Restaurants = COUNT(BangaloreZomatoData_Cleaned[Name])

Total Areas = DISTINCTCOUNT(BangaloreZomatoData_Cleaned[Area])

Average Cost = AVERAGE(BangaloreZomatoData_Cleaned[AverageCost])

Average Delivery Rating = AVERAGE(BangaloreZomatoData_Cleaned[Delivery Ratings])

Top Rated Restaurants =
    CALCULATE(
        [Total Restaurants],
        BangaloreZomatoData_Cleaned[Delivery Ratings] > 4.2
    )
