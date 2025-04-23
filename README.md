# Cycle Sniper Strategy Documentation

## 1. Overview of the Strategy

### Objective
Identify Weekly Cycle Lows (WCL) and Daily Cycle Lows (DCL) using confluence among:
- A leading cycle indicator (predicts timing windows)
- Momentum signals: UP_down (used for both WCL & DCL)
- Trend-based line crosses (FRAMA)

### UP_down's Role
- For bearish momentum: Look for red bars indicating downward momentum
- For bullish momentum: Look for green bars indicating upward momentum
- These transitions apply to both WCL (bearish to bullish shift) and DCL (either bearish exhaustion or ongoing bullish momentum)

## 2. Weekly Cycle Low (WCL) Procedure

For a WCL, we're watching UP_down for a shift from bearish to bullish momentum. You could watch for strengthening bullish signals if the market is already bullish, but typically expect a bottoming scenario (red to green transition).

1. Leading Indicator Window
2. UP_down (red to green transition)
3. FRAMA Cross
4. All-in Confluence
5. Stop-Loss & Exit

## 3. Daily Cycle Low (DCL) Procedure

### 1. Leading Indicator Window
- The leading cycle indicator identifies the date range or bar count for a potential DCL

### 2. FRAMA (Set to DCL Period)
- Settings: A shorter FRAMA period aligned with typical daily cycle length
- Signal: Look for a candle close above the FRAMA line to suggest a potential bottom

### 3. UP_down for DCL
- Bearish-to-Bullish Transition:
  - Watch for a transition from red to green bars, indicating a shift from negative to positive momentum
- Already Bullish Scenario:
  - If UP_down is already showing green bars, look for strengthening signals
  - Interpretation:
    1. Initial green bars indicate positive momentum starting
    2. Multiple consecutive green bars can indicate strengthening momentum
  - Trigger: If this shift occurs during the DCL window—particularly around the time of a FRAMA cross—this can reinforce confidence that the daily cycle low is forming or has formed

### 4. Combined Entry Trigger (DCL)
- Long Entry requires confluence of:
  1. Leading Indicator: We are in the DCL timing window
  2. FRAMA Cross: Candle close above the FRAMA (DCL setting)
  3. UP_down:
     - Shows a transition from red to green bars
     - Or shows strengthening bullish momentum with consecutive green bars
- Waiting Scenario:
  - If UP_down transitions before FRAMA, wait for the additional signal to confirm
  - Then re-check UP_down to ensure it hasn't reverted to red bars

### 5. Stop-Loss and Exit (DCL)
- Stop-Loss:
  - Place it below the most recent swing low or just below FRAMA
- Exit:
  - If price closes back under FRAMA, or if UP_down shows renewed bearish momentum (red bars)
  - If approaching the next WCL window where the price tends to correct on a larger timeframe

## 4. Handling Failed Cycles

### Definition of Failure
- A cycle is deemed failed if a new low is formed after you've identified a cycle low or if momentum indicators revert to strong bearish conditions

### DCL Failure
- If price makes a lower low below the presumed DCL, or FRAMA breaks down immediately, exit the position
- If UP_down reverts back to red bars, that's a sign of renewed bearish momentum—treat that as a failure

## 5. Timing and Practical Checklist

1. Identify the Next WCL or DCL Window
   - Using the leading cycle indicator
2. Indicator Monitoring
   - WCL: UP_down (red to green transition), FRAMA cross (WCL)
   - DCL: FRAMA cross (DCL), UP_down (transition to or strengthening of green bars)
3. Confluence for Entry
   - Aim for signal alignment within the predicted window
4. Risk Management
   - Use stops below swing lows, watch for momentum shifts in UP_down as an exit signal
5. Failure
   - Reassess if price or momentum breaks down again

## 7. Advanced Cycle Analysis

### Cycle Failure Scenarios
1. Full Confirmation Failure
   - Definition: When all three confirmation signals have fired (Leading Indicator, UP_down, and FRAMA), but price makes a new low below the identified cycle low
   - Characteristics:
     - Price breaks below the identified cycle low point
     - Often accompanied by accelerated downward momentum
     - Can indicate a larger market structure breakdown
   
   Risk Management Actions:
   - Immediate position exit when price breaks the cycle low
   - Increase cash position
   - Wait for new confirmation signals before re-entry
   - Consider this a warning sign for larger timeframe cycles

2. Post-Confirmation Breakdown Patterns:
   - False Breakout Pattern:
     - Initial bounce followed by swift reversal
     - Usually occurs within 3-5 bars of confirmation
   - Slow Grind Down:
     - Gradual erosion of support
     - UP_down may show weakening momentum before price breakdown
   - Cascade Failure:
     - Sharp, immediate reversal
     - Often triggered by external market events

### Unconfirmed Cycles
1. Definition: When only 2 out of 3 confirmation signals have fired

2. Common Scenarios:
   a) Leading Indicator + UP_down (No FRAMA):
      - Higher risk scenario
      - Consider smaller position sizes
      - Requires tighter stop losses
      - Wait for FRAMA confirmation before full position

   b) Leading Indicator + FRAMA (No UP_down):
      - Moderate risk scenario
      - Momentum confirmation missing
      - Watch for potential momentum shift
      - Consider scaling in approach

   c) UP_down + FRAMA (No Leading Indicator):
      - Timing uncertainty
      - May be early or late in cycle
      - Risk of catching false bottom
      - Requires broader market context

3. Risk Management for Unconfirmed Cycles:
   - Reduce position size to 30-50% of normal
   - Use tighter stop losses
   - Scale in approach recommended
   - Exit if remaining signal doesn't confirm within expected window
   - Monitor volume for additional confirmation

4. Trading Strategy Adjustments:
   - Wait for third confirmation if market volatility is high
   - Consider broader market conditions
   - Use multiple timeframe analysis
   - Monitor related assets for confirmation
   - Consider options strategies instead of direct positions

5. Recovery Scenarios:
   - If missing signal confirms later:
     - Can scale up position size
     - Adjust stops to normal levels
     - Resume standard risk management
   - If missing signal fails to confirm:
     - Maintain reduced position size
     - Consider early exit
     - Document for pattern recognition
