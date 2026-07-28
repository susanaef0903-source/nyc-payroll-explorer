# NYC Payroll Explorer

**Live app:** https://sue-nyc-payroll.streamlit.app/

New York City publishes every city employee's payroll record as open data. I spent 20+ years running payroll, so I built the tool I would have wanted: an app that asks the questions a payroll professional actually asks.

The app queries the live [NYC Open Data Citywide Payroll dataset](https://data.cityofnewyork.us/City-Government/Citywide-Payroll-Data-Fiscal-Year-/k397-673e) and answers three questions for any fiscal year from 2020 to 2025:

1. **Where does overtime run hot?** Which agencies pay the most overtime, and what share of their payroll it represents.
2. **What do the biggest city jobs pay?** Pay for the city's largest job titles.
3. **Payroll footprint by borough.** Where the money lands geographically.

## How it works

Built with Python, pandas, and Streamlit. The data is not stored in this repo: the app sends live SoQL queries (Socrata's SQL dialect) to the NYC Open Data API, and caches results for an hour so the app stays fast.

## Run it locally

```
pip install -r requirements.txt
streamlit run app.py
```

## About

Part of my portfolio: [susanaef0903-source.github.io/personal-website](https://susanaef0903-source.github.io/personal-website/) . The deployed app currently builds from my personal-website repo; this repo is the project's standalone home.
