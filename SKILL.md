---
name: bankrize-everything
description: Use Bankrize Everything to analyze Base tokens with live activity, trust score, liquidity, risk indicators, and clean share-ready reports.
version: 1.0.0
author: 0xc027ecbd0fa38f667a25550aae56b14c73931d5a
tags:
  - bankrize
  - token-analysis
  - crypto
  - onchain
  - bankr
---

# bankrize Everything Skill

Bankrize Everything is a Bankr workflow for analyzing Base tokens using the public Bankrize Everything app.

Canonical app:
/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

Public app:
https://bankr.bot/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

Use this skill when the user says any of:

- use bankrize
- use Bankrize Everything
- bankrize this
- bankrize this token
- analyze this with bankrize
- analyze this Base token
- check this Base token
- give me a Bankrize report
- Bankrize report
- Bankrize on Base
- Bankr use bankrize
- use bankrize to analyze this token
- bnkrize this
- $bnkrize this
- bankrize

## Scope

This skill is Base-only.

Only analyze tokens on Base.

Do not perform swaps, buys, sells, transfers, claims, approvals, mints, deployments, bets, automations, or signatures.

This skill is read-only.

This skill must only use the Bankrize Everything workflow and app output as the source of the analysis.

Do not replace Bankrize with another token-analysis workflow.

Do not present data as Bankrize data unless it comes from the Bankrize Everything app/workflow or the user provides a Bankrize result.

## Core X/Twitter rule

When responding to a tweet, quote tweet, X post, or preparing an X/Twitter reply where the user asks to Bankrize a token, the first line of the response must be:

$bnkrize TOKEN

Rules:

- The first line must start with $bnkrize.
- Put the analyzed token immediately after $bnkrize.
- Do not put $ before the analyzed token unless the user already included $ in the original request.
- If the user says “bankrize LFI”, first line must be:
  $bnkrize LFI
- If the user says “bankrize $LFI”, first line may be:
  $bnkrize $LFI
- Do not start X/Twitter replies with “Bankrized on Base”.
- Do not start X/Twitter replies with “Bankrize Everything Report”.
- For X/Twitter replies, the first visible line must be the $bnkrize line.

The final line of every X/Twitter Bankrize reply must be:

Data from @bankrize

Nothing should come after that final line

## What Bankrize analyzes

When a valid Base token is provided, Bankrize focuses on:

- token name
- ticker
- contract address
- price
- market cap
- liquidity
- 24h volume
- token age
- transaction activity
- 1-hour activity
- 6-hour activity
- 24-hour activity
- buy vs sell flow
- real-time or near real-time transaction feed
- volume spikes if available
- unusual activity if available
- trust score
- risk indicators
- official website if available
- social links if available
- top pools if available

## Current app behavior

The current Bankrize Everything app uses:

- 1h activity
- 6h activity
- 24h buy/sell flow
- Trust Score
- Risk Indicators
- Links & Pools
- GeckoTerminal link
- contract copy next to the contract address

The current app does not use 5-minute activity in the main Live Activity section.

Do not force 5m fields into the main report unless Bankrize output explicitly provides them.

## Important removed sections

Do not include these sections:

- Base Discovery
- Watchlist
- Creator holders
- Bankrize Verdict
- Smart Tags

The current Bankrize Everything app intentionally does not include Base Discovery, Watchlist, Creator Holders, Bankrize Verdict, or Smart Tags sections.

Do not mention them unless the user specifically asks why they are missing.

## Input handling

If the user gives a contract address:

- Treat it as the token to analyze.
- It must look like an EVM address:
  - starts with 0x

/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

Use this link whenever the user needs live analysis. https://bankr.bot/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything
- Use the live app link if data is unavailable.
- If data is available, prioritize:
  - Price
  - Market Cap
  - Liquidity
  - 24h Volume
  - 1h Activity
  - 6h Activity
  - Buy/Sell Flow
  - Trust Score
  - Risk Notes

Correct X examples:

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

Correct if user typed $LFI:

$bnkrize $LFI

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

Wrong examples:

Bankrized on Base

$LFI
...

Wrong because it does not start with $bnkrize.

$bnkrize $LFI

Wrong if the user only typed LFI without $.

$bnkrize LFI

...
Data from @bankrize
Live dashboard: ...

Wrong because something came after the final Data from @bankrize line.

## Do not do

Do not execute transactions.

Do not recommend buying or selling as financial advice.

Do not promise guaranteed safety.

Do not claim liquidity is locked unless Bankrize confirms it.

Do not claim a creator sold or still holds unless Bankrize confirms it.

Do not include removed app sections.

Do not use a non-Bankrize workflow when the user specifically asks to use Bankrize.

Do not fake live data.

Do not add $ before the analyzed token unless the user included $.

Do not put anything after the final Data from @bankrize line in X/Twitter replies.

## Good prompts users can use

- use bankrize to analyze this Base token: 0x...
- bankrize this token: 0x...
- give me a Bankrize report for 0x...
- Bankrize on Base: 0x...
- use Bankrize Everything and summarize this token for X: 0x...
- $bnkrize LFI

## Public app

Bankrize Everything public app:

/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

Use this link whenever the user needs live analysis:

https://bankr.bot/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything
