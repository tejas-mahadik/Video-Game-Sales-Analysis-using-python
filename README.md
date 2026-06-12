# 🎮 Video Game Sales Analysis

A **Python-based data analysis project** built using Pandas, NumPy, Matplotlib, and Seaborn. This notebook performs an end-to-end exploratory analysis of video game sales data — covering data cleaning, feature engineering, statistical operations, groupby aggregations, and rich visualizations.

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `Video_Game_Sales_Analysis.ipynb` | Jupyter Notebook with full analysis and visualizations |
| `vgsales.csv` | Raw dataset containing 108 video game sales records |

---

## 📊 Dataset Details

**Source:** `vgsales.csv` — Video Game Sales Dataset

| Column | Type | Description |
|--------|------|-------------|
| `Rank` | Integer | Sales rank |
| `Name` | String | Game title |
| `Platform` | String | Gaming platform (DS, PS3, Switch, etc.) |
| `Year` | Float | Release year |
| `Genre` | String | Game genre (Action, Shooter, RPG, etc.) |
| `Publisher` | String | Game publisher |
| `NA_Sales` | Float | North America sales (millions) |
| `EU_Sales` | Float | Europe sales (millions) |
| `JP_Sales` | Float | Japan sales (millions) |
| `Other_Sales` | Float | Rest of world sales (millions) |
| `Rating` | String | ESRB rating (E, T, M, AO, etc.) |
| `Global_Sales` | Float | Total worldwide sales (millions) |

**Dataset Shape:** 108 rows × 12 columns

**Missing Values (before cleaning):**
- `Year` — 10 missing
- `Publisher` — 6 missing
- `Rating` — 22 missing

---

## 🔢 Analysis Summary

| Metric | Value |
|--------|-------|
| Total Games Analyzed | 108 |
| Total Global Sales | 413.05 Million |
| Best Selling Game | Mario Kart 8 Deluxe |
| Most Popular Genre | Shooter |
| Top Platform | DS |
| Top Publisher | Bandai Namco |
| Year with Most Releases | 2017 |
| Average Global Sales | 3.82 Million |
| Blockbuster Games (≥5M) | 29 |

---

## 📒 Notebook Structure

| Section | Description |
|---------|-------------|
| **1. Load Dataset** | Read CSV, display first 5 rows |
| **2. Dataset Overview** | Shape, dtypes, missing value counts |
| **3. Data Cleaning** | Fill nulls — median for Year, 'Unknown' for Publisher/Rating |
| **4. NumPy Operations** | Statistical analysis — mean, median, std, percentiles, log transform |
| **5. Feature Engineering** | Create 6 new derived columns |
| **6. Filtering Operations** | Conditional filters — blockbusters, recent games, region dominance |
| **7. GroupBy Operations** | Aggregations by Genre, Platform, Publisher |
| **8. Visualizations** | 6+ charts using Matplotlib and Seaborn |
| **9. Publisher Analysis** | Stacked bar chart — regional sales by top 8 publishers |
| **10. Final Summary** | Printed summary of all key findings |

---

## 🛠️ Feature Engineering

6 new columns created from raw data:

| Feature | Description |
|---------|-------------|
| `Sales_Category` | Blockbuster (≥5M) / Hit (≥2M) / Moderate (≥1M) / Low |
| `Era` | Console generation — 6th / 7th / 8th / 9th Gen |
| `NA_Dominant` | Boolean — True if NA Sales > 50% of Global Sales |
| `NA_Ratio` | North America sales as % of global |
| `EU_Ratio` | Europe sales as % of global |
| `Popularity_Score` | Normalized score out of 10 based on Global Sales |

---

## 🔍 Key Insights

1. **Shooter and Action** genres lead with 64.72M and 64.01M in total global sales respectively.
2. **DS platform** dominates with 66.85M total sales across 17 games.
3. **Bandai Namco** is the top publisher with 18 games and $67.01M in total sales.
4. **2017** had the highest number of game releases in the dataset.
5. **29 blockbuster games** crossed 5 million in global sales.
6. **20 games** had higher Japan sales than North America sales — indicating strong JP-market titles.
7. **Nintendo** has the highest average sales per game (4.43M) among top publishers.

---

## 📦 Requirements

```
Python 3.x
pandas
numpy
matplotlib
seaborn
```

Install dependencies with:

```bash
pip install pandas numpy matplotlib seaborn
```

---

## 🚀 How to Run

1. Clone or download this repository.
2. Place `vgsales.csv` in the same folder as the notebook, or update the file path:
   ```python
   df = pd.read_csv('vgsales.csv')
   ```
3. Open `Video_Game_Sales_Analysis.ipynb` in **Jupyter Notebook** or **VS Code**.
4. Run all cells from top to bottom.

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| Python 3.13 | Core programming language |
| Pandas | Data loading, cleaning, groupby, filtering |
| NumPy | Statistical operations, array math, log transform |
| Matplotlib | Bar charts, line charts, area charts |
| Seaborn | Heatmaps, distribution plots |
| Jupyter Notebook | Interactive development environment |

---

## 👤 Author

**Tejas**
Data Analysis Project — Video Game Sales Analysis using Python
