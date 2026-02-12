# Stock Portfolio

This folder contains two implementations of a Stock Portfolio Summary Calculator: a Jupyter notebook and a Python script. Both tools help you analyze and track your stock investments.

## Overview

### What These Programs Do

These programs implement a **Stock Portfolio Summary Calculator** that guides users through analyzing their stock investments step by step:

**Input:**
- User provides information for exactly 3 stocks in their portfolio
- For each stock, the program collects:
  - Stock symbol (ticker, e.g., AAPL, GOOGL)
  - Purchase price per share (original cost)
  - Current price per share (market price)
  - Number of shares owned
- All inputs include validation to ensure positive numeric values

**Processing:**
- The program calculates performance metrics for each individual stock:
  - **Position Value**: Current price × number of shares
  - **Dollar Gain/Loss**: (Current price - Purchase price) × number of shares
  - **Percentage Gain/Loss**: (Dollar gain/loss ÷ Total cost basis) × 100%
  
- Portfolio totals are computed:
  - Total portfolio value
  - Total cost basis (original investment)
  - Total dollar gain/loss
  - Total percentage gain/loss

**Output:**
- Comprehensive summary table showing all 3 stocks with their metrics
- Portfolio totals row with aggregate performance
- Portfolio analysis section identifying:
  - Best performing stock (highest percentage gain)
  - Worst performing stock (lowest percentage gain or highest loss)
  - Overall portfolio status (UP, DOWN, or EVEN) with visual indicators 🟢🔴⚪

## Files in This Folder

### 1. `stock_portfolio.ipynb` (Jupyter Notebook)

To run:
- Open this notebook in JupyterLab or Jupyter Notebook.
- Ensure `yfinance` and `pandas` are installed (`pip install yfinance pandas`).

Note: Prices are fetched live; run the main cell to refresh values.
- Interactive notebook format for step-by-step exploration
- Organized into logical cells:
  - Cell 1: Welcome message and setup
  - Cell 2: Data collection from user
  - Cell 3: Calculations for all metrics
  - Cell 4: Display formatted summary and analysis

### 2. `stock_portfolio.py` (Python Script)
- Standalone executable script with well-organized functions:
  - `clear_screen()`: Clean terminal for better readability
  - `display_welcome()`: Show welcome banner
  - `get_float_input()`: Validated float input with error handling
  - `get_int_input()`: Validated integer input with error handling
  - `collect_stock_info()`: Gather 3 stock entries
  - `calculate_metrics()`: Compute all performance metrics
  - `display_summary()`: Format and show results
  - `main()`: Orchestrate the entire workflow

## How to Use

### Running the Notebook:
- Open `stock_portfolio.ipynb` in JupyterLab or Jupyter Notebook
- Run each cell sequentially by clicking "Run" or pressing Shift+Enter
- Follow the prompts to enter your stock information
- View the formatted portfolio summary and analysis

### Running the Script:
```bash
python stock_portfolio.py
```
- Follow the interactive prompts to enter stock information
- The program will clear the screen and display results formatted in a table
- Shows detailed portfolio analysis with best/worst performers and overall status

## Key Features

✅ Input Validation: Ensures all numeric values are positive and properly formatted  
✅ Error Handling: Graceful handling of invalid user inputs  
✅ Comprehensive Metrics: Calculates position values, gains/losses in dollars and percentages  
✅ Professional Formatting: Well-formatted tables and visual indicators  
✅ Portfolio Analysis: Identifies best/worst performers and overall portfolio health  
✅ User-Friendly: Clear prompts and visual feedback with emojis