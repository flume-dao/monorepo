<div align="center">
  <img border-radius="25px" max-height="250px" src="./banner.png" />
  <h1>Flume for Uniswap V3/V4</h1>
  <p>
    <a href="https://opensource.org/licenses/MIT"><img alt="License" src="https://img.shields.io/github/license/flume-dao/contracts?color=3AB2FF" /></a>
    <a href="https://flume.fi"><img alt="App" src="https://img.shields.io/badge/Launch App-F9C3B3" /></a>
  </p>
</div>

## Introduction

Flume is a data-driven automated liquidity manager (ALM) for concentrated liquidity DEXs like Uniswap v3 and its forks (eg. Algebra).
Built on its competitors flaws, Flume addresses critical inefficiencies in existing ALMs, to maximize liquidity providers net profits and ensure liquidity pools capital efficiency.
By only providing a single vault/strategy by pair, Flume is trivial to use, and a reliable LP solution for both retail and institutionals.   

We identified as major loss factors:
- flawed rebalancing mechanisms
- lack of market awareness and forecasting
- high swap slippage and market impact
- hidden costs 

---

## The Problem with Existing CLMs

Concentrated Liquidity Managers (CLMs) have theoretically simplified the concentrated liquidity landscape by enabling LPs to maintain yields through targeted price ranges. However, most existing solutions face serious challenges:

| **Competitor Flaws** | **Impact** |
|-----------------------|------------|
| Excessive Rebalancing | High impermanent loss for LPs due to market impact and swap fees. |
| Inefficient Triggers | Poorly timed rebalances increase slippage and reduce profitability. |
| Deterministic Rebalancing | Predictable swaps invite arbitrageurs, further reducing LP returns. |
| Poor Volatility and Momentum Analysis | Reactivity (if any) to market movements instead of proactive positioning. |
| Absence of Forecasting | Strategies fail to adapt to evolving market conditions. |

These flaws result in **major inefficient capital allocation**, **high costs**, and **missed profits**.

---

## Why Flume?

Flume eliminates inefficiencies by combining **accurate price action analysis**, **smarter rebalancing** and **liqudity aggregation**, to achieve unparalleled liquidity management.

### Key Features

1. **Accurate Range Forecasting**  
   - Uses real-time **volatility** and **momentum** analysis for precise range predictions.
   - Ensures liquidity stays centered around the current price.

2. **Confidence-Based Rebalance Triggers**  
   - Rebalances are based on position divergence vs optimal, not just on static range breakout.
   - Reduces the impact of impermanent loss by maximizing capital utilization.

3. **Aggregated Liquidity Rebalancing**  
   - Leverages external liquidity sources (e.g., 1inch, 0x, CoW Protocol) to minimize swap loss vs arbitrage and optimize execution.

4. **Universal Strategy**  
   - A single strategy for all pools, catering to both stable pairs and highly volatile assets, simplifying the user experience.
   - No more confusing narrow, wide, upside or downside (left/right) strategies for LPs, these are now unified.

5. **Multi-Position Vaults**  
   - Supports non-linear liquidity distributions across the range (e.g., normal or asymmetric) for maximum capital efficiency.  

6. **Lean and Secure Codebase**  
   - Built on an **Arrakis V2 fork**, chosen with auditors for its **code quality**, **security model** vs 7 competitors.

7. **MEV Resistance**  
   - Dynamic transaction triggers, **mempool avoidance** and **sequencer priority fees** protect Flume against MEV. 

### Comparison with Other CLMs

| Criteria                | Flume | Gamma | Arrakis V2 | Arrakis V3 | Beefy CLM | Maverick | DeFiEdge | Ichi/CupcakeHop/Bril |
|-------------------------|-------|-------|------------|------------|-----------|----------|----------|----------------------|
| **Aggregated Swaps**    | ✔️   | -     | -          | ✔️        | -         | ❌       | ✔️      | ❌                  |
| **Low Complexity**      | ✔️   | ✔️   | ✔️        | ❌         | ❌        | ❌       | ❌       | ✔️                 |
| **Multi-position**      | ✔️   | ❌    | ✔️        | ✔️        | ✔️       | ✔️      | ✔️      | ❌                  |
| **Uniswap Compatible**  | ✔️   | ✔️   | ✔️        | ✔️ (V4) | ✔️      | ❌       | ✔️      | ✔️                 |
| **Multi-DEX**           | ✔️   | ✔️   | ✔️        | ❌         | ✔️       | ❌       | ✔️      | ❌                  |
| **Volatility Aware**    | ✔️   | ❌    | ✔️        | ✔️        | ✔️       | ❌       | ❌       | ❌                  |
| **MEV Resistant**       | ✔️   | ❌    | -          | ✔️        | ❌        | ❌       | ✔️      | ❌                  |
| **AAA Audited**         | ✔️   | ✔️   | ✔️        | ✔️        | ✔️       | ✔️      | ✔️      | ❌                  |

---
