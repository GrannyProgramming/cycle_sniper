# Cycle Sniper Indicator (without SQZMOM)

A comprehensive TradingView Pine Script indicator designed to accurately detect cycle lows (Daily and Weekly), provide predictive future cycle range estimates, and generate confirmed trading signals.

---

## 🔍 Indicator Overview

The Cycle Sniper leverages advanced harmonic cycle analysis combined with DRO (Dynamic Range Oscillator), FRAMA (Fractal Adaptive Moving Average), Larry Williams EMA signals, T3 normalization, and Up/Down bar confirmation methods to:

- Identify historical and future cycle lows.
- Generate actionable entry signals.
- Visualize market cycle dynamics clearly.

---

## ⚙️ Key Features

### ✅ Cycle Detection
- **Daily Cycle Lows (DCL)**: Predict and visualize daily cycle low zones.
- **Weekly Cycle Lows (WCL)**: Forecast weekly cycle low windows.

### ✅ Signal Confirmations
- **Larry Williams EMA Signals**: EMA-based bullish/bearish confirmations.
- **FRAMA Indicator**: Adaptive moving average for cycle alignment.
- **T3 Exit Signals**: Momentum-based exit from oversold conditions.

### ✅ Predictive Features
- **Future Cycle Predictions**: Visualize future potential cycle low ranges.
- **Historical Cycle Predictions**: Display past predictions for cycle analysis accuracy verification.

---

## 🎛️ Customizable Inputs

- **Ticker Presets**: Automatic configuration for BTCUSD, GOLD, NDQ, OIL, or manual input. ( will Update with more assests once matured)
- **Cycle Period Selection**: Choose harmonic periods (20, 40, 60, 80 days, or 20 weeks).
- **FRAMA Settings**: Adjust FRAMA fast and slow moving average parameters. ( set automatically to the optimal cycle length for the Asset)
- **Confirmation Methods**: Enable or disable Larry Williams, FRAMA, and Momentum-based exit from oversold conditions..

---

## 🚀 How to Use

1. **Apply to Chart**: Load the script onto your TradingView chart.
2. **Adjust Inputs**: Use settings to toggle predictions, signals, and select preferred cycles.
3. **Observe Signals**: Watch for plotted signals and future cycle predictions to make informed trade decisions.

---

## 📌 Signal Types

- 🔺 **Larry Williams Long/Short**: Green/red triangles signaling EMA crossovers.
- 🔵 **FRAMA Lines**: Yellow (Daily) and Blue (Weekly) adaptive moving averages.
- 🟢 **Method 1 Signals**: Short red bar sequences followed by green confirmations.
- 🔴 **Method 2 Signals**: Longer red bar sequences confirmed by green bars.
- 🟩 **Integrated Long Entry Signal**: Confirmed signals from selected indicators for safer entries.

NOTE: No longer using Larry Williams or T3
---

## ⚠️ Important Notes

- Always confirm signals with additional technical analysis.
- Adjust parameters according to ticker volatility and cycle length.
- This indicator is designed for educational purposes and should be used with discretion in live trading.

---

**Happy Trading! 🚀**
