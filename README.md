# Cycle Sniper Trading Strategy

## Current Implementation Status
✅ Implemented:
- FRAMA indicator integration
- T3 indicator integration
- Basic up_down indicator logic (Up_Down_V2)
- Core signal processing for WCL and DCL detection

🔄 In Progress:
- Failed cycle detection and handling
- Multiple trough prediction handling
- Cycle confirmation state management

📝 Planned Features:
- Ticker switching capability with 20-week plotting
- LTR/MTR/RTR implementation
- Unconfirmed cycle visualization (1/3, 2/3, 3/3 states)
- Swing low accurate labeling system

## Core Strategy Components

### 1. Signal Sources
- FRAMA (Primary trend indicator)
- Up_Down_V2 (Momentum indicator)
- Leading cycle timing indicator

### 2. Cycle Detection Methods

#### Method 1 (DCL Focus - Very Bullish Conditions)
- Monitors for 3-4 consecutive red bars
- Confirms on 2 consecutive green bars
- Used outside WCL range
- Priority: Secondary to Method 2 unless in very bullish conditions

#### Method 2 (WCL Focus - Primary Method)
- Requires 5+ consecutive red bars
- Confirms on 2 consecutive green bars
- Primary method for detecting Weekly Cycle Lows
- Takes precedence when strong red sequence (≥5 bars) is present

### 3. Risk Management
- Stop-loss placement below swing lows or FRAMA
- Exit triggers on momentum shifts
- 2% sector exposure limit

## Development Roadmap

### Phase 1: Core Infrastructure (Current)
- [x] Basic indicator implementation
- [x] Signal generation logic
- [x] Initial UI components

### Phase 2: Enhanced Detection (Next)
- [ ] Failed cycle detection
- [ ] Timing-based DCL implementation
- [ ] WCL transition handling
- [ ] DCL after WCL trading logic

### Phase 3: Multi-Asset Support
- [x] Ticker switching functionality
- [ ] 20-week moving average plotting
- [ ] Translation analysis (LTR/MTR/RTR)

### Phase 4: UI/UX Improvements
- [ ] Cycle confirmation state visualization
- [ ] Unconfirmed cycle markers
- [ ] Swing low labeling system
- [ ] Historical cycle display controls

### Phase 5: Edge Cases & Optimization
- [ ] Multiple trough prediction handling
- [ ] Late entry logic refinement
- [ ] Performance optimization
- [ ] Enhanced error handling

## Implementation Notes

### Cycle Confirmation States
1. Confirmed Cycle
   - Indicator: Green dot + "DCL"
   - Condition: Green bars exceed yellow threshold

2. Unconfirmed Cycle
   - Indicator: Yellow dot + "DCL"
   - Condition: Entry signals fired but pending confirmation

3. Failed States
   - Unconfirmed Failure: Yellow dot + "✖️"
   - Confirmed Failure: Red dot + "✖️"

### Priority Rules
1. Method 2 is primary for WCL detection
2. Method 1 takes precedence in very bullish conditions
3. Edge case handling for late entries when no yellow line breach occurs

## Contributing
Please follow the established coding standards:
- Document all indicator calculations
- Include comprehensive error handling
- Follow step-by-step implementation approach
- Break complex tasks into manageable components

## Testing Guidelines
1. Verify cycle detection accuracy
2. Validate confirmation state transitions
3. Test edge case handling
4. Ensure proper risk management enforcement

## Future Considerations
- Enhanced backtesting capabilities
- Additional Confirmation logic 
- Short analysis 
- 
