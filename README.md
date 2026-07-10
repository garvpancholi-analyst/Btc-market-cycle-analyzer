# Bitcoin Market Cycle Analyzer

- Identifying Bull and Bear market phases in Bitcoin's 5-year price 
- history using Python, pandas, and the 200-Day Moving Average.

---

## Overview

Most crypto investors make decisions based on gut feeling.
This project takes a data-driven approach — using 5 years of 
historical BTC price data (2019–2023) to objectively classify 
every single day as either a Bull or Bear market phase, and 
analyse how price behaviour differs between the two.



## Tools & Libraries

-------------------------------------------------------------
| Tool                | Purpose                              |
|---------------------|--------------------------------------|
| Python              | Core programming language            |
| pandas              | Data loading, cleaning, and analysis |
| matplotlib          | Data visualization                   |
| Jupyter Notebook    | Development environment              |
--------------------------------------------------------------

## 📂 Project Structure

###  How It Works — 5 Stage Pipeline

### Stage 1 — Load & Inspect
- Loaded raw BTC daily closing price data (2019–2023)
- Used `head()`, `info()`, and `describe()` to understand
  structure, data types, and missing values before processing

### Stage 2 — Clean
- Converted `Date` column from plain text to `datetime64` format
- Removed missing values using `dropna()`
- Removed duplicate rows using `drop_duplicates()`
- Sorted data chronologically (oldest → newest)

### Stage 3 — Feature Engineering
- Calculated **200-Day Moving Average** using `rolling(window=200).mean()`
  — for each day, this is the average closing price of the past 200 days
- Tagged every day as **Bull** or **Bear**:
  - 🟢 Bull → price is above the 200-Day MA (market trending up)
  - 🔴 Bear → price is below the 200-Day MA (market trending down)

### Stage 4 — Analysis
- **Finding 1** → Compared avg, max price and total days in Bull vs Bear phases
- **Finding 2** → Calculated yearly average price trend (2019 → 2023)
- **Finding 3** → Counted total Bull vs Bear days and converted to percentage

### Stage 5 — Visualization
Built a single comprehensive chart with 4 layers:
- Black line → actual BTC price history
- Orange dashed line → 200-Day Moving Average
- Green shading → Bull phase periods
- Red shading → Bear phase periods



## 📊 Chart

![Bitcoin Market Cycle Chart](chart.png)



## Key Findings

- BTC spent the **majority of days in Bull phase** across 5 years
- Average price during Bull phase was significantly higher 
  than during Bear phase
- BTC price grew from **~$3,500 in 2019** to significantly 
  higher levels by 2023 — showing clear long-term upward trend
- Bear phases, while fewer in days, saw the sharpest 
  short-term price drops



## Skills Demonstrated

- End-to-end data analysis pipeline
-  Real-world data cleaning (missing values, duplicates, dtype fixing)
-  Feature engineering — deriving new columns from existing data
-  Groupby analysis with multiple aggregations
-  Multi-layer matplotlib visualization



## 🚀 How to Run


# 1. Clone this repository
git clone https://github.com/yourusername/btc-market-cycle-analyzer

# 2. Install required libraries
pip install pandas matplotlib

# 3. Open the notebook
jupyter notebook btc_complete_project.ipynb

# 4. Run all cells top to bottom



## 👤 Author

**Garv Pancholi**
📧 garvpancholi2@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/garvp7)
🐙 [GitHub](https://github.com/yourusername)



## 📜 License

This project is open source and available under the MIT License.
