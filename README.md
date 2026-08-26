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

The Bid / Purchase Cart supports a maximum of two assets, with only one asset allowed from each device type, and generates a structured CSV bid record and opens an email draft addressed to five designated Remedial Health recipients. The catalogue currently has no pre-selected/unavailable assets; all 198 assets are available for selection. The email draft is pre-addressed to the designated Remedial Health recipients and the CSV is downloaded for attachment.

## Source

The asset register was structured from the supplied IT Asset Disposal document used for this catalogue.


### CSV export
Purchase requests are exported as UTF-8 CSV with real CRLF row endings and a UTF-8 BOM for Excel/Google Sheets compatibility. Each selected asset occupies one row and the Asset Tag is the primary asset identifier.

### Email bid workflow
The Bid / Purchase Cart supports a maximum of two assets, with only one asset permitted from each device type. Submitting the form generates an Excel-compatible CSV and opens an email draft with the required recipients, subject and professional bid body. Browser security prevents a standard `mailto:` link from silently attaching a locally generated file; supported mobile browsers are offered a native file-share flow that can attach the CSV to the selected email application.

### Current availability state
All 198 assets are currently available. The `data/selected-assets.json` file is intentionally empty (`count: 0`, `assetTags: []`). If an asset is later reserved/selected by the administrator, add its Asset Tag to that file and the site will mark it as SELECTED.

## Current selection rules

- Buyers may select a maximum of **2 assets** per request.
- A buyer may select **only 1 asset from each device type**. For example, Laptop + Phone is valid; Laptop + Laptop is not.
- The rule is enforced in the browser before submission.
- All 198 assets are currently available; no asset is pre-selected.

## Payment deadline

The sale basis is **CASH AND CARRY**. Buyers are expected to make payment by **31st August 2026**. If payment is delayed beyond that date, the selected item(s) may be made visible to the general public.

## Selected asset administration

Use `data/selected-assets.json` to manually mark an asset as selected and optionally record the buyer name and payment status. See `SELECTED_ASSET_ADMIN_GUIDE.md` for the supported structure and payment statuses.
