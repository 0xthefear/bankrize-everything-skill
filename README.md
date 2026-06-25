# Bankrize Everything Skill

![License](https://img.shields.io/badge/license-MIT-blue)
![Version](https://img.shields.io/badge/version-1.1.0-8b5cf6)
![Network](https://img.shields.io/badge/network-Base-0052ff)
![Read--only](https://img.shields.io/badge/mode-read--only-22c55e)

Bankrize Everything is a read-only Bankr skill + app for analyzing tokens on **Base**. It turns a ticker or contract address into a clean, share-ready report: live trading activity, buy/sell flow, a trust score, risk indicators, links, and top pools.

**Public app:**
https://bankr.bot/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

## Screenshots

![Bankrize dashboard overview](https://i.imgur.com/77Q2NqK.png)

![Token report](https://i.imgur.com/lDgdx3z.png)

![Buy / sell flow](https://i.imgur.com/x15TTqC.png)

![Trust score and risk indicators](https://i.imgur.com/FzLwnGa.png)

![Top pools](https://i.imgur.com/bkeAQsx.png)

## What it does

When given a valid Base token, Bankrize reports:

- token name, ticker, and contract address (with one-click copy)
- price, market cap, liquidity, and 24h volume
- token age and total transaction activity
- 1h / 6h / 24h activity windows
- buy vs sell flow with visual flow bars
- near real-time recent transactions feed
- Trust Score (0–100) with reasons
- Risk Indicators (liquidity, mint/freeze flags, suspicious activity)
- official website and social links when available
- top pools by liquidity and volume
- GeckoTerminal deep link

## What it does not do

- It does not trade: no buy, sell, swap, transfer, approve, sign, claim, mint, deploy, or automation.
- It is **read-only**.
- It is **Base-only**.
- It does not include Base Discovery, Watchlist, Creator Holders, Bankrize Verdict, or Smart Tags sections.

## Install

In Bankr, install this skill by giving Bankr the GitHub repo URL:

```
install this skill: https://github.com/0xthefear/bankrize-everything-skill
```

## Usage

After installing, you can say:

- `use bankrize to analyze this Base token: 0x...`
- `bankrize this token: 0x...`
- `give me a Bankrize report for 0x...`
- `Bankrize on Base: 0x...`
- `$bnkrize LFI`

In the app: paste a ticker or Base contract address and hit Bankrize.

## Trust Score

A 0–100 heuristic rating derived from market and activity data:

- **70–100** — good
- **35–69** — medium risk
- **0–34** — high risk

Each score comes with short, human-readable reasons. It is a heuristic, not a guarantee of safety. See [docs/TRUST_SCORE.md](docs/TRUST_SCORE.md) for the full breakdown.

## Documentation

- [docs/DOCUMENTATION.md](docs/DOCUMENTATION.md) — full overview, features, and how it works
- [docs/USAGE.md](docs/USAGE.md) — chat, app, and X/Twitter usage examples
- [docs/TRUST_SCORE.md](docs/TRUST_SCORE.md) — trust score bands and inputs
- [docs/FAQ.md](docs/FAQ.md) — common questions
- [SECURITY.md](SECURITY.md) — read-only scope and security policy
- [CONTRIBUTING.md](CONTRIBUTING.md) — how to contribute
- [CHANGELOG.md](CHANGELOG.md) — version history

## Credits

Built by [0xthefear](https://github.com/0xthefear). Data and workflow: [@bankrize](https://x.com/bankrize).
