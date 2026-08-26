# Selected Asset & Payment Status Guide

All 198 assets are currently available. No asset is pre-selected.

When an asset is selected and the buyer is confirmed, update `data/selected-assets.json` manually.

## JSON format

```json
{
  "status": "SELECTED",
  "updated": "2026-08-26",
  "count": 1,
  "assetTags": ["84"],
  "assets": [
    {
      "assetTag": "84",
      "buyerName": "John Doe",
      "paymentStatus": "PAID IN PART"
    }
  ]
}
```

### Supported payment statuses

- `PENDING PAYMENT`
- `PAID IN PART`
- `PAID IN FULL`

`buyerName` is optional. If supplied, it is displayed on the selected asset card.

### Important

- Keep `assetTags` and `assets[].assetTag` aligned.
- A selected asset is blocked from new purchase requests.
- The website displays `SELECTED` for unavailable selected items.
- The payment status is informational and can be changed manually after payment confirmation.
- Do not enter sensitive payment details in this public JSON file.
