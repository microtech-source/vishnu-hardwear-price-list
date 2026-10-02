# Vishnu Hardwear Paint Price List

A mobile-friendly, offline-capable paint price catalog for Vishnu Hardwear. The home screen opens first; Browse Price List moves into searchable product cards with brand and product-type filters.

## Catalog data

`data/seed.json` contains 84 products across Asian Paints, Indigo, Nerolac, Birla, and Perma. Prices and pack sizes are transcribed from the shop's handwritten notebook pages. Empty notebook entries remain “Update soon.” Hard-to-read, corrected, or crossed-out entries are flagged for owner review. No missing amount has been estimated.

- `data/rate-list-extracted.csv` — normalized source rows.
- `data/image-matches.csv` — product image provenance and match notes.
- `public/images/` — locally stored packshots used by the catalog and service worker.

## Run locally

Serve this directory with any static web server and open the root URL. The service worker caches the catalog, styles, scripts, and images after the first visit so the core price list works offline. Owner imports of XLSX files need an internet connection for the optional SheetJS library; CSV, browsing, search, and filters work offline.

Owner mode starts with PIN `1234`; change it on the device before sharing the app. Data edits are stored in that browser/device. Use the backup and restore controls to move data.

## Android

Open `android/` in Android Studio and build the app. Package id: `com.vishnuhardwear.pricelist`; displayed app name: `Vishnu Hardwear`.

## Branding

Shop spelling: **Vishnu Hardwear**. Browser title, PWA name, Android label, screen headers, and exported filenames use this exact spelling. Without `input/logo.png` or `input/logo.jpg`, the app uses the VH icon.
