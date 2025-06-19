# Predicting Price Moves with News Sentiment

## Week 1 Challenge: Kifiya Artificial Intelligence Mastery (10 Academy)

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-lightgrey?style=flat-square&logo=pandas&logoColor=black)
![NLTK](https://img.shields.io/badge/NLTK-green?style=flat-square&logo=python&logoColor=white)
![TA-Lib](https://img.shields.io/badge/TA--Lib-orange?style=flat-square)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)

---

## 1. Project Overview

[cite_start]This repository presents the solution for the 10 Academy Artificial Intelligence Mastery Week 1 Challenge, focusing on "Predicting Price Moves with News Sentiment"[cite: 1]. [cite_start]The goal is to analyze real-world financial news and discover how headlines shape stock swings, learn to analyze sentiment scores, run technical indicators, and link them to daily returns[cite: 1]. [cite_start]This challenge refines skills in Data Engineering (DE), Financial Analytics (FA), and Machine Learning Engineering (MLE) [cite: 7][cite_start], and is designed to simulate the pressures and deadlines typical in the financial analytics field.

## 2. Challenge Objectives

[cite_start]The project addresses two primary objectives for Nova Financial Solutions:
* [cite_start]**Sentiment Analysis:** Quantify the tone and sentiment expressed in financial news by performing sentiment analysis on the 'headline' text, using natural language processing (NLP) techniques to derive sentiment scores. [cite_start]These scores can be associated with the 'Stock Symbol' to understand emotional context.
* [cite_start]**Correlation Analysis:** Establish statistical correlations between the sentiment derived from news articles and corresponding stock price movements. [cite_start]This involves tracking stock price changes around the article's publication date and analyzing sentiment's impact on stock performance.

## 3. Dataset

[cite_start]The project utilizes the **Financial News and Stock Price Integration Dataset (FNSPID)**, a comprehensive financial dataset designed to enhance stock market predictions by combining quantitative and qualitative data. Key columns include:
* [cite_start]`headline`: News article title, often including key financial actions.
* [cite_start]`date`: Publication date and time, including timezone information (UTC-4 timezone).
* [cite_start]`stock`: Stock ticker symbol (e.g., AAPL for Apple).

For news data, `raw_analyst_ratings.csv` is used, and historical stock data is fetched via `yfinance`.


## 4. Project Structure

.
├── .github/              # GitHub Actions workflows 
│   └── workflows/
│       └── unittests.yml
├── data/                 # Raw and processed data, raw_analyst_ratings.csv
├── notebooks/            # Jupyter notebooks for analysis
│   ├── eda.ipynb         # task 1
│   ├── task_2_analysis.ipynb
│   └── task_3_correlation.ipynb
├── src/                  # Reusable Python code 
│   └── init.py
├── tests/                # Unit tests 
│   └── init.py
├── .gitignore            # Files ignored by Git 
├── README.md             # Project documentation (this file)
└── requirements.txt      # Python dependencies 

## 5. Setup & Installation

### 5.1 Prerequisites
* Python 3.9+
* Git

### 5.2 Steps
1.  **Clone the repository:**
    ```bash
    git clone https://github.com/abeni505/week1-news-sentiment-analysis.git
    cd week1-news-sentiment-analysis
    ```
2.  **Create & activate virtual environment:**
    ```bash
    python -m venv venv-10academy
    source venv-10academy/bin/activate # Linux/macOS
    # For Windows: .\venv-10academy\Scripts\activate
    ```
3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Download NLTK data:**
    ```python
    import nltk
    nltk.download('vader_lexicon')
    nltk.download('punkt')
    ```
    Run these in a Python interpreter or within a notebook cell.

## 6. How to Run

1.  Activate your virtual environment.
2.  Launch Jupyter Lab/Notebook from the project root: `jupyter lab` or `jupyter notebook`.
3.  Navigate to `notebooks/`.
4.  Open and run all cells in `task_2_analysis.ipynb` and `task_3_correlation.ipynb` sequentially to reproduce the analysis.

## 7. Task Breakdown

The challenge was structured into three incremental tasks.

### 7.1 Task 1: Git, GitHub & EDA

* **Objective:** Configure a reproducible Python data-science environment with GitHub integration  and perform Exploratory Data Analysis (EDA) on text and time series data.
* **Key Activities:**
    * Set up a GitHub repository and manage branches (`main`, `task-1`).
    * Commit work frequently with descriptive messages (at least three times a day).
    * Conduct Descriptive Statistics on textual lengths (e.g., headline length) and article counts per publisher.
    * Analyze publication dates to see trends over time.
    * Perform Text Analysis (Topic Modeling) to identify common keywords or significant events.
    * Investigate publisher contributions and differences in news types.

### 7.2 Task 2: Quantitative Analysis

* **Objective:** Compute and visualize technical indicators using financial data.
* **Key Activities:**
    * Load stock price data (Open, High, Low, Close, Volume).
    * Apply TA-Lib and PyNance for technical indicators (MA, RSI, MACD).
    * Visualize data and indicators.
    * Calculate daily stock returns.

### 7.3 Task 3: Correlation Analysis

* **Objective:** Measure the correlation between news sentiment and daily stock returns.
* **Key Activities:**
    * Align news and stock datasets by dates, normalizing timestamps.
    * Conduct sentiment analysis on headlines using `nltk` (VADER) to quantify tone.
    * Compute daily stock returns.
    * Aggregate daily sentiment scores  and calculate Pearson correlation coefficient between sentiment and stock returns.

## 8. Key Learnings

This challenge provided hands-on experience in:
* Configuring Python data-science environments with Git/GitHub integration.
* Performing EDA on diverse data types (text and time series).
* Computing and interpreting financial technical indicators (MA, RSI, MACD).
* Applying NLP for sentiment analysis on news headlines.
* Measuring and interpreting statistical correlations in financial data.
* Effective documentation and report writing.

## Author
Abenezer M. Woldesenbet
