# FAQ

**What is Bankrize Everything?**
A read-only Bankr skill and app that analyzes tokens on Base. Give it a ticker or contract address and it returns a clean report: price, liquidity, volume, buy/sell flow, a trust score, risk indicators, links, and top pools.

**Does it trade for me?**
No. Bankrize is read-only. It never swaps, buys, sells, transfers, approves, claims, mints, deploys, bets, or signs anything.

**Which chains does it support?**
Base only. It does not analyze tokens on other chains.

**What is the Trust Score?**
A 0–100 heuristic summarizing how risky a token looks. See [TRUST_SCORE.md](./TRUST_SCORE.md) for the bands and what feeds it.

**Is a high Trust Score a guarantee the token is safe?**
No. It's a heuristic, not financial advice. A high score does not mean liquidity is locked or that the token is safe. Always do your own research.

**Why does the data update on its own?**
The app auto-refreshes the active token roughly every 30 seconds so the report stays current.

**Where does the data come from?**
The Bankrize workflow. Nothing is faked or guessed — if a field can't be confirmed, it isn't claimed.

**How do I use it?**
In chat: "bankrize this token: 0x...". In the app: paste a ticker or Base contract address and hit Bankrize. See [USAGE.md](./USAGE.md) for more examples.

**Who made it?**
Built by 0xthefear. Data and workflow: @bankrize.
