# data-projects
 Data analysis and engineering projects — Python, SQL, R, and ML workflows
Insider Trading & Stock Returns — Econometric Analysis
An event study examining whether SEC-reported insider transactions predict short-term stock returns, using Python and SQL.
Overview
This project tests the hypothesis that insider BUY transactions are associated with higher short-term stock returns than insider SELL transactions. Using an event-study framework, I analyzed stock price movements in the 1–5 day window following insider trades reported to the SEC.
Key finding: BUY transactions show meaningfully higher average returns than SELL transactions in the post-transaction window, consistent with the hypothesis that insiders trade on non-public information.
Methodology

Event window: 1–5 trading days after the insider transaction date
Dependent variable: Daily stock return (% change in closing price)
Independent variable: Binary indicator for BUY vs. SELL transaction type
Model: OLS regression (statsmodels) with heteroskedasticity-robust inference
Data: Stock price time series merged with SEC insider transaction records

Tech Stack
ToolPurposePythonData processing, modeling, visualizationPandasData cleaning, merging, time-series manipulationstatsmodelsOLS regression, model evaluationMatplotlibResults visualizationSQL (PostgreSQL)Schema design, data cleaning, aggregation queries
Project Structure

data-projects/
├── analysis.py              # Main Python analysis script
├── sql/
│   ├── schema.sql           # Database schema
│   ├── cleaning.sql         # Data cleaning queries
│   └── analysis.sql         # Analytical SQL queries
├── data/
│   ├── stock_prices.csv     # Daily stock price data
│   └── insider_transactions.csv  # SEC insider transaction records
├── results/
│   └── findings.md          # Summary of key findings
└── README.md



How to Run
bashpip install pandas statsmodels matplotlib
python analysis.py
Skills Demonstrated

Data cleaning and merging across multiple structured datasets
Time-series manipulation and event-window construction
OLS regression modeling and statistical inference
SQL schema design and analytical query writing
Data visualization and findings communication

Author
Kirolos Bekhit — Economics & Informatics, University of Massachusetts Amherst
linkedin.com/in/kirolos-bekhit
