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

The Bid / Purchase Cart supports a maximum of three assets and sends the selected asset details and buyer/payment information to WhatsApp.

## Source

The asset register was structured from the supplied IT Asset Disposal document used for this catalogue.
