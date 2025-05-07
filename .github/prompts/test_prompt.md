# Test Generation Instructions for Cycle Sniper

## Test Categories
1. Cycle Detection Tests
   - Verify DCL/WCL identification
   - Test harmonic period calculations
   - Validate cycle confirmation logic

2. Signal Generation Tests
   - Test FRAMA calculations
   - Verify up/down detection
   - Check combined signal logic

3. Risk Management Tests
   - Validate stop-loss calculations
   - Test position sizing logic
   - Verify exposure limits

## Test Structure
- Use describe/it pattern
- Include setup/teardown
- Test edge cases
- Verify error handling

## Data Requirements
- Use realistic market data samples
- Test across different timeframes
- Include volatile market conditions
- Cover multiple asset types
