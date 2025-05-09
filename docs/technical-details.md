# Technical Details

## Core Components

### 1. Cycle Detection System
- **DRO (Dynamic Range Oscillator)**
  - Calculates price momentum using EMA differences
  - Identifies significant swing points in price action
  - Adapts to market volatility automatically
  - Default period: 7 (adjustable 5-12)

### 2. FRAMA (Fractal Adaptive Moving Average)
- **Dual FRAMA System**
  - Daily Cycle FRAMA (Yellow line)
  - Weekly Cycle FRAMA (Blue line)
- **Adaptive Calculation**
  - Uses fractal dimension to adjust smoothing
  - Fast response to volatility changes
  - Self-adjusts based on market conditions

### 3. Cycle Analysis
- **Wavelength Calculation**
  ```
  Wavelength = |Peak Distance - Trough Distance| × 2
  ```
- **Cycle Categories**
  - 20 Day: Short-term cycles
  - 40 Day: Medium-term cycles
  - 60 Day: Intermediate cycles
  - 80 Day: Long-term cycles
  - 20 Week: Extended cycles

### 4. Signal Generation

#### DCL (Daily Cycle Low)
- Requires 3 bars below FRAMA within 4-bar period
- Current close must reclaim FRAMA level
- Offset by 2 bars for visual clarity

#### WCL (Weekly Cycle Low)
- Requires 3 bars below FRAMA within 8-bar period
- Current close must reclaim FRAMA level
- Offset by 5 bars for visual clarity

## Key Calculations

### 1. Bandpass Filter
```
BPF = 0.5 * (1 - α) * (price - price[2]) + β * (1 + α) * BPF[1] - α * BPF[2]

Where:
β = cos(π * (360/Period)/180)
γ = 1/cos(π * (720 * Delta/Period)/180)
α = γ - √(γ² - 1)
```

### 2. FRAMA Calculation
```
FRAMA = (1 - α) * FRAMA[1] + α * Price

Where:
α = Adaptive factor based on fractal dimension
N = (2 - α)/α  // Effective period
```

### 3. Cycle Timing
- **Period**: Distance between cycle points
- **Wavelength**: Full cycle duration
- **Prediction Zones**: ±25% of wavelength around predicted low

## Bandpass Filter Deep Dive

### Implementation Details
```
BPF = 0.5 * (1 - α) * (price - price[2]) + β * (1 + α) * BPF[1] - α * BPF[2]
```

1. **Components Explained**:
   - `price - price[2]`: Measures price change over 2 bars
   - `β`: Controls center frequency response
   - `α`: Determines bandwidth
   - `BPF[1], BPF[2]`: Previous filter outputs

2. **Parameter Selection**:
   ```
   β = cos(2π * fc)              // fc = center frequency
   γ = 1/cos(2π * Δf)           // Δf = bandwidth
   α = γ - √(γ² - 1)            // Filter coefficient
   ```

3. **Frequency Response**:
   - Passes cycles near the target period
   - Attenuates shorter and longer cycles
   - Minimal phase distortion
   - Preserves cycle timing



1. **Signal Processing Steps**:
   ```
   Raw Price → Bandpass Filter → Cycle Detection → Signal Generation
      │              │                │                │
      v              v                v                v
   Noisy Data    Filtered       Peak/Trough      Entry Points
                  Signal        Detection
   ```

2. **Cycle Measurement**:
   ```
   Wavelength = |Peak-to-Trough Distance| × 2
   
   Example:
   Peak at bar 100, Trough at bar 120
   Distance = 20 bars
   Wavelength = 40 bars
   ```

## Cycle Length Examples

### 20-Day Cycle
- **Best For**: Short-term trading, volatile assets
- **Characteristics**:
  - More frequent signals
  - Shorter prediction zones
  - Higher noise sensitivity
- **Example**: Gold miners (GDX) in volatile periods
  ```
  Typical Pattern:
  Day 1-5:    Downtrend
  Day 6-10:   Bottom formation
  Day 11-15:  Uptrend
  Day 16-20:  Top formation
  ```

### 40-Day Cycle
- **Best For**: Standard stocks, medium-term trades
- **Characteristics**:
  - Balanced signal frequency
  - Standard prediction zones
  - Good noise filtering
- **Example**: SPX typical cycle
  ```
  Typical Pattern:
  Day 1-10:   Downtrend
  Day 11-20:  Bottom formation
  Day 21-30:  Uptrend
  Day 31-40:  Top formation
  ```

### 80-Day Cycle
- **Best For**: Crypto, longer-term positions
- **Characteristics**:
  - Fewer signals
  - Wider prediction zones
  - Strong noise filtering
- **Example**: Bitcoin (BTC) major swings
  ```
  Typical Pattern:
  Day 1-20:   Downtrend
  Day 21-40:  Bottom formation
  Day 41-60:  Uptrend
  Day 61-80:  Top formation
  ```

## Prediction Zone Calculation

```
│           Previous          │         Current          │      Future
│             Cycle          │          Cycle           │    Prediction
│                           │                           │
│    ╭╮         ╭╮         │    ╭╮         ╭╮         │    ╭╮
├────╯ ╰───────╯ ╰─────────┼────╯ ╰───────╯ ╰─────────┼────╯ ╰────
│                          │                           │
└──────── Wavelength ──────┴──────── Wavelength ──────┴─── Next ───

Prediction Zone = Current Low + Wavelength ± (Wavelength/4)
```

### Zone Width Calculation
1. **Base Width**: 25% of wavelength on each side
2. **Tolerance**: Additional 10% for market variation
3. **Total Width**: Base width + Tolerance

Example for 40-day cycle:
```
Wavelength = 40 days
Base Width = 10 days each side
Tolerance  = 4 days
Zone Width = 28 days total (10 + 10 + 4 + 4)
```

## Optimization Methods

### 1. Ticker-Specific Settings
- Pre-configured DRO periods
- Optimized harmonic cycle lengths
- Customized for asset characteristics

### 2. Adaptive Features
- Self-adjusting cycle detection
- Dynamic FRAMA smoothing
- Automatic volatility adjustment

## Performance Considerations

### 1. Processing Efficiency
- Uses circular arrays for data storage
- Limited to 1,000,000 data points
- Optimized bandpass calculations

### 2. Memory Management
- Automatic cleanup of old calculations
- Efficient data structure usage
- Smart prediction zone updates

1. **Memory Management**:
   ```
   if array.size(low_indices) > MAX_ARRAY_SIZE
       array.pop(low_indices)
   ```

2. **Calculation Efficiency**:
   ```
   // Efficient FRAMA updates
   frama_val := (1 - α) * frama_val[1] + α * price
   ```

3. **Update Frequency**:
   - Prediction zones: Update only when necessary
   - FRAMA: Updated every bar
   - Cycle detection: Based on price action

## Implementation Notes

### 1. Best Practices
- Use Daily timeframe
- Minimum 200 bars of history
- Enable ticker presets when available

### 2. Technical Limitations
- Maximum lookback: 5000 bars
- Decimal precision: 2 places
- Memory-optimized for long-term usage
