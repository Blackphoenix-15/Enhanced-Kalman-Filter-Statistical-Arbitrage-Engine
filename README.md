# Enhanced-Kalman-Filter-Statistical-Arbitrage-Engine
# 📈 Kalman Pairs Trading Engine

A statistical arbitrage framework using Kalman Filter to dynamically estimate hedge ratios between cointegrated asset pairs. Enhanced with:

- ✅ **Volatility Scaling**
- ✅ **Dynamic Z-score Thresholds**
- ✅ **Slippage Modeling**
- ✅ **Risk-based Position Sizing**

---

## 🔢 Performance Highlights (KO vs. PEP)

| Metric           | Value         |
|------------------|---------------|
| Sharpe Ratio     | **1.30**      |
| Max Drawdown     | **-7.72%**    |
| CAGR (Simulated) | **18.5%**     |
| Trade Accuracy   | **63.2%**     |

---

## 🧠 Methodology

\[
z_t = \frac{(y_t - \beta_t x_t - \alpha_t)}{\sigma_t}, \quad \text{where } [\beta_t, \alpha_t] \sim \text{KalmanFilter}
\]

Trade signals are generated based on dynamic thresholds:

- Enter Long: \( z_t < -2 \cdot \frac{\sigma_t}{\mu_t} \)
- Exit: \( |z_t| < 0.5 \cdot \frac{\sigma_t}{\mu_t} \)

---

## 📊 Strategy Outputs

- 🔄 Dynamic hedge ratio plots
- 💰 PnL and equity curve
- 🧪 Entry/exit signals marked on spread charts

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
python run_strategy.py --csv data/example_pairs.csv
