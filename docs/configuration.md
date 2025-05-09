# Configuration Guide

## Main Settings

### Ticker Presets
- **Setting**: `Ticker Presets` (Default: true)
- **Impact**: Automatically applies optimized settings for supported tickers
- **Recommendation**: Keep enabled unless you have a specific reason to use manual settings
- **Supported Tickers**: 50+ major stocks and crypto (BTC, ETH, GOLD, etc.)

### Future Cycle Predictions
- **Setting**: `Show Future Cycle Lows` (Default: true)
- **Impact**: Displays green (DCL) and blue (WCL) prediction zones
- **Usage**: Helps anticipate upcoming cycle lows
- **Accuracy**: Predictions are estimates based on historical cycles

### Historical Predictions
- **Setting**: `Show Historical Cycle Lows Predictions` (Default: true)
- **Impact**: Shows past cycle low predictions as background colors
- **Usage**: Validate indicator accuracy and understand cycle patterns

## Cycle Detection Settings

### DRO Period (Manual Mode)
- **Setting**: `DRO period` (Default: 7, Range: 5-12)
- **Impact**: Controls sensitivity of cycle detection, set manually using the DRO oscillator
- **Optimal Values**:
  - 5-6: Fast-moving assets (Crypto, High-volatility stocks)
  - 7-8: Standard stocks
  - 9-12: Slow-moving assets (Gold, Silver)

### Harmonic Period
- **Setting**: `Harmonic Period` (Options: 20/40/60/80 Day, 20 Week)
- **Impact**: Defines the primary cycle length to track
- **Selection Guide**:
  - 20 Day: Short-term trading, highly volatile assets
  - 40 Day: Standard cycle for most stocks
  - 60 Day: Longer-term trends, stable assets
  - 80 Day: Extended cycles (crypto, commodities)
  - 20 Week: Major market cycles

## FRAMA Settings

### FRAMA Parameters
- **Fast MA**: Controls short-term sensitivity (Default: 1)
- **Slow MA**: Controls long-term smoothing (Default: 200)
- **Impact**: Affects confirmation signal timing
- **Optimization**:
  - Lower Fast MA (1-3): More responsive, more signals
  - Higher Slow MA (150-250): Smoother trend following

## Signal Confirmation

### FRAMA Indicator
- **Setting**: `Show FRAMA Indicator` (Default: true), automatically uses the cycle length to dicate the FRAMA length.
- **Purpose**: Provides trend confirmation
- **Usage**: Wait for price to cross above FRAMA lines for entry confirmation

### Trading Strategy Integration

#### Optimal Settings by Market Type

1. **Crypto Markets**
   - DRO: 5-6
   - Harmonic: 80 Day
   - Example: BTC typically shows 80-day cycles

2. **Stock Markets**
   - DRO: 7-8
   - Harmonic: 40-60 Day
   - Example: SPX shows consistent 40-day cycles

3. **Precious Metals**
   - DRO: 9-11
   - Harmonic: 20 Day
   - Example: GOLD shows shorter, more frequent cycles


## Tooltip Configuration

### Position
- **Options**: Various screen positions
- **Recommendation**: Choose based on chart layout
- **Default**: bottom_right

### Text Size
- **Options**: tiny, small, normal, large, huge
- **Impact**: Affects tooltip visibility
- **Default**: small
