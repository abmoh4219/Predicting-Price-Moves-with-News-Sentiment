Predicting Price Moves with News Sentiment
Overview
This project, developed for the 8 Academy AIM Week 1 Challenge, analyzes the relationship between news sentiment and stock price movements. It includes quantitative analysis of stock data using technical indicators (SMA, RSI, MACD) and sentiment analysis of news headlines using NLTK VADER, correlating sentiment with stock returns. The project focuses on stocks: AAPL, AMZN, GOOG, META, MSFT, NVDA, and TSLA.
Repository Structure
├── data/
│   ├── fnspid.csv              # News headlines dataset
│   ├── yfinance_data/          # Stock price data (AAPL.csv, AMZN.csv, etc.)
│   └── processed/              # Processed stock data with indicators
├── notebooks/
│   ├── quant_analysis.ipynb    # Task 2: Quantitative analysis with TA-Lib
│   ├── sentiment_analysis.ipynb # Task 3: Sentiment analysis and correlation
│   ├── final_report.md         # Final report summarizing findings
│   └── *.png                   # Visualization outputs
├── README.md                   # Project setup and info
└── requirements.txt            # Python dependencies

Setup Instructions
Prerequisites

Python 3.8+
Git
Virtual environment tool (e.g., venv)

Installation

Clone the Repository:
git clone https://github.com/abmoh4219/Predicting-Price-Moves-with-News-Sentiment.git
cd Predicting-Price-Moves-with-News-Sentiment


Create and Activate Virtual Environment:
python -m venv venv
source venv/Scripts/activate  # Windows
# or
source venv/bin/activate     # Linux/macOS


Install Dependencies:
pip install -r requirements.txt

Note: ta-lib may require additional setup. See TA-Lib Installation for platform-specific instructions.

Download NLTK Data:
python -c "import nltk; nltk.download('vader_lexicon')"


Verify Data:Ensure data/fnspid.csv and data/yfinance_data/*.csv exist. If not, contact the project maintainer for access.


Running the Notebooks

Start Jupyter Notebook:python -m notebook


Run Notebooks:
Open notebooks/quant_analysis.ipynb for Task 2 (generates technical indicators and saves to data/processed/).
Open notebooks/sentiment_analysis.ipynb for Task 3 (computes sentiment and correlations).


Outputs:
Plots saved in notebooks/.
Processed data saved in data/processed/.



Project Details

Task 2: Quantitative Analysis
Uses TA-Lib to calculate SMA (20-day), RSI (14-day), and MACD for each stock.
Visualizes price trends and indicators.


Task 3: Sentiment Analysis and Correlation
Applies NLTK VADER to analyze news sentiment from fnspid.csv.
Correlates daily sentiment with stock returns.


Challenges:
Optimized performance by sampling news data and reducing plot sizes.
Fixed path issues for saving processed data.



Dependencies
Key libraries (see requirements.txt for full list):

pandas, numpy: Data manipulation
matplotlib, seaborn: Visualization
talib: Technical indicators
nltk: Sentiment analysis
jupyter: Interactive notebooks

Contributing

Fork the repository.
Create a branch: git checkout -b feature-name.
Commit changes: git commit -m "Description".
Push: git push origin feature-name.
Submit a pull request.

License
This project is licensed under the MIT License.
Contact
For issues or questions, contact [your-email] or open a GitHub issue.
