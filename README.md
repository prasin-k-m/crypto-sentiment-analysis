# 📊 Crypto Market Sentiment vs Trader Performance Analysis

## 🧠 Project Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear & Greed Index) and trader performance using historical trading data. The objective is to uncover patterns in trading behavior and profitability under different market sentiment conditions, and to derive insights that can support smarter trading decisions.

---

## 📁 Datasets Used

### 1. Bitcoin Market Sentiment Dataset
| Column | Description |
|--------|-------------|
| `date` | Date of sentiment record |
| `classification` | Extreme Fear, Fear, Neutral, Greed, Extreme Greed |
| `value` | Sentiment score |

### 2. Historical Trader Data
| Column | Description |
|--------|-------------|
| `Account` | Trader account ID |
| `Coin` | Cryptocurrency traded |
| `Execution Price` | Price at trade execution |
| `Size USD` | Position size in USD |
| `Side` | Buy or Sell |
| `Timestamp IST` | Trade timestamp |
| `Closed PnL` | Profit or loss on closed trade |

---

## ⚙️ Methodology

### 🔹 Data Preprocessing
- Converted timestamp columns to datetime format
- Extracted date for alignment across datasets
- Checked for missing values and duplicates

### 🔹 Data Integration
- Merged trader data with sentiment data using the `date` column
- Used inner join to ensure only overlapping periods were analyzed

### 🔹 Feature Engineering
Created key variables:
- `profit` → Closed PnL
- `win` → Profitable trade indicator
- `trade_size` → Position size in USD

### 🔹 Exploratory Data Analysis (EDA)
Analyzed:
- Average profit by sentiment
- Win rate by sentiment
- Trade size behavior across sentiment levels

Visualizations:
- Bar plot → Profit vs Sentiment
- Box plot → Profit distribution
- Line plot → Daily total profit

---

## 📊 Key Findings

- **Profitability increases with bullish sentiment**, with Extreme Greed showing the highest returns
- **Fear conditions outperform normal Greed**, suggesting traders benefit from buying during market downturns
- **Win rates remain below 50%** across all sentiment levels, indicating market uncertainty
- **Traders take larger positions during Fear**, reflecting aggressive risk-taking behavior
- **Sentiment shows weak linear correlation** with profit, meaning it is not a standalone predictor
- **Profit distribution** indicates a high-risk, high-reward environment with extreme outliers

---

## 📈 Visualizations

The project includes:
- Average Profit by Sentiment
- Profit Distribution by Sentiment
- Daily Total Profit Trend

---

## 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 📌 Conclusion

Market sentiment influences trading performance, but it does not fully determine profitability. A combination of sentiment, risk behavior, and market dynamics plays a crucial role in trading outcomes.

---

## 📂 Project Structure

crypto-sentiment-analysis/
│
├── data/
│   ├── fear_greed_index.csv
│   └── historical_data.csv
│
├── notebook.ipynb
└── README.md

---

## 👤 Author

**Prasin K M**  
Data Science Intern | Aspiring AI/ML Engineer
