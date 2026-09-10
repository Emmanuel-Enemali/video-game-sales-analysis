# Video Game Sales Analysis 🎮

An exploratory data analysis project examining video game sales across the United States and Australia between 2010 and 2017 — covering data cleaning, regional sales distribution, and publisher and platform insights.

---

## 📌 Project Overview

This project analyzes a dataset of **5,893 video game releases** across **15 columns**, exploring national and global sales figures, regional breakdowns, genre distribution, and publisher performance. The analysis was carried out entirely in Python using Jupyter Notebook.

| Records | Columns | Years Covered |
|---|---|---|
| 5,893 | 15 | 2010 – 2017 |

---

## ❓ Key Questions Explored

- How are national sales distributed across regions and countries?
- What proportion of total sales (national and global) comes from each country?
- What data quality issues are present and what steps are required to prepare the data for analysis?

---

## 🧹 Data Cleaning

The following actions were taken to clean the dataset:

- **Duplicates** — 16 duplicate rows identified and removed, reducing records from 5,909 to 5,893
- **Missing Values** — 27 missing Region entries filled with "North"; 12 missing Publisher entries filled with "Unknown"
- **Currency Formatting** — National Sales column stored as text with a "$" prefix; symbol stripped using regex-based `.replace()`
- **Data Type Correction** — National Sales converted from string to float64 using `pd.to_numeric()`
- **Text Standardization** — Inconsistent country labels (e.g., "USA") standardized to "United States"
- **Column Renaming** — Columns renamed for clarity: `NA_Sales` → National Sales, `Global_Sales` → Global Sales, etc.

---

## 📊 Key Findings

- **The United States dominates** — accounting for **80.6%** of national sales and **81.1%** of global sales
- **Australia** contributed the remaining **19.4%** of national and **18.9%** of global sales
- **The West region** generated the highest national sales overall and was the only region with substantial Australian contribution
- **East and Central regions** were driven almost entirely by United States sales

---

## ⚠️ Limitations

- Dataset covers only two countries (United States and Australia) — conclusions cannot be extended to global markets
- 27 missing Region values defaulted to "North" — may introduce bias in regional comparisons
- 12 missing Publisher values filled with "Unknown" — limits publisher-level analysis accuracy
- Wii Sports retained as a legitimate outlier — median-based statistics recommended over means for this dataset

---

## 💡 Recommendations

1. Prioritize the **United States market**, particularly the **West region**, in future marketing and inventory planning
2. Investigate the true regional distribution of the 27 records defaulted to "North"
3. Research and correct the 12 "Unknown" publisher records where possible
4. Expand the dataset to include additional countries for broader global insights
5. Use **median-based statistics** alongside means given the presence of high-value outliers like Wii Sports

---

## 🗂️ Dataset Overview

| Attribute | Detail |
|---|---|
| Original Row Count | 5,909 |
| Final Row Count | 5,893 |
| Columns | 15 |
| Countries Covered | United States, Australia |
| Years Covered | 2010 – 2017 |
| Missing Values (Publisher) | 12 (filled with "Unknown") |
| Missing Values (Region) | 27 (filled with "North") |

---

## 🛠️ Tools Used

- **Python 3.13** — Core programming language
- **Pandas** — Data cleaning and manipulation
- **NumPy** — Numeric operations
- **Matplotlib & Seaborn** — Data visualization
- **Jupyter Notebook (VS Code)** — Development environment

---

## 📁 Repository Structure

```plaintext
video-game-sales-analysis/
├── data/
│   └── video_games_dataset.csv
├── report/
│   └── video_games_report.pdf
├── visualizations/
│   ├── sales_chart1.png
│   └── sales_chart2.png
└── README.md
```

---

*Built as part of my data analytics portfolio — dive in, fork it, or connect if you'd like to collaborate.*
