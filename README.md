# 📊 Trader Performance vs Market Sentiment Analysis

## 📌 Objective

This project analyzes how Bitcoin market sentiment (Fear vs Greed) influences trader behavior and performance using Hyperliquid trading data.

---

## 📂 Datasets

1. **Bitcoin Market Sentiment**

   * Columns: Date, Classification (Fear / Greed)

2. **Trader Data (Hyperliquid)**

   * Includes: account, trade size, side, PnL, timestamps, etc.

---

## ⚙️ Methodology

### 🔹 Data Preparation

* Cleaned and validated datasets (checked missing values, duplicates)
* Converted timestamps and aligned data at daily level
* Merged sentiment data with trader activity

### 🔹 Feature Engineering

* Daily PnL per trader
* Win rate (binary indicator of profitable trades)
* Trade size (used as proxy for leverage)
* Trade frequency
* Long/Short ratio
* Drawdown proxy (minimum daily PnL)

> *Trade size was used as a proxy for leverage due to the absence of explicit leverage data in the dataset.*

---

## 📊 Analysis

### 1. Performance vs Sentiment

* Compared PnL, win rate, and drawdown across Fear vs Greed

### 2. Behavioral Changes

* Trade frequency
* Position sizes
* Long/Short bias

### 3. Trader Segmentation

* High vs Low risk (based on trade size)
* Frequent vs Infrequent traders
* Consistent vs Inconsistent traders

---

## 🔍 Key Insights

1. Traders achieve higher profitability during **Greed** periods compared to Fear periods.
2. Trade sizes increase significantly during Greed, indicating higher risk-taking behavior.
3. High-risk traders benefit in Greed markets but suffer larger losses during Fear periods.
4. Frequent traders perform better in Greed but tend to overtrade during Fear conditions.

---

## 💡 Strategy Recommendations

### 1. Risk Reduction in Fear Markets

Reduce position sizes and avoid large trades, especially for high-risk traders.

### 2. Selective Aggression in Greed Markets

Increase trading activity and exposure selectively for consistent traders.

### 3. Control Overtrading Behavior (Optional)

Frequent traders should reduce activity during volatile Fear markets.

---

## 🤖 Bonus Work

### Predictive Model

* Built a Random Forest model to predict next-day profitability

### Clustering

* Identified trader archetypes using KMeans clustering

---

## 🛠️ Tech Stack

* Python (Pandas, NumPy)
* Visualization (Matplotlib, Seaborn)
* Machine Learning (Scikit-learn)

---

## ▶️ Setup & How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/krishna26005-debug/Trader-Sentiment-Analysis.git
cd Trader-Sentiment-Analysis
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Notebook

```bash
jupyter notebook notebooks/project.ipynb
```

### 4. View Outputs

* Charts are saved in: `Outputs/Charts/`
* Notebook contains full analysis, insights, and strategies

---

## 📌 Conclusion & Business Impact

Market sentiment significantly influences trader behavior and performance. Traders tend to take higher risks and achieve better returns during Greed periods, while Fear periods expose them to higher downside risk.

This analysis demonstrates how sentiment-driven strategies and trader segmentation can be used to optimize trading performance and improve risk management.

---
