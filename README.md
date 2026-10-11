---
license: cc-by-4.0
pretty_name: tickerseer open data
tags:
- finance
- stocks
- valuation
- earnings
---

# tickerseer open data

Aggregate tables from [tickerseer.com](https://tickerseer.com), refreshed monthly. Everything
here is either an aggregate over sub-industries or a row already published on
the site. Per-stock ratings are not in this dataset.

## Files

- `ledger-rows.csv`
- `ledger-scorecard/2026-W41.csv`
- `market-structure/2026-08.csv`
- `market-structure/2026-09.csv`
- `market-structure/2026-10.csv`
- `valuation-temperature/2026-07.csv`
- `valuation-temperature/2026-08.csv`
- `valuation-temperature/2026-09.csv`
- `valuation-temperature/2026-10.csv`

## valuation-temperature/<YYYY-MM>.csv

The monthly Valuation Temperature tables (https://tickerseer.com/reports/valuation-temperature):
`cheapest` (sub-industries by median PEG, with forward growth), `quadrant`
(the quality-against-value quadrant) and `richest_vs_history` (sub-industries
most above their own historical normal P/E) and, where the month file
carries it, `market-structure/<YYYY-MM>.csv` (whole-universe aggregates such as
the median overvaluation). Months 2026-07 to 2026-10. The `universe` column is
each month's own stamp, blank where the file carries none: 2026-07: no universe stamp, 2026-08: no universe stamp, 2026-09: no universe stamp, 2026-10: us. A month
with no stamp was computed over the unfiltered frame, which included some
companies domiciled outside the United States; each month's page on the site
discloses its own share.

## ledger-scorecard/<YYYY-Www>.csv and ledger-rows.csv

The settled earnings-week calls tickerseer published since 2026-05-11,
as of 2026-10-05. `ledger-rows.csv` is the same file the site serves at
https://tickerseer.com/track-record.csv: one row per settled call, with a modeled dollar
withheld where the reconstruction is marked suspect. The scorecard is the
per-structure and per-direction tally from https://tickerseer.com/research. Method pages:
https://tickerseer.com/docs (the ratings and valuation signals), https://tickerseer.com/indices/methodology
(the paper indices), https://tickerseer.com/track-record#methodology (how a call is graded).

## Licence and citation

CC BY 4.0. Cite as: tickerseer, "tickerseer open data", https://tickerseer.com, retrieved <date>.
Kaggle id: tickerseer/tickerseer-open-data.
