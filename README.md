# zomato-restaurant-insights-eda
# 🍽️ Zomato Restaurant Insights: A Global Dining EDA

> Exploratory data analysis of **9,500+ restaurants across the world** from Zomato: ratings, cuisines, pricing, online delivery and the busiest dining neighbourhoods of Delhi.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-Interactive%20Charts-3F4F75?logo=plotly&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-4c72b0)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## 📌 Project Overview

Food discovery platforms generate a huge amount of data about what people eat, where they eat and how much they are willing to pay. This project digs into the Zomato dataset to answer practical, business-style questions:

- Which countries have the largest restaurant presence on the platform?
- How are restaurants rated, and how many have no rating at all?
- Which cuisines consistently earn **Excellent** ratings?
- Where are the most expensive restaurants in the world?
- Which Delhi localities are the busiest, and do they offer online delivery?
- Does a higher price actually mean a higher rating?

## 🗂️ Dataset

| Item | Details |
|---|---|
| Main file | `zomato.csv` (9,551 rows × 21 columns) |
| Lookup file | `Country_Code.xlsx` (maps country codes to country names) |
| After cleaning and merging | 9,542 rows × 22 columns, with no missing values |

**Key columns:** Restaurant Name, City, Locality, Cuisines, Average Cost for two, Has Table booking, Has Online delivery, Price range, Aggregate rating, Rating text, Votes.

## 🧹 Data Preparation

1. Loaded the CSV with `latin-1` encoding to handle special characters in restaurant names.
2. Checked for missing values and dropped the rows with a missing `Cuisines` value (9 rows).
3. Merged the dataset with the country-code lookup table to add a readable `Country` column.
4. Confirmed the final dataset is clean (zero nulls) before analysis.

## 🔍 Analysis & Visualisations

| Theme | What was explored | Charts |
|---|---|---|
| 🌍 **Geography** | Restaurant count by country | Count plot, interactive bar |
| ⭐ **Ratings** | Rating distribution, rating colours and text, unrated restaurants per country | Pie, stacked bar, bar |
| 🚚 **Online delivery** | Share of restaurants offering delivery, and delivery by country | Pie, grouped counts |
| 🍜 **Cuisines** | Top cuisines among *Excellent*-rated restaurants, and top 10 cuisines overall | Horizontal bar, pie |
| 💸 **Pricing** | The 25 costliest restaurants for two people worldwide | Interactive bar by city |
| 📍 **Delhi deep-dive** | Localities with the most restaurants, delivery availability, and price vs rating | Bar, count plot, scatter |

### 💡 Highlight
**Connaught Place** is Delhi's busiest dining locality with roughly **122 listed restaurants**, though other localities are not far behind.

## 🛠️ Tech Stack

- **Python**: core language
- **Pandas & NumPy**: data cleaning, merging and aggregation
- **Matplotlib & Seaborn**: static statistical plots
- **Plotly Express**: interactive charts
- **Jupyter Notebook**: analysis environment

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/<aryank2074-ai>/zomato-restaurant-insights-eda.git
cd zomato-restaurant-insights-eda

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn plotly openpyxl jupyter

# 3. Launch the notebook
jupyter notebook zomato_project.ipynb
```

> 📁 Make sure `zomato.csv` and `Country_Code.xlsx` sit in the same folder as the notebook.

## 📁 Repository Structure

```
zomato-restaurant-insights-eda/
├── zomato_project.ipynb   # Full analysis notebook
├── zomato.csv             # Restaurant dataset
├── Country_Code.xlsx      # Country code lookup
└── README.md
```

## 🔮 Future Improvements

- Add a map view of restaurants using latitude and longitude
- Compare ratings and pricing across more cities, not just Delhi
- Build a simple predictive model for restaurant ratings
- Turn the findings into an interactive dashboard (Streamlit or Power BI)

## 🙌 Acknowledgements

Dataset sourced from Zomato's publicly available restaurant data.

---

⭐ If you found this project useful, consider giving it a star!
