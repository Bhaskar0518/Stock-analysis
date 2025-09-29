# Stock-analysis
This project showcases an interactive Tableau dashboard for analyzing stock performance across major tech companies—Apple (AAPL), Google (GOOG), Microsoft (MSFT), and Netflix (NFLX). It integrates custom buy signal logic based on volume spikes and bullish price action, helping users identify potential entry points for investment.

---

```markdown
# 📈 Stock Buy Signal Dashboard – Tableau

An interactive Tableau dashboard analyzing stock performance for major tech companies using volume spikes and bullish price-action logic to flag potential buy signals.

## 🔍 Overview

This dashboard visualizes stock data for **Apple (AAPL), Google (GOOG), Microsoft (MSFT), and Netflix (NFLX)** across multiple timeframes. It combines traditional price metrics with a custom buy signal algorithm based on volume and price movement.

## 🧠 Signal Logic

Buy signals are flagged when:
- **Volume** exceeds its moving average
- **Close price** is greater than **Open price** (bullish candle)

### Tableau Formula:
```tableau
IF SUM([KVolume]) > WINDOW_AVG(SUM([KVolume]))
AND SUM([Close]) > SUM([Open])
THEN "Buy Signal" ELSE "No Signal" END
```

## 📊 Features

- 📅 **Time Series Charts**: Track closing prices with buy signal markers
- 📈 **Volume Trend Analysis**: Compare daily volume against moving average
- 📌 **Signal Summary Table**: Count and rank buy signals per company
- 🧮 **KPI Cards**: Highlight highest close, lowest open, average volume, and signal count
- 📆 **Date Filters**: Interactive month/year selection
- 🧭 **Multi-Company Comparison**: Pie and bar charts for distribution and value

## 📁 Files Included

- `stock_dashboard.twbx` – Tableau Packaged Workbook
- `stock_data.csv` – Sample dataset with Open, High, Low, Close, Adj Close, Volume
- `report.pdf` – Executive summary with dashboard screenshots and insights
- `README.md` – Project documentation

## 🛠️ How to Use

1. Open `stock analysis.twbx` in Tableau Desktop or Tableau Public
2. Connect to `stock_data.csv` if prompted
3. Explore signal logic, filter by date/company, and review KPI summaries


---

Let me know if you'd like help generating the PDF report or adding a screenshot preview. I can also help you write a short project summary for LinkedIn or your portfolio site.
