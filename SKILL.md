name: bankrize-everything
description: Use Bankrize Everything to analyze Base tokens with live activity, trust score, liquidity, risk indicators, and clean share-ready reports.
version: 1.0.0
author: 0xc027ecbd0fa38f667a25550aae56b14c73931d5a
tags:
  - bankrize
  - base
  - token-analysis
  - crypto
  - onchain
  - bankr
---

# Bankrize Everything Skill

Bankrize Everything is a Bankr workflow for analyzing Base tokens using the public Bankrize Everything app.

Canonical app:
/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

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

## Scope

This skill is Base-only.

Only analyze tokens on Base.

Do not perform swaps, buys, sells, transfers, claims, approvals, mints, deployments, bets, automations, or signatures.

This skill is read-only.

This skill must only use the Bankrize Everything workflow and app output as the source of the analysis.

Do not replace Bankrize with another token-analysis workflow.

Do not present data as Bankrize data unless it comes from the Bankrize Everything app/workflow or the user provides a Bankrize result.

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
- 5-minute activity
- 1-hour activity
- buy vs sell flow
- average trade size
- largest recent trade
- real-time or near real-time transaction feed
- volume spikes
- unusual activity
- trust score
- risk indicators
- official website if available
- social links if available
- top pools if available

## Important removed sections

Do not include these sections:

- Base Discovery
- Watchlist
- Creator holders

The current Bankrize Everything app intentionally does not include Base Discovery, Watchlist, or Creator Holders sections.

Do not mention them unless the user specifically asks why they are missing.

## Input handling

If the user gives a contract address:

- Treat it as the token to analyze.
- It must look like an EVM address:
  - starts with 0x
  - 42 characters long
- Assume Base unless the user says another chain.
- If another chain is requested, explain that Bankrize Everything is currently Base-only.

If the user gives only a ticker:

- Explain that tickers can be ambiguous.
- Ask for the Base contract address for the most accurate Bankrize analysis.
- If a Bankrize search result is available from the app/workflow, use the best Base match and clearly say it is a matched result.

If the user gives no token:

- Ask for the Base token contract address or ticker.

## Source rules

Use Bankrize Everything as the canonical source.

Canonical app:
/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

If live Bankrize data is available in the environment:

- Use it.
- Summarize it in the Bankrize report format below.

If live Bankrize data is not available in the environment:

- Do not invent values.
- Give the app link.
- Tell the user to open the app and enter the token.
- If the user pastes the Bankrize output back, summarize it cleanly.

Never fake:

- trade counts
- volume
- liquidity
- market cap
- trust score
- risk indicators
- largest trade
- transaction feed
- buy/sell flow

Unknown is better than fake.

## Required response style

Use concise crypto-native language.

Prioritize numbers.

Avoid fluff.

Use clear labels. For X/Twitter replies, keep the response compact and shareable.

When possible, format the output like this:

Bankrized on Base

Token:
Contract:
Price:
Market Cap:
Liquidity:
5m Activity:
1h Activity:
Buy/Sell Flow:
Avg Trade Size:
Largest Recent Trade:
Trust Score:
Risk Notes:

Live dashboard:
/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

## Detailed report format

When the user wants a fuller report, use this structure:

Bankrize Everything Report

Token
- Name:
- Ticker:
- Contract:
- Base-only:

Market
- Price:
- Market cap:
- Liquidity:
- 24h volume:
- Token age:

Live Activity
- Last 5 minutes:
- Last 1 hour:
- Buy vs sell:
- Average trade size:
- Largest recent trade:
- Recent transaction feed:
- Volume spike detection:
- Unusual activity:

Trust Score
- Score:
- Label:
- Main reasons:

Risk Indicators
- Liquidity risk:
- Activity risk:
- Sell pressure:
- Missing socials/website:
- Other notes:

Links
- Website:
- Socials:
- Live dashboard:

## Trust score labels

Use these labels if a Bankrize score is available:

- 80–100: strong
- 60–79: moderate
- 40–59: caution
- 0–39: high risk

Do not calculate a new trust score unless the Bankrize workflow/app provides the needed values.

If no score is available, say:

“Trust Score: unavailable from current Bankrize output.”

## X/Twitter behavior

If responding to a tweet or preparing a tweet, use a short format.

Example:

Bankrized on Base

$TOKEN
5m: 1 trade — $1,000 volume
1h: 50 trades — $40,000 volume
Flow: 32 buys / 18 sells
Liquidity: $...
Trust Score: ../100
Risk: ...

Live:
/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

If exact live data is unavailable, use:

Bankrize can analyze this live here:

/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

Paste the Base token contract into the app for the live 5m/1h activity, volume, buy/sell flow, trust score, and risk readout.

## Do not do

Do not execute transactions.

Do not recommend buying or selling as financial advice.

Do not promise guaranteed safety.

Do not claim liquidity is locked unless Bankrize confirms it.

Do not claim a creator sold or still holds unless Bankrize confirms it.

Do not include removed app sections.

Do not use a non-Bankrize workflow when the user specifically asks to use Bankrize.

## Good prompts users can use

- use bankrize to analyze this Base token: 0x...
- bankrize this token: 0x...
- give me a Bankrize report for 0x...
- Bankrize on Base: 0x...
- use Bankrize Everything and summarize this token for X: 0x...

## Public app

Bankrize Everything public app:

/u/0xc027ecbd0fa38f667a25550aae56b14c73931d5a/apps/bankrize-everything

Use this link whenever the user needs live analysis.
