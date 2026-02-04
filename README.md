
The goal of this project is to analyze how **market sentiment (Fear vs Greed)** impacts **trader behavior and performance** on the Hyperliquid trading platform.  
The analysis aims to uncover **behavioral patterns and actionable insights** that can inform smarter trading strategies.

## Datasets Used

## Bitcoin Market Sentiment (Fear/Greed Index)
Columns:
- `date` – Date of sentiment observation
- `classification` – Fear or Greed
- `value` – Fear & Greed index score

## Hyperliquid Historical Trader Data
Key fields used:
- `account` – Trader account ID
- `coin` – Traded asset
- `side` – Buy / Sell
- `size_usd` – Trade size in USD
- `closed_pnl` – Profit or Loss of the trade
- `timestamp_ist` – Trade execution time (IST)

## Data Preparation

Steps performed:
- Standardized column names for consistency
- Converted timestamps to proper datetime format
- Aligned both datasets at **daily level**
- Handled missing values and verified data quality
- Aggregated trade-level data into **daily trader-level metrics**

## Key Metrics Created:
- Daily PnL per trader
- Win rate
- Trade frequency
- Average trade size
- Total traded volume
- Long/Short ratio


## Analysis Performed

## Performance vs Sentiment
- Compared daily PnL, win rate, and volatility across **Fear vs Greed** days
- Visualized distributions using boxplots and summary statistics

## Behavior vs Sentiment
- Studied changes in:
  - Trade frequency
  - Trade size
  - Risk-taking behavior
- Observed behavioral shifts under different sentiment regimes

## Trader Segmentation
Traders were segmented into:
- High vs Low Activity Traders
- Consistent vs Inconsistent Traders

Each segment was analyzed separately across Fear and Greed days.

## Key Insights

1. Trader PnL tends to be more volatile during **Greed** days, while **Fear** days show reduced variance but lower median returns.
2. High-activity traders experience sharper drawdowns during Fear regimes compared to low-activity traders.
3. Consistent traders maintain relatively stable performance across sentiment regimes, indicating disciplined strategies outperform reactive behavior.


## Actionable Strategy Recommendations

1. Risk Control Rule:  
   During Fear days, reduce trade frequency and exposure for high-activity traders to minimize drawdowns.

2. Selective Aggression Rule: 
   Allow consistent traders to increase activity during Greed days, while restricting inconsistent traders from overtrading.



## Bonus 
- Built a simple baseline model to predict daily trader profitability using behavioral and sentiment features.
- The model serves as an exploratory tool rather than a production-ready predictor.


## How to Run

## Requirements
- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn 
Install dependencies:
```bash
pip install -r requirements.txt
