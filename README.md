# Vishnu Hardwear

Offline-first paint price list for Vishnu Hardwear. Open `index.html` in a browser, or serve this folder from any static web host. The PWA caches the app after its first online visit; installed copies keep price and photo edits in browser storage.

## Starter data

The included Nerolac price list is the preverified data supplied in the brief (27 Dec 2025). Three values are flagged for owner review: Beauty Little Master Sheen, 4 L (₹700); Beauty Little Master, 20 L (₹1,700; ₹1,800 was crossed out); Excel Everlast 14, 10 L (₹6,070; ₹610 was crossed out). No product image uploads were present, so all 16 products currently show the no-photo placeholder. The brief identifies a Nerolac Beauty Acrylic Distemper can photo, but that file was not attached.

Owner mode starts with PIN `1234`. Change this PIN and configure your prices before sharing the app. Browser storage is per device. Use the named backup file to move a complete list, including uploaded images, to another device.

## Data files

- `data/seed.json`: app starter data.
- `data/rate-list-extracted.csv`: source rows and review flags.
- `data/image-matches.csv`: image match ledger (empty until product photos are supplied).
- `input/rate-lists/` and `input/images/`: place source uploads here. Originals are excluded from Git by `.gitignore`.
- `input/logo.png` or `input/logo.jpg`: optional shop logo. Without it, the app uses the VH mark in blue.

The UI lets owners import CSV, export the current list, bulk attach photos, and export or restore a JSON backup. CSV imports accept `brand, product, size, price, category, image`; blank price cells stay blank.

## Android

Open `android/` in Android Studio and build the `app` debug variant. Package id: `com.vishnuhardwear.pricelist`. The WebView loads the same app from its assets, enables DOM storage, and includes a multi-select image picker. GitHub Actions builds a debug APK on pushes and publishes it as a workflow artifact.

## GitHub Pages deployment

The action in `.github/workflows/pages.yml` can deploy the static app to GitHub Pages after Pages is configured for GitHub Actions. A live link lets anyone who has it see the prices; share it only with staff. A private source repository does not make a deployed site private. Android APKs are available as Actions artifacts.

## Brand

Use the exact spelling **Vishnu Hardwear**. The browser title, manifest app name, Android app label, staff header, owner and PIN headings, and exported file names follow it. Repository name: `vishnu-hardwear-price-list` (private).

