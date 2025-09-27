# Magic Trend (Pine Script v6)

A TradingView indicator that blends CCI-anchored trend bands with ATR buffers, multi-timeframe (MTF) trend dashboard, projected trend line, S/R zone fill, and alertable buy/sell flips.

> Version **1.1** · 2025-09-27

## Features
- **Trend line** based on CCI regime (+/-) with ATR buffers
- **Buy/Sell signals** on directional flips
- **Projected trend line** (linebreak style) for context
- **Trend strength classification**: Highly/Moderately Bullish/Bearish, Sideways
- **Compact MTF dashboard**: D, W, M, 3M (Q), 12M (Y)
- **Support/Resistance zones** via rolling swing highs/lows
- **Alerts** for Buy/Sell flips

## Install in TradingView
1. Open TradingView ➜ **Pine Editor**.
2. Create a new script and paste the contents of [`src/MagicTrend_V1_1.pine`](src/MagicTrend_V1_1.pine).
3. Click **Add to chart**. Adjust inputs in the settings panel.
4. To enable alerts: **Alerts** ➜ choose *Buy Alert* or *Sell Alert* conditions.

## Inputs
| Name | Default | Purpose |
|---|---:|---|
| `cciLength` | 20 | CCI period. |
| `atrLength` | 5 | ATR smoothing window (via `ta.sma(ta.tr(true))`). |
| `multiplier` | 1.0 | ATR buffer multiplier. |
| `originalColoring` | true | Color by CCI regime (true) or line slope (false). |
| `showSignals` | true | Toggle label-up/down markers on flips. |
| `showProjection` | true | Show projected (last) trend line. |
| `showMTFDashboard` | true | Show MTF compact table (D/W/M/3M/12M). |
| `slopeHigh` | 0.5 | Threshold for Highly Bullish/Bearish. |
| `slopeLow` | 0.15 | Threshold for Moderately Bullish/Bearish. |
| `showSRZones` | true | Show filled S/R band from swing highs/lows. |
| `srLookback` | 20 | Lookback window for swing highs/lows. |

## Files
```
.
├── src/
│   └── MagicTrend_V1_1.pine
├── examples/
│   └── README.md
├── .gitignore
├── CHANGELOG.md
├── LICENSE
└── README.md
```

## Local development
No build step needed—this is standard Pine Script. For versioning, update the indicator title string and add an entry to `CHANGELOG.md`.

## Contributing
Issues and PRs welcome. Please avoid repainting logic suggestions unless accompanied by reproducible evidence or code.

## License
MIT (see `LICENSE`).

---

> _Disclaimer: For research and educational purposes only. Not financial advice._
