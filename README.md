# Stock Analysis Tool

## Description
This tool is designed to analyze stock data using **Polygon.io** and **NewsAPI**. It provides historical stock data with RSI (Relative Strength Index) and RSI moving average calculations, sentiment analysis of related news articles, and buy/sell recommendations.

The tool is ideal for traders, investors, and data enthusiasts who want to integrate sentiment analysis and technical indicators into their decision-making.

---

## Features
- Fetch historical stock data for the last 3 months using **Polygon.io API**.
- Perform sentiment analysis on news articles using **NewsAPI**.
- Calculate **RSI** and **RSI Moving Average** for technical analysis.
- Provide a detailed report for the last 15 trading days.
- Generate buy/sell recommendations based on RSI and sentiment analysis.
- Securely manage API keys using environment variables.

---

## Requirements
- Python 3.7 or higher
- Required libraries:
  - `requests`
  - `pandas`
  - `pandas-ta`
  - `textblob`
  - `python-dotenv`
- Valid API keys for:
  - **Polygon.io** (Free API available, sign up here https://polygon.io/
  - **NewsAPI** (Free API available, sign up here https://newsapi.org/

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name.git
   cd your-repo-name
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up environment variables:
   - Create a `.env` file in the project directory:
     ```env
     POLYGON_API_KEY=your_polygon_api_key
     NEWS_API_KEY=your_news_api_key
     ```
   - Replace `your_polygon_api_key` and `your_news_api_key` with your actual API keys.

4. Make the script executable:
   ```bash
   chmod +x script_name.py
   ```

---

## Usage

Run the script with the following command:
```bash
python script_name.py TICKER
```

### Example:
```bash
python script_name.py AAPL
```

- Replace `script_name.py` with the name of the Python file.
- Replace `AAPL` with the stock ticker you want to analyze.

### Output
The script generates a report for the last 15 trading days, showing:
- Date
- Open, High, and Close prices
- RSI and RSI Moving Average
- Sentiment score and count of news articles
- Buy/Sell recommendations

---

## Environment Variables

This script uses the following environment variables:
- `POLYGON_API_KEY`: Your **Polygon.io** API key.
- `NEWS_API_KEY`: Your **NewsAPI** key.

Ensure that these are stored in a `.env` file for secure access.

---

## Example Output

```
Date: 2024-11-27, Open: 45.50, High: 47.80, Close: 46.90, RSI: 58.40, RSI MA: 55.70, Sentiment Score: 72, News Count: 5, Recommendation: Buy
Date: 2024-11-26, Open: 46.10, High: 47.00, Close: 46.30, RSI: 54.90, RSI MA: 54.10, Sentiment Score: 62, News Count: 3, Recommendation: Neutral
```

---

## Recommendations Logic

- **Strong Buy:** Sentiment score > 70 and RSI < 30.
- **Buy:** Sentiment score > 50 and RSI < 50.
- **Neutral:** Sentiment score between 40–60 and RSI between 40–60.
- **Sell:** Sentiment score < 50 and RSI > 70.
- **Strong Sell:** Sentiment score < 30 and RSI > 70.

---

## Support

For issues or questions, please open an [issue on GitHub](https://github.com/your-repo-name/issues) or contact `fhrml1004@korea.ac.kr`.

Happy analyzing! 🚀
