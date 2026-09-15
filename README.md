# Price Pulse

An HTML report template for the pricing data that [pricing-analyzer](https://github.com/ankitx23/pricing-analyzer) generates. It turns a `report-data.json` export into a single self-contained dashboard: per-SKU price trends, sparklines, and stability/variability indicators (stable vs. volatile pricing over the tracked window), built to be opened straight from the filesystem with no server needed.

## How it fits together

`template.html` is the source. A build step swaps the `__REPORT_DATA__` placeholder for real JSON and writes out a standalone `index.html` you can open in a browser. Neither the generated `index.html` nor the `report-data.json` it embeds is committed here, since both would contain real account pricing data — this repo only tracks the template.

## Notes

- Light/dark mode follow the OS preference automatically.
- Sparklines are sized to the actual data width rather than a fixed guess, so they stay accurate at any zoom level.
