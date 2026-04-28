<div align="center">
  <h1>Pumpr</h1>
  <p><strong>PumpFun for Perps. Launch a perp market on anything in 30 seconds.</strong></p>

  <p>
    <a href="https://pumpr.tech"><img src="https://img.shields.io/badge/Website-pumpr.tech-blue" alt="Website" /></a>
    <a href="https://twitter.com/PumprOnSol"><img src="https://img.shields.io/badge/Twitter-@PumprOnSol-1DA1F2?logo=twitter&logoColor=white" alt="Twitter" /></a>
    <a href="https://t.me/PumprOnSolana"><img src="https://img.shields.io/badge/Telegram-Community-2CA5E0?logo=telegram&logoColor=white" alt="Telegram" /></a>
  </p>
</div>

## What is Pumpr?

Pumpr is a permissionless perpetual launchpad on Solana. Anyone can deploy a perp market on any asset in 30 seconds. The creator earns 0.5% volume forever. Long memes. Short KOLs. Trade outcomes. The first perp DEX where listings are driven by a bonding curve.

## Core Mechanics

| Feature                     | Description                                                                   |
| --------------------------- | ----------------------------------------------------------------------------- |
| **Permissionless Listings** | Deploy isolated perp markets instantly.                                       |
| **Three Oracle Types**      | Pyth (blue-chips), TWAP (on-chain tokens), Bonding-curve (illiquid/creators). |
| **Creator Economics**       | Creator earns 50 bps of all volume forever via a transferable NFT.            |
| **Leverage**                | Trade with up to 50x leverage (25x at launch).                                |

## Token Tiers ($PUMPR)

| Tier       | Requirement | Benefits                                                                    |
| ---------- | ----------- | --------------------------------------------------------------------------- |
| **Tier 0** | 0 $PUMPR    | Trade any market, full launch fee (0.5 SOL).                                |
| **Tier 1** | 1M $PUMPR   | -10% trading fee, -10% listing fee, creator leaderboard eligible.           |
| **Tier 2** | 5M $PUMPR   | -25% trading fee, -50% listing fee, +20% LP yield boost, governance voting. |
| **Tier 3** | 10M $PUMPR  | -40% trading fee, -75% listing fee, +50% LP yield boost, 50x leverage.      |

## How It Works

```ascii
+-------------------+        +--------------------+        +-------------------+
| 1. Creator Picks  | -----> | 2. Chooses Oracle  | -----> | 3. Sets Params    |
|    Asset (Token,  |        |    (Pyth, TWAP, or |        |    (Leverage,     |
|    KOL, Agent)    |        |    Bonding-curve)  |        |    Margin)        |
+-------------------+        +--------------------+        +-------------------+
                                                                    |
                                                                    v
+-------------------+        +--------------------+        +-------------------+
| 6. Traders Open   | <----- | 5. Market Live     | <----- | 4. Pays Listing   |
|    Long/Short     |        |    (Creator Gets   |        |    Fee (SOL or    |
|    Positions      |        |    Market NFT)     |        |    $PUMPR)        |
+-------------------+        +--------------------+        +-------------------+
```

## Architecture

```ascii
+-------------------------------------------------------------+
|                      CLIENT LAYER                           |
|  [ Next.js Web App ]   [ Telegram Bot ]   [ TradingView ]   |
+-------------------------------------------------------------+
                              |
+-------------------------------------------------------------+
|                       EDGE / API                            |
|        [ Next.js Routes ]         [ Hono on Bun ]           |
+-------------------------------------------------------------+
         |                    |                   |
+-----------------+   +-----------------+   +-----------------+
| Database Cache  |   |   Solana RPC    |   |   Pyth Oracle   |
+-----------------+   +-----------------+   +-----------------+
         |                    |                   |
+-------------------------------------------------------------+
|                  SOLANA ANCHOR PROGRAM                      |
|                                                             |
|  [ Market PDA ]   [ Position PDA ]   [ LP Vault PDA ]       |
|  [ Insurance ]    [ Creator NFT ]    [ Liquidation Eng ]    |
+-------------------------------------------------------------+
```

## Tech Stack

| Layer           | Technology                                |
| --------------- | ----------------------------------------- |
| **Frontend**    | Next.js, React                            |
| **Backend API** | Hono (Bun), Next.js API Routes            |
| **Database**    | PostgreSQL                                |
| **Blockchain**  | Solana (Anchor Framework)                 |
| **Oracles**     | Pyth, On-chain TWAP, Custom Bonding-curve |

## Roadmap

- **Phase 1 (MVP):** Working perp engine, Pyth+TWAP oracles, 10 whitelisted markets, LP vault.
- **Phase 2 (Growth):** Permissionless launch, Bonding-curve oracle, Telegram Mini App.
- **Phase 3 (Scale):** Multi-collateral, Cross-margin, Auction-based liquidation, Mobile PWA.
- **Phase 4 (Ecosystem):** SDK, White-label solutions, Cross-chain, CLAMM.

## Reference Links

| Resource        | Link                                          |
| --------------- | --------------------------------------------- |
| **Website**     | [pumpr.tech](https://pumpr.tech)              |
| **App**         | [app.pumpr.tech](https://app.pumpr.tech)      |
| **Docs**        | [pumpr.tech/docs](https://pumpr.tech/docs)    |
| **X / Twitter** | [@PumprOnSol](https://twitter.com/PumprOnSol) |

<br>
<br>

<div align="center">
  <sub>Pumpr is experimental DeFi infrastructure. Trading perpetual markets involves substantial risk of loss including total liquidation of margin collateral. Use at your own risk.</sub>
</div>
