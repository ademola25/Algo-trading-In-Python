# Trading Signal Generator

This folder contains two implementations of a Trading Signal Generator: a Jupyter notebook and a Python script. Both tools analyze stock metrics and generate automated trading signals based on technical indicators and trading rules.

## Overview

### What These Programs Do

These programs implement a **Trading Signal Generator** that analyzes stock market data and provides BUY, SELL, or HOLD recommendations based on technical analysis:

**Input:**
- User provides the following stock metrics:
  - Stock symbol (ticker, e.g., AAPL, GOOGL)
  - Current price (market price of the stock)
  - 50-day moving average price (trend indicator)
  - 200-day moving average price (long-term trend)
  - RSI value (Relative Strength Index, 0-100 range)
  - Current trading volume (shares traded today)
  - Average trading volume (typical daily volume)

**Processing:**
The program analyzes the metrics using technical analysis rules:

1. **Golden Cross / Death Cross Detection:**
   - Golden Cross: 50-day MA > 200-day MA (Bullish signal)
   - Death Cross: 50-day MA < 200-day MA (Bearish signal)

2. **Percentage Calculations:**
   - Price vs 50-day Moving Average percentage difference
   - Price vs 200-day Moving Average percentage difference
   - Volume vs Average Volume percentage difference

3. **Signal Generation Rules:**
   - **BUY Signal**: Current price > both MAs AND RSI < 70 AND volume > average volume
   - **SELL Signal**: Price < both MAs OR RSI > 70 (overbought condition)
   - **HOLD Signal**: Default when no clear buy/sell conditions are met

4. **Signal Strength Indicators:**
   - Strengthened by Golden/Death Cross patterns
   - Strengthened by extremely high volume (> 1.5× average)
   - Strengthened by extreme RSI values (> 80 for sell signals)

**Output:**
- Technical analysis metrics (price vs moving averages percentages, volume analysis)
- Pattern detection (Golden Cross or Death Cross)
- Clear trading recommendation: **BUY**, **SELL**, or **HOLD**
- Explanation of the recommendation reasoning
- Signal strength indicators showing additional supporting factors
- Context information for better understanding (e.g., "Price is between 50-day and 200-day MAs")

## Files in This Folder

### 1. `trading_signal_generator.ipynb` (Jupyter Notebook)
- Interactive notebook with markdown explanations
- Single code cell containing all signal generation logic
- Prompts for user input and displays analysis results
- Easy to run step-by-step for learning and experimentation

### 2. `trading_signal_generator.py` (Python Script)
- Standalone executable script
- Well-organized with a `main()` function
- Imports only standard library (`os` for universal compatibility)
- Complete signal generation logic in one cohesive program
- Can be run directly from the command line

## How to Use

### Running the Notebook:
- Open `trading_signal_generator.ipynb` in JupyterLab or Jupyter Notebook
- Run the cell by clicking "Run" or pressing Shift+Enter
- Enter your stock metrics when prompted
- View the trading recommendation and technical analysis

### Running the Script:
```bash
python trading_signal_generator.py
```
- Follow the interactive prompts to enter stock metrics
- Receive an analysis with a clear BUY/SELL/HOLD recommendation
- View supporting technical indicators and pattern analysis

## Key Features

✅ **Technical Analysis Indicators**: Analyzes price, moving averages, RSI, and volume  
✅ **Pattern Recognition**: Detects Golden Cross (bullish) and Death Cross (bearish) patterns  
✅ **Rule-Based Signals**: Implements comprehensive trading rules using logical operators  
✅ **Signal Strength**: Provides supporting indicators to strengthen signal confidence  
✅ **Clear Explanations**: Explains the reasoning behind each recommendation  
✅ **User-Friendly**: Interactive prompts and formatted output for easy interpretation  
✅ **Educational**: Demonstrates practical application of Python comparison and logical operators in trading

## Technical Indicators Explained

- **Moving Averages (MA)**: Smoothed price trends over 50 and 200 days
- **Golden Cross**: Bullish signal when short-term MA crosses above long-term MA
- **Death Cross**: Bearish signal when short-term MA crosses below long-term MA
- **RSI (Relative Strength Index)**: Momentum indicator (0-100 scale)
  - < 30: Oversold (potentially undervalued)
  - 30-70: Neutral range
  - > 70: Overbought (potentially overvalued)
- **Volume**: Trading activity; higher volume indicates stronger conviction

## Disclaimer

⚠️ This is a simplified educational tool demonstrating basic technical analysis principles. Real trading decisions should consider multiple factors, risk management, and professional financial advice. Always do thorough research before trading.
