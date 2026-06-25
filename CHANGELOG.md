# Changelog

All notable changes to Bankrize Everything are documented here.
This project follows [Keep a Changelog](https://keepachangelog.com/) and semantic versioning.

## [1.1.0]

### Changed
- App UI fully redesigned (v11): removed the left-side workflow panel for a single-column, focused layout.
- New glassmorphism theme with a premium dark background and a blue–purple–teal gradient accent.
- Added animations: floating aurora glow orbs, staggered card fade-in, soft hover lift on buttons and cards, pulsing live dot, glowing score ring, and shimmer skeletons on load.
- Functionality untouched — scripts, IDs, search, token analysis, trust score, buy/sell flow, pools, and the 30s auto-refresh all behave exactly as before.

### Fixed
- `README.md` rewritten to match real app behavior; removed references to 5-minute activity, average trade size, and largest recent trade (the app does not surface these in the main report).
- Corrected the install URL to the real repository.
- `package.json` author field aligned to `0xthefear`.

### Added
- `docs/DOCUMENTATION.md` — full project documentation.
- `docs/TRUST_SCORE.md` — trust score bands and inputs.
- `docs/FAQ.md` — common questions.
- `docs/USAGE.md` — chat, app, and X/Twitter usage examples.
- `SECURITY.md` — read-only scope and security policy.
- `CONTRIBUTING.md` — contribution and scope rules.
- `.gitignore`.
- `.github/` issue and pull request templates.
- `assets/` folder with screenshot guidance.
- App screenshots embedded in `README.md`.

## [1.0.0]

### Added
- Initial Bankrize Everything skill and app.
- Base-only, read-only token analysis: price, market cap, liquidity, 24h volume, token age, 1h/6h/24h activity, buy/sell flow, near real-time tx feed, trust score, risk indicators, links, and top pools.
- `analyzeToken` and `searchTokens` server-side scripts.
- X/Twitter reply format (`$bnkrize TOKEN` … `Data from @bankrize`).
