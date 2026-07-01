# Ticker-Flexible DCF Model

A DCF model built to be re-run for any company, not rebuilt from scratch each time. Enter a ticker, historicals pull in automatically, you add forward revenue estimates, it outputs an implied share price.

## How it works

1. Enter a ticker → historical financials (revenue, EBIT, D&A, CapEx, NWC, debt, tax) pull automatically
2. Manually paste in forward revenue estimates (not automated — you source these yourself)
3. Model projects unlevered FCF, discounts at WACC, outputs implied share price

## Methodology

CAPM cost of equity, Blume-adjusted beta (sourced externally, not a raw single-stock regression), WACC-weighted discount rate, Gordon Growth terminal value.

## Results

- **MRK**: $149.97 implied — in line with market price (~$125–129) and analyst consensus
- **TSLA**: $137 implied vs. market price (~$400–420) — confirmed the underlying data pulls correctly refreshed for Tesla (not stale MRK data), so this reflects a real disconnect: the market is pricing in growth (robotaxis, FSD, Optimus) that a standard cash-flow forecast can't capture

## Known limitations

- Forward revenue is manual, not pulled live
- Historical data pulls use Google Sheets functions — fully live in Sheets, static fallback values if opened in Excel

## Next steps

WACC/terminal growth sensitivity table, automated forward revenue pull.
