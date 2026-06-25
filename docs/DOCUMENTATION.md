# Bankrize Everything — Documentation

Bankrize Everything is a read-only Bankr skill + app for analyzing tokens on Base. It turns a ticker or contract address into a clean, share-ready report: live trading activity, buy/sell flow, a trust score, risk indicators, links, and top pools.

## Documentation index

- [DOCUMENTATION.md](./DOCUMENTATION.md) — this file (overview, features, how it works)
- [TOKEN.md](./TOKEN.md) — the $bnkrize token (burn, contract, launcher)
- [USAGE.md](./USAGE.md) — chat, app, and X/Twitter usage examples
- [TRUST_SCORE.md](./TRUST_SCORE.md) — trust score bands and what feeds them
- [FAQ.md](./FAQ.md) — common questions
- [../SECURITY.md](../SECURITY.md) — read-only scope and security policy
- [../CONTRIBUTING.md](../CONTRIBUTING.md) — how to contribute
- [../CHANGELOG.md](../CHANGELOG.md) — version history

## Overview

- **Network:** Base only
- **Type:** read-only token intelligence (no trading, no signing)
- **Surfaces:** a Bankr App (interactive dashboard) and a Bankr Skill (chat + X/Twitter workflow)
- **Author:** 0xthefear
- **Token:** $bnkrize on Base — see [TOKEN.md](./TOKEN.md)

**Live app:**
https://bankr.bot/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

## The $bnkrize token

Bankrize is paired with the **$bnkrize** token on Base.

- **Contract:** `0x3d59236677AdcfC9dbACB141bA65C0b4c6230Ba3`
- **Launcher:** built with the bankrbot launcher
- **Burn:** $bnkrize has a burn objective and burns — **2.5% burned** so far

Full details in [TOKEN.md](./TOKEN.md).

## Features

When given a valid Base token, Bankrize reports:

- Token name, ticker, and contract address (with one-click copy)
- Price, market cap, liquidity, and 24h volume
- Token age and total transaction activity
- 1h / 6h / 24h activity windows
- Buy vs sell flow with visual flow bars
- Near real-time recent transactions feed
- Trust Score (0–100) with reasons
- Risk Indicators (liquidity, mint/freeze flags, suspicious activity)
- Official website and social links when available
- Top pools by liquidity and volume
- GeckoTerminal deep link

## How it works

The app exposes two server-side scripts:

- **analyzeToken** — fetches live market, activity, risk, socials, and pool data for a token (by ticker or contract) and returns a normalized report object.
- **searchTokens** — resolves a partial ticker/name query into matching Base tokens for the autocomplete picker.

The frontend renders these into the dashboard and auto-refreshes the active token every 30 seconds. All data shown is sourced from the Bankrize workflow — nothing is faked or guessed.

## Trust Score

The trust score is a 0–100 rating derived from the returned market and activity data:

- **70–100:** good
- **35–69:** medium risk
- **0–34:** high risk

Each score is accompanied by short, human-readable reasons. The score is a heuristic, not a guarantee of safety. See [TRUST_SCORE.md](./TRUST_SCORE.md) for the full breakdown.

## Installation

In Bankr, install by giving Bankr the repo URL:

```
install this skill: https://github.com/0xthefear/bankrize-everything-skill
```

## Usage

In chat:

- `use bankrize to analyze this Base token: 0x...`
- `bankrize this token: 0x...`
- `give me a Bankrize report for 0x...`
- `Bankrize on Base: 0x...`

In the app: paste a ticker or Base contract address and hit Bankrize. More examples in [USAGE.md](./USAGE.md).

## X / Twitter format

For X/Twitter replies, the first line must be the `$bnkrize` line and the last line must be the data credit. Example:

```
$bnkrize LFI

Price: $...
Market Cap: $...
Liquidity: $...
24h Volume: $...
1h: ...
6h: ...
Flow: ...
Trust Score: ../100
Risk: ...

Data from @bankrize
```

Rules: don't add `$` before the token unless the user did; never start with "Bankrized on Base" or "Bankrize Everything Report"; nothing comes after the final "Data from @bankrize" line.

## Scope & limits

- Base only — do not analyze tokens on other chains
- Read-only — no swaps, buys, sells, transfers, approvals, claims, mints, deployments, bets, automations, or signatures
- Does not include Base Discovery, Watchlist, Creator Holders, Bankrize Verdict, or Smart Tags sections
- Not financial advice; never promises guaranteed safety; never claims liquidity is locked or that a creator holds/sold unless the data confirms it

See [../SECURITY.md](../SECURITY.md) for the full scope and security policy.

## Credits

Built by 0xthefear. Data and workflow: @bankrize. Token: $bnkrize on Base, built with the bankrbot launcher.
