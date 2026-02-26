📌 Project Overview

This project analyzes how Bitcoin market sentiment (Fear/Greed Index) relates to trader behavior and performance on Hyperliquid.

The goal is to uncover statistically supported patterns that can inform smarter, sentiment-aware trading strategies.

🎯 Objective

To evaluate:

Does trader performance differ between Fear and Greed regimes?

Do traders change behavior based on sentiment?

Are certain trader segments more affected by sentiment?

Can these insights inform risk-adjusted strategy recommendations?

📂 Datasets Used

Bitcoin Fear/Greed Index

Fields: Date, Classification

Frequency: Daily sentiment regime

Hyperliquid Historical Trader Data

211,224 trade records

Fields include:

Account

Execution Price

Size USD

Closed PnL

Fee

Leverage (if applicable)

Timestamp IST

Direction (Long/Short)

🛠 Methodology
1️⃣ Data Preparation

Loaded both datasets

Converted timestamps to daily level

Merged trade data with daily sentiment

Checked for missing values & duplicates

2️⃣ Feature Engineering

Created the following metrics:

Closed PnL

Net PnL (Closed PnL – Fee)

Win indicator

Trade size (Size USD)

Risk segments (High vs Low risk)

Sentiment binary (Fear vs Greed)

3️⃣ Statistical Analysis

Compared mean PnL across regimes

Compared win rate and trade size

Conducted t-tests to validate statistical significance

Segmented traders by risk profile

4️⃣ Visualization

High-risk PnL distribution by sentiment

Trade size distribution by sentiment

Win rate comparison

📈 Key Insights

Overall profitability does not significantly differ between Fear and Greed regimes (p = 0.28).

High-risk traders perform significantly better during Greed regimes (p = 0.002).

Traders increase position sizes during Fear periods.

Sentiment impact is segment-dependent rather than universal.

💡 Strategy Recommendations

Dynamic Risk Scaling
Reduce leverage exposure for high-risk traders during Fear regimes.

Sentiment-Based Capital Allocation
Allocate more capital to aggressive strategies during Greed periods.

1️⃣ Clone Repository
git clone https://github.com/your-username/trader-sentiment-analysis.git
cd trader-sentiment-analysis
2️⃣ Create Virtual Environment (Recommended)
python -m venv venv
source venv/bin/activate     # Mac/Linux
venv\Scripts\activate        # Windows
3️⃣ Install Dependencies
pip install -r requirements.txt

If requirements.txt is not provided, install manually:

pip install pandas numpy matplotlib seaborn scipy
▶️ How to Run
Option 1 — Jupyter Notebook
jupyter notebook

Open:

Primetrade_ai.ipynb

Run all cells sequentially.

Option 2 — Python Script
python primetrade_ai.py

Ensure datasets are placed in the same directory as the script.
