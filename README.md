# Stock-Analysis-with-Traditional-Machine-Learning-and-Deep-Learning-Models

## How to Use This Stock Analysis Framework

This comprehensive framework allows you to analyze stocks using both traditional and deep learning models, then create hybrid models that leverage the strengths of each approach. Here's what this code does:

### Key Features

1. *Data Collection*: Uses Alpha Vantage API to fetch stock data
2. *Feature Engineering*: Creates technical indicators like moving averages, RSI, etc.
3. *Model Implementation*:
   - 5 Traditional models: Linear Regression, Decision Tree, Random Forest, SVR, and KNN
   - Deep learning models: RNN-LSTM and CNN-LSTM
   - Hybrid models: Combined LSTM model and a final hybrid with the best traditional model

### Model Comparison

The framework automatically:
1. Trains all models
2. Evaluates performance using MSE, MAE, and R²
3. Identifies the best traditional model
4. Creates visualizations to compare model performance
5. Generates prediction plots for the most effective models

### How to Run

1. First, obtain an Alpha Vantage API key (free or premium based on your needs)
2. Replace YOUR_ALPHA_VANTAGE_API_KEY with your actual key
3. You can analyze a single stock or multiple stocks:

python
# For a single stock
analyzer = StockAnalyzer(symbol="AAPL", api_key=YOUR_API_KEY)
analyzer.run_full_analysis()

# For multiple stocks
stocks = ['AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA']
results, summary = run_multi_stock_analysis(symbols=stocks, api_key=YOUR_API_KEY)


### Note on API Limits

Alpha Vantage has rate limits (especially on free plans), so the multi-stock analysis includes delays between requests. If you're analyzing many stocks, consider upgrading your API plan or implementing additional handling for rate limits.
