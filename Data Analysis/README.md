# Analysis of Global Inflation Dynamics Post-COVID

## Project Overview

This project uses Python to analyse post-COVID inflation dynamics across nine major economies: USA, EU, China, India, Japan, UK, Brazil, Canada, and Vietnam. The analysis examines how inflation evolved from 2020 to 2024 and identifies the macroeconomic factors most strongly associated with inflation patterns, including interest rates, oil prices, food prices, money supply, and supply chain disruption.

## Analytical Problem

How did inflation evolve across major economies after COVID-19? Which macroeconomic factors have the strongest correlation with the inflation dynamics?

## Intended User

Economics students, policy researchers, and informed citizens.

## Dataset

- **File:** `global_inflation_post_covid.csv` (located at `../global_inflation_post_covid.csv` relative to this notebook)
- **Coverage:** 9 countries × monthly observations, 2020–2024
- **Assess date** 2026.4.18
- **Countries:** USA, EU, CHN, IND, JPN, GBR, BRA, CAN, VNM

| Column | Description |
|--------|-------------|
| `country` | Country / region code |
| `date` | Year-month (monthly frequency) |
| `inflation_rate` | Monthly CPI-based inflation rate (%) |
| `interest_rate` | Central bank policy interest rate (%) |
| `oil_price` | Crude oil price (USD/barrel) |
| `gdp_growth` | Monthly GDP growth rate (%) |
| `unemployment_rate` | Unemployment rate (%) |
| `money_supply_m2` | M2 money supply (billions, local currency) |
| `exchange_rate_usd` | Exchange rate vs USD |
| `food_price_index` | Food price index (base = 100) |
| `supply_chain_index` | Supply chain pressure index (higher = more disruption) |

## Project Files

- `inflation_analysis.ipynb` — main notebook with the full analytical workflow
- `reflection_report.md` — 500–800 word reflection report for submission
- `requirements.txt` — Python package requirements

## Methods

The notebook includes the following workflow:

1. Problem definition and user context
2. Data loading from local CSV (relative path)
3. Data cleaning and missing value handling
4. Summary statistics by country
5. Inflation trend line charts with COVID and surge period annotations
6. Country × year inflation heatmap
7. Interest rate vs inflation dual-axis charts (USA, EU, UK, China)
8. Oil price and food price index vs inflation (USA)
9. Supply chain pressure analysis and scatter plot
10. Pearson correlation heatmap across all macroeconomic variables
11. Peak inflation identification per country
12. M2 money supply normalisation and growth vs inflation scatter
13. Key findings and interpretation
14. Limitations and conclusion

## Key Findings

- All nine economies experienced relatively high inflation rate in 2021–2023, with the peak concentrated in 2022.
- Oil prices and food price indices show the strongest positive correlation with inflation across the dataset.
- Advanced economies (USA, UK, EU) significantly raised interest rates from 2022; China and Japan maintained accommodative policy.
- Supply chain pressure peaked in 2021–2022 and normalised in 2023, coinciding with the easing of inflation.
- Emerging markets (Brazil, India, Vietnam) showed higher average inflation and greater volatility.

## How to Run

1. Ensure `global_inflation_post_covid.csv` is located one directory above `ownwork/` (i.e., at `../global_inflation_post_covid.csv`).

2. Install the required packages:

pip install -r requirements.txt

3. Open the notebook:

jupyter notebook inflation_analysis.ipynb

4. Run all cells from top to bottom.

## Repository Structure

homework/
├── global_inflation_post_covid.csv
└── ownwork/
    ├── inflation_analysis.ipynb
    ├── README.md
    ├── reflection_report.md
    └── requirements.txt

## Product link
https://github.com/cathelleshen13-hp/ACC102-Mini-Assignment

## Limitations & next steps
- The dataset uses simulated/synthetic data for some variables, which may not fully accurately reflect the dynamic situations in the real world.
- Correlation does not imply causation. Multiple factors act simultaneously and interact with each other in complex ways.
- The M2 money supply data is presented in local currency units. Without standardization, it cannot be directly compared between different countries.
- The exchange rate variable represents different base currencies across countries, which limits direct horizontal comparisons between different countries.
- The analysis does not model lagged effects, which are important in monetary transmission.
- Country-level aggregation masks significant regional and sectoral variation within each economy.