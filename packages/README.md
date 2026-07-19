# Server package feed

This folder will host `feed.json` (kind `forge-server-feed`) once the package
CI publishes its first release:

```json
{
  "kind": "forge-server-feed",
  "latest": {
    "name": "…",
    "coreRev": "…",
    "built": "…",
    "url": "https://…/forge-server-pack-….zip",
    "sha256": "<hex>",
    "sizeBytes": 0,
    "notes": "…"
  }
}
```

Until then this folder is intentionally empty — consumers treat a missing feed
as "no feed configured".
