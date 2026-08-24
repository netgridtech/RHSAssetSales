# RHS Asset Sales — Remedial Health IT Gadgets Disposal Clearance Auctioning

GitHub-ready static website for the Remedial Health IT asset disposal / staff clearance auction catalogue.

## Contents

- `index.html` — website entry point
- `data/assets.json` — master 198-asset register used by the website
- `assets/logo.*` — Remedial Health logo
- `assets/images/` — local device visuals grouped by device type

## Deploy with GitHub Pages

1. Upload the contents of this folder to the root of a GitHub repository.
2. Confirm that `index.html` is in the repository root.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select `main` and `/ (root)`, then save.
6. GitHub Pages will publish the site at `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`.

## Important

The site is a static client-side application. The asset catalogue is loaded from `data/assets.json`, so future asset-register updates can be made without editing the main HTML structure.

The Bid / Purchase Cart supports a maximum of one asset and generates a structured CSV bid record and opens an email draft addressed to the three designated Remedial Health recipients. On supported mobile browsers, the native file-share flow can attach the CSV to the selected email app.

## Source

The asset register was structured from the supplied IT Asset Disposal document used for this catalogue.


### CSV export
Purchase requests are exported as UTF-8 CSV with real CRLF row endings and a UTF-8 BOM for Excel/Google Sheets compatibility. Each selected asset occupies one row and the Asset Tag is the primary asset identifier.

### Email bid workflow
The Bid / Purchase Cart is limited to one asset. Submitting the form generates an Excel-compatible CSV and opens an email draft with the required recipients, subject and professional bid body. Browser security prevents a standard `mailto:` link from silently attaching a locally generated file; supported mobile browsers are offered a native file-share flow that can attach the CSV to the selected email application.
