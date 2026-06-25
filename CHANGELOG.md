# Changelog

All notable changes to Bankrize Everything are documented here.

## [Unreleased]

### Changed
- App UI fully redesigned (v11): removed the left-side workflow panel for a single-column, focused layout.
- New glassmorphism theme with a premium dark background and a blue–purple–teal gradient accent.
- Added animations: floating aurora glow orbs, staggered card fade-in, soft hover lift on buttons and cards, pulsing live dot, glowing score ring, and shimmer skeletons on load.
- Functionality untouched — scripts, IDs, search, token analysis, trust score, buy/sell flow, pools, and the 30s auto-refresh all behave exactly as before.

### Docs
- Rewrote `README.md` to match real app behavior and fixed the install URL.
- Added `docs/DOCUMENTATION.md`.
- Added this changelog.

## [1.0.0]

### Added
- Initial Bankrize Everything skill and app.
- Base-only, read-only token analysis: price, market cap, liquidity, 24h volume, token age, 1h/6h/24h activity, buy/sell flow, near real-time tx feed, trust score, risk indicators, links, and top pools.
- `analyzeToken` and `searchTokens` server-side scripts.
- X/Twitter reply format (`$bnkrize TOKEN` … `Data from @bankrize`).
