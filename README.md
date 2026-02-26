📊 Trader Performance vs Market Sentiment

Primetrade.ai – Round 0 Assignment
Author: Nishikant Kumar

📌 Project Overview

This project analyzes how Bitcoin market sentiment (Fear/Greed Index) influences trader behavior and profitability on Hyperliquid.

The objective is to uncover statistically supported behavioral patterns and translate them into actionable, sentiment-aware trading insights.

🎯 Objective

We evaluate:

Does trader performance differ between Fear and Greed regimes?

Do traders adjust behavior (risk, size, frequency, direction) based on sentiment?

Are specific trader segments more sensitive to sentiment shifts?

Can these insights inform risk-adjusted trading strategies?

📂 Datasets Used
1️⃣ Bitcoin Fear/Greed Index

Fields: Date, Classification

Frequency: Daily

Used to define sentiment regimes (Fear vs Greed)

2️⃣ Hyperliquid Historical Trader Data

211,224 trade records

Fields include:

Account

Execution Price

Size USD

Closed PnL

Fee

Timestamp IST

Direction (Long/Short)

🛠 Methodology
1️⃣ Data Preparation

Loaded both datasets

Converted timestamps to daily level

Merged trades with daily sentiment

Verified missing values and duplicates

Standardized column formats

2️⃣ Feature Engineering

Created the following metrics:

Net PnL = Closed PnL – Fee

Win indicator (PnL > 0)

Trade size proxy (Size USD)

Risk segmentation (High vs Low risk based on size)

Trade frequency per account

Sentiment binary (Fear = 0, Greed = 1)

3️⃣ Statistical Analysis

Compared mean PnL across regimes

Compared win rates by sentiment

Compared trade size distributions

Conducted t-tests to evaluate statistical significance

Segmented traders (risk-based + frequency-based)

4️⃣ Visualization

PnL distribution by sentiment

Trade size distribution by sentiment

Win rate comparison

Segment-wise performance analysis

📈 Key Insights

Overall profitability does not significantly differ between Fear and Greed regimes (p = 0.28).

High-risk traders perform significantly better during Greed regimes (p = 0.002).

Traders increase position sizes during Fear periods.

Sentiment impact is segment-dependent rather than universal.

Behavioral adjustment is visible in position sizing and trading intensity.

💡 Strategy Recommendations
1️⃣ Dynamic Risk Scaling

Reduce exposure for high-risk traders during Fear regimes to limit volatility amplification.

2️⃣ Sentiment-Based Capital Allocation

Allocate more capital to aggressive strategies during Greed regimes where risk-tolerant traders statistically outperform.

3️⃣ Segment-Specific Adjustment

Apply sentiment-aware adjustments selectively — broad market-wide leverage reduction may not be optimal.

▶️ How to Run
1️⃣ Clone Repository
git clone https://github.com/Nishikant090/Trader-Performance-vs-Market-Sentiment
cd trader-sentiment-analysis
2️⃣ Create Virtual Environment (Recommended)
python -m venv venv

Mac/Linux:

source venv/bin/activate

Windows:

venv\Scripts\activate
3️⃣ Install Dependencies
pip install -r requirements.txt

If requirements.txt is not included:

pip install pandas numpy matplotlib scipy
▶️ Run Notebook
jupyter notebook

Open:

Primetrade_ai.ipynb

Run all cells sequentially.
