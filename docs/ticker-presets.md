# Ticker Presets Guide

## Overview
Cycle Sniper comes with optimized settings for 100+ popular tickers. Each preset configures:
- **DRO Period**: Controls cycle detection sensitivity (5-12)
- **Harmonic Period**: Defines primary cycle length to track

## Preset Categories

### Crypto Assets
| Ticker | DRO | Cycle Length | Notes |
|--------|-----|--------------|-------|
| BTCUSD | 6   | 80 Day      | Bitcoin |
| BTBT   | 5   | 80 Day      | Bitcoin miners |
| CIFR   | 5   | 60 Day      | Crypto infrastructure |
| HUT    | 6   | 80 Day      | Mining operation |
| MSTR   | 10  | 40 Day      | Bitcoin holdings |
| RIOT   | 6   | 60 Day      | Mining company |
| COIN   | 7   | 60 Day      | Crypto exchange |

### Precious Metals
| Ticker | DRO | Cycle Length | Notes |
|--------|-----|--------------|-------|
| GOLD   | 9   | 20 Day      | Gold benchmark |
| SILVER | 9   | 20 Day      | Silver prices |
| GDX    | 11  | 40 Day      | Gold miners ETF |
| KGC    | 12  | 20 Day      | Kinross Gold |
| NEM    | 11  | 20 Day      | Newmont Mining |

### Tech Stocks
| Ticker | DRO | Cycle Length | Notes |
|--------|-----|--------------|-------|
| AAPL   | 7   | 40 Day      | Apple Inc. |
| MSFT   | 7   | 40 Day      | Microsoft |
| NVDA   | 7   | 60 Day      | NVIDIA |
| AMD    | 6   | 40 Day      | Advanced Micro Devices |
| GOOGL  | 9   | 20 Day      | Alphabet |

### Market Indices
| Ticker | DRO | Cycle Length | Notes |
|--------|-----|--------------|-------|
| SPX    | 8   | 40 Day      | S&P 500 |
| NDQ    | 8   | 60 Day      | Nasdaq |
| RUT    | 8   | 40 Day      | Russell 2000 |

### Healthcare & Biotech
| Ticker | DRO | Cycle Length | Notes |
|--------|-----|--------------|-------|
| AMGN   | 9   | 40 Day      | Amgen Inc. |
| ELV    | 7   | 60 Day      | Elevance Health |
| JNJ    | 7   | 40 Day      | Johnson & Johnson |
| LLY    | 6   | 40 Day      | Eli Lilly |
| MRK    | 7   | 60 Day      | Merck & Co |
| REGN   | 6   | 20 Day      | Regeneron |
| UNH    | 8   | 40 Day      | UnitedHealth |

### Financial Services
| Ticker | DRO | Cycle Length | Notes |
|--------|-----|--------------|-------|
| AXP    | 8   | 40 Day      | American Express |
| BLK    | 6   | 40 Day      | BlackRock |
| CME    | 10  | 60 Day      | CME Group |
| GS     | 8   | 40 Day      | Goldman Sachs |
| JPM    | 6   | 40 Day      | JPMorgan Chase |
| MA     | 8   | 40 Day      | Mastercard |
| V      | 8   | 40 Day      | Visa |

### Consumer & Retail
| Ticker | DRO | Cycle Length | Notes |
|--------|-----|--------------|-------|
| COST   | 7   | 40 Day      | Costco |
| HD     | 9   | 60 Day      | Home Depot |
| LOW    | 8   | 40 Day      | Lowe's |
| MCD    | 9   | 40 Day      | McDonald's |
| NKE    | 9   | 60 Day      | Nike |
| PG     | 8   | 40 Day      | Procter & Gamble |
| WMT    | 11  | 40 Day      | Walmart |

### Industrial & Energy
| Ticker | DRO | Cycle Length | Notes |
|--------|-----|--------------|-------|
| CAT    | 7   | 40 Day      | Caterpillar |
| CVX    | 8   | 80 Day      | Chevron |
| HON    | 6   | 60 Day      | Honeywell |
| LMT    | 8   | 60 Day      | Lockheed Martin |
| RTX    | 9   | 40 Day      | Raytheon |
| UNP    | 8   | 40 Day      | Union Pacific |
| XOM    | 7   | 40 Day      | ExxonMobil |

## DRO Period Guidelines

### Fast Markets (DRO 5-6)
- Volatile crypto assets
- High-beta tech stocks
- Emerging market stocks

### Standard Markets (DRO 7-8)
- Major indices
- Large-cap stocks
- Traditional tech stocks

### Slow Markets (DRO 9-12)
- Precious metals
- Utility stocks
- Stable value stocks

## Cycle Length Selection

### 20 Day Cycles
- **Best For**: Precious metals, volatile commodities
- **Examples**: GOLD, SILVER, VIX
- **Characteristics**: Frequent signals, shorter swings

### 40 Day Cycles
- **Best For**: Major indices, traditional stocks
- **Examples**: SPX, AAPL, MSFT
- **Characteristics**: Standard market rhythm

### 60 Day Cycles
- **Best For**: Tech stocks, growth stocks
- **Examples**: NVDA, ADBE, CRM
- **Characteristics**: Longer trends

### 80 Day Cycles
- **Best For**: Crypto assets, major trend changes
- **Examples**: BTCUSD, HUT, HIVE
- **Characteristics**: Major market cycles

## Custom Optimization

If your ticker isn't listed:
1. **Similar Asset**: Use settings from a similar ticker
2. **Market Type**: Follow DRO guidelines for market type
3. **Cycle Analysis**: Start with 40 Day and adjust based on results

## Performance Notes

- **Best Results**: Use preset values when available
- **Manual Mode**: Enable when experimenting with settings
- **Validation**: Watch 3-5 cycles before adjusting parameters
