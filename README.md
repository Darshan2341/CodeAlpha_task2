# Stock Portfolio Tracker

A Python-based Stock Portfolio Tracker that allows users to manage and track their stock investments. The program allows you to add stocks to your portfolio, remove stocks, and track the value and performance of your investments in real-time by querying current stock prices.

## Features

- **Add/Remove Stocks**: Add or remove stocks from your portfolio with the ability to specify the number of shares and purchase price.
- **Real-time Stock Price Fetching**: Fetch the latest stock prices using `yfinance`.
- **Portfolio Value Calculation**: Calculate the current value of your portfolio based on real-time stock prices.
- **Profit/Loss Calculation**: Track the profit or loss for each stock and your overall portfolio.
- **Cost Basis Tracking**: The program keeps track of the price at which each stock was purchased.

## Requirements

- Python 3.x
- `yfinance` library (for fetching stock prices)

### Install Dependencies

You can install the required dependencies using `pip`:

```bash
pip install yfinance
How to Run
Clone this repository to your local machine:
bash
Copy
git clone https://github.com/your-username/stock-portfolio-tracker.git
Navigate to the project directory:
bash
Copy
cd stock-portfolio-tracker
Run the stock portfolio tracker:
bash
Copy
python stock_portfolio_tracker.py
The program will display the current portfolio value and performance of the stocks in the portfolio, including profit/loss.
Example Usage
Below is an example of how you can interact with the program:

python
Copy
portfolio = StockPortfolio()

# Adding stocks to the portfolio with cost price
portfolio.add_stock("AAPL", 10, 150.00)  # 10 shares of Apple at $150 each
portfolio.add_stock("GOOGL", 5, 2800.00)  # 5 shares of Google at $2800 each
portfolio.add_stock("AMZN", 2, 3500.00)   # 2 shares of Amazon at $3500 each
portfolio.add_stock("TSLA", 3, 700.00)    # 3 shares of Tesla at $700 each

# Display portfolio value and performance
portfolio.calculate_portfolio_value()

# Removing stocks and recalculating
portfolio.remove_stock("TSLA", 1)  # Sell 1 share of Tesla
portfolio.calculate_portfolio_value()
Sample Output:
pgsql
Copy
AAPL: 10 shares @ $170.45 = $1704.50, Cost Basis = $1500.00, P/L = $204.50
GOOGL: 5 shares @ $2850.00 = $14250.00, Cost Basis = $14000.00, P/L = $250.00
AMZN: 2 shares @ $3400.00 = $6800.00, Cost Basis = $7000.00, P/L = -$200.00
TSLA: 3 shares @ $800.00 = $2400.00, Cost Basis = $2100.00, P/L = $300.00
Total Portfolio Value: $23654.50
Total Portfolio Cost Basis: $22600.00
Total Portfolio Profit/Loss: $1054.50
