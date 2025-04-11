# Cycle Indicator Script for TradingView

This script identifies and visualizes cycle lows (Daily Cycle Lows - DCL, Weekly Cycle Lows - WCL) and provides future cycle range predictions based on harmonic and oscillator-based methodologies.

---

## Features

- **Cycle Low Detection:**
  - Identifies Daily Cycle Lows (DCL)
  - Identifies Weekly Cycle Lows (WCL)

- **Future Cycle Predictions:**
  - Projects future cycles based on historical harmonic period analysis
  - Provides oscillator-based cycle range estimations

- **User Interface & Customization:**
  - Toggle visibility for Daily/Weekly Cycle Lows
  - Customize future prediction ranges and visual styles (icons, lines, boxes)

---

## How to Use

1. **Load Script:**
   - Open TradingView
   - Open Pine Script Editor
   - Paste script and save
   - Add the indicator to your chart

2. **Customize Settings:**
   - Open indicator settings (gear icon)
   - Enable/disable DCL and WCL indicators
   - Adjust future prediction visualization

---

## Technical Overview

- **DRO Logic:**
  - Detects swing lows based on price and oscillator divergences

- **Harmonic Period Calculation:**
  - Derives cycles from historical data using harmonic means

- **Oscillator-Based Predictions:**
  - Uses oscillator extremes to estimate future cycle windows

- **Alignment:**
  - Synchronizes future cycle predictions with historic offsets

---

## Troubleshooting

- Ensure Pine Script version compatibility (v5 recommended)
- Check logs in Pine Script Editor for any errors or warnings

---

## Support & Contribution

For any issues or suggestions:
- Raise an issue on GitHub
- Propose enhancements through pull requests

---

## License

Distributed under MIT License. See `LICENSE` for more information.
