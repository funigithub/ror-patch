# ror-patch — Risk of Ragnarok patch site (GitHub Pages host)

This **public** repository exists only to serve the Risk of Ragnarok patcher
content over **GitHub Pages** at:

> https://funigithub.github.io/ror-patch/

It is **generated** — do not hand-edit. The source of truth, tooling, and
release process live in the **private** `funigithub/risk-of-ragnarok-patcher`
repo, which assembles this site and pushes it here. See that repo's
`docs/release-process.md`.

## What's served here

| Path | Purpose |
|---|---|
| `/patch/main/patch_main.txt` | the Elurair patch list (what the launcher reads) |
| `/patch/main/ror-*.zip` | small / incremental patch payloads |
| `/patch/main/patch_allow.txt` | maintenance kill-switch (`deny` body = maintenance) |
| `/latest.json` | latest version + sha256/size |
| `/news.json` | news feed |
| `/server-status.json` | online / maintenance flag |
| `/index.html`, `/assets/` | landing page |
| `/patch-notes/*.html` | rendered patch notes |

Large / full-client downloads are **not** here; they live on the private repo's
GitHub Releases.

Pages deploy is handled by `.github/workflows/deploy-pages.yml` on every push to
`main`.
