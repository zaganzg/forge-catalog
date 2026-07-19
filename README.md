# forge-catalog

Public catalog feeds for AzerothCore 3.3.5a (WotLK) servers: curated Eluna/ALE
Lua scripts, server package feeds, and (soon) optional module listings.

The JSON files in this repository are consumed by tooling over raw URLs — they
are data, not code. Nothing here redistributes third-party content: every
script entry points at its **original public source**, pinned to an immutable
commit, together with the `sha256` of the exact vetted bytes. Consumers must
verify that hash before installing anything.

## Layout

| Path | Kind | Purpose |
| --- | --- | --- |
| `scripts/catalog.json` | `forge-script-catalog` | Curated Eluna/ALE Lua scripts. Each entry: commit-pinned `url` + `sha256` + size, name/author/category/description and optional `setup` note. |
| `packages/` | `forge-server-feed` | Server package feed (`feed.json`) — published once the package CI is live. |
| `modules/` | — | Optional-module listings (package variants) — future. |

## Trust model

- Every script was read and vetted by hand before being listed.
- URLs are pinned to a specific commit, never a branch, so the bytes cannot
  drift out from under the recorded `sha256`.
- A catalog entry is only as good as its hash: if the source ever changes,
  verification fails closed and nothing is installed.

## Contributing

Suggestions for new scripts are welcome via issues, but entries are only added
after manual review of the full source at a pinned commit.
