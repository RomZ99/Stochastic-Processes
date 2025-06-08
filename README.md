# Stochastic-Processes

> **Work-In-Progress Archive**  
> Evolving trading-strategy experiments, versioned like a stochastic process.

This repository is an ongoing sandbox of Python and Jupyter-Notebook work in progress. Much like a stochastic process, the code here branches, mutates, and grows over time. You’ll find half-baked ideas, learning artifacts, and reusable building-blocks—even if the top-level strategy isn’t “production-ready” yet.

---

## 🔍 Overview

- **Purpose:**  
  Capture experiments in momentum-based, sector-parity equity strategies, backtest engines, and related helper functions.

- **Status:**  
  **WIP** — this is an _archive_ of experiments, not a finished library. Think of it as a code lab where functions evolve unpredictably (a bit like stock prices!).
---

## ⚙️ Key Reusable Functions

1. **`compute_momentum(prices, lookback_months=12, skip_months=1)`**  
   - Converts a price DataFrame into a momentum-signal DataFrame, with lookback & skip periods.  
   - **Returns:** momentum (dates × tickers)

2. **`sector_parity_selection(signal, sector_map, top_n)`**  
   - Picks the top-n tickers by `signal` while enforcing at most one per sector (then fills remaining slots).  
   - **Returns:** list of ticker strings

3. **`run_backtest(prices, sector_map, capital, …)`**  
   - Orchestrates a weekly rebalance, equal-weight portfolio, optional stop-loss, and NAV calculation.  
   - **Returns:** (`nav`, `positions`)  

---

## 🚧 Usage

1. **Clone this repo**  
   ```bash
   git clone https://github.com/RomZ99/Stochastic-Processes.git
   cd Stochastic-Processes
