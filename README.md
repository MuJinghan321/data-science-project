# Automobile Sales During Recessions — A Data Visualization Analysis

## Research Question

**How do economic recessions impact automobile sales, and which vehicle categories and economic factors are most affected?**

This project analyzes historical automobile sales data spanning 1980–2020, covering six major recession periods (1980, 1981–82, 1991, 2000–01, 2007–09, and 2020 COVID-19) to understand how economic downturns shape consumer behavior and automotive market dynamics.

---

## Dataset

**Source:** The dataset is a curated automotive sales dataset used in data visualization coursework (originally from IBM Skills Network).

**Contents:** Monthly sales data from 1980 to 2020, with 13 variables:

| Variable | Description |
|---|---|
| Date | Month-end date of sales observation |
| Recession | Binary indicator: 1 = recession period, 0 = normal period |
| Automobile_Sales | Number of vehicles sold in the period |
| GDP | Per capita GDP (USD) |
| Unemployment_Rate | Monthly unemployment rate (%) |
| Consumer_Confidence | Consumer confidence index (synthetic) |
| Seasonality_Weight | Seasonal effect weight on sales |
| Price | Average vehicle price |
| Advertising_Expenditure | Company advertising spend |
| Vehicle_Type | Vehicle category (SuperMini, Small Family, Medium Family, Executive, Sports) |
| Competition | Market competition index |
| Month / Year | Extracted time components |

**Usage rights:** The dataset is used for educational and portfolio demonstration purposes.

---

## Methods & Tools

- **Data manipulation:** Pandas, NumPy
- **Static visualizations:** Matplotlib, Seaborn
  - Line charts (time-series trends)
  - Bar charts (grouped comparisons)
  - Subplots (side-by-side analysis)
  - Bubble plots (multi-variable encoding)
  - Scatter plots (correlation analysis)
  - Pie charts (proportion breakdown)
- **Geographic visualization:** Folium (choropleth map)
- **Analysis approach:** Descriptive data visualization — comparing recession vs. non-recession periods across multiple dimensions (vehicle type, GDP, unemployment, advertising spend, consumer confidence).

---

## Key Findings

1. **Overall sales drop sharply during recessions.** Average automobile sales decline significantly in recession years, with the 2008 financial crisis and 2020 COVID-19 showing the deepest dips.

2. **Luxury and sports vehicles are most vulnerable.** Executive cars and sports cars experience the steepest sales declines during recessions, while smaller family cars and superminis show relative resilience — consumers shift toward practical, affordable vehicles in downturns.

3. **Unemployment rate is a strong negative driver.** As unemployment rises above ~3%, automobile sales fall sharply across all vehicle categories, with entry-level segments showing the highest volatility.

4. **Consumer confidence correlates positively with sales.** During recessions, higher consumer confidence is associated with stronger sales, confirming that sentiment is a key factor in big-ticket purchases.

5. **Advertising budgets are cut during recessions.** The company spends substantially more on advertising in non-recession periods, and ad spend is disproportionately allocated toward lower-priced vehicles during downturns.

### Limitation

A key limitation is that the dataset is **synthetic/simulated** rather than real company data. The Consumer_Confidence index is explicitly noted as synthetic, and the dataset does not represent any specific real-world automaker. This means the patterns observed are illustrative rather than empirically validated against actual business outcomes.

---

## How to Run the Analysis

### Prerequisites

- Python 3.9 or higher
- Jupyter Notebook / Jupyter Lab

### Installation

```bash
# Clone the repository
git clone https://github.com/MuJinghan321/data-science-project.git
cd data-science-project

# Install dependencies
pip install -r requirements.txt
```

### Run the notebook

```bash
jupyter notebook automobile_sales_recession_analysis.ipynb
```

Make sure the `data/` folder is in the same directory as the notebook, as it loads `automobile_sales.csv` and `us-states.json` from there.

---

## Project Structure

```
data-science-project/
├── data/
│   ├── automobile_sales.csv      # Main dataset
│   └── us-states.json            # GeoJSON for Folium map
├── images/                       # Exported visualization charts
├── automobile_sales_recession_analysis.ipynb   # Main analysis notebook
├── requirements.txt              # Python dependencies
└── README.md                     # This file
```
