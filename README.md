# 🦠 COVID-19 Data Analysis & Visualization — India
An end-to-end data analysis project that processes nested JSON and CSV COVID-19 datasets using Pandas and json.load(). Includes time-series visualizations, multi-state comparisons, annotated event-marked charts, and Pandas Styler heatmaps for southern Indian states.

A Python-based data analysis project that explores India's state-wise COVID-19 trends using real government-released datasets. The project covers end-to-end data wrangling, filtering, and visualization of Confirmed, Recovered, and Deceased case data across Indian states.

---

## 📌 Project Highlights

- Parsed and flattened nested JSON datasets using `json.load()` and `pd.json_normalize()`
- Filtered and analyzed state-wise data — with a focused deep-dive on **Karnataka**
- Plotted time-series line graphs comparing **Confirmed vs Recovered** cases
- Built styled, annotated charts with custom colors, axis labels, and event markers (e.g., Second Lockdown)
- Applied **Pandas Styler** techniques — heatmaps, color gradients, and bar charts — for tabular insights across southern states (AP, KA, KL, TN)

---

## 📁 Project Structure

```
covid19-analysis/
│
├── data/
│   ├── covid_states_daily.json       # State-wise daily case data (JSON)
│   └── case_time_series.csv          # National daily case time series (CSV)
│
├── analysis/
│   ├── state_analysis.py             # State-wise filtering, cleaning & visualization
│   ├── national_trends.py            # National confirmed/recovered/deceased trends
│   └── styled_charts.py             # Annotated & styled matplotlib charts
│
├── README.md
└── requirements.txt
```

> 💡 **Note:** See the [File Structure Suggestion](#-suggestion-how-to-organize-your-files) section below for why the code is split this way.

---

## 📊 Datasets Used

| File | Description |
|------|-------------|
| `covid_states_daily.json` | State-wise daily Confirmed, Recovered, and Deceased counts across all Indian states |
| `case_time_series.csv` | National-level daily time series with cumulative and daily case counts |

> Data sourced from India's official COVID-19 API (covid19india.org).

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Core programming language |
| Pandas | Data loading, cleaning, filtering, and styling |
| NumPy | Numerical operations |
| Matplotlib | Line charts and annotated visualizations |
| Seaborn | Statistical plot styling |
| JSON (stdlib) | Parsing nested JSON datasets |

---

## 📈 Sample Visualizations

### Karnataka — Confirmed vs Recovered Cases
- Line graph comparing daily confirmed and recovered cases over time
- Vertical date labels on X-axis for readability

### National Daily Confirmed Cases (Styled)
- Dark-themed chart with annotated data points
- Event marker: *"Second Lockdown — 15th April"*
- Custom colors, marker styles, and axis formatting

### Pandas Styler — Southern States Comparison
- Heatmap using `background_gradient(cmap='Reds')`
- Highlighted max (red) and min (green) values
- Bar chart visualization within the DataFrame table

---

## 🔍 Key Challenges & How I Solved Them

| Challenge | Solution |
|-----------|----------|
| `pd.read_json()` produced inconsistent results on nested JSON | Switched to `json.load()` + `pd.json_normalize()` for reliable flattening |
| Mixed data types preventing numeric operations | Used `apply(pd.to_numeric)` after dropping non-numeric columns |
| Cluttered X-axis dates | Applied `plt.xticks(rotation='vertical')` for clean date display |
| Raw data had no clear date index | Set `dateymd` as the DataFrame index for time-series alignment |


## 📄 License

This project is open source and available under the [MIT License](LICENSE).
