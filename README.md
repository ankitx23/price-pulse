# Price Pulse

An HTML report template for the pricing data that [pricing-analyzer](https://github.com/ankitx23/pricing-analyzer) generates. It turns a `report-data.json` export into a single self-contained dashboard: per-SKU price trends, sparklines, and stability/variability indicators (stable vs. volatile pricing over the tracked window), built to be opened straight from the filesystem with no server needed.

**Live demo:** [ankitx23.github.io/price-pulse](https://ankitx23.github.io/price-pulse/) (seeded with made-up numbers, not real account data)

## How it fits together

`template.html` is the source. A build step swaps the `__REPORT_DATA__` placeholder for real JSON and writes out a standalone `index.html` you can open in a browser. The `index.html` committed here is built from synthetic demo data so the GitHub Pages preview actually works — the real, generated `report-data.json` (and any `index.html` built from it) is gitignored, since both would contain real account pricing data.

## Notes

- Light/dark mode follow the OS preference automatically.
- Sparklines are sized to the actual data width rather than a fixed guess, so they stay accurate at any zoom level.
