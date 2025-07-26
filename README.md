Wallet Risk Scoring Project::::::::::::

Project Overview:--------------------
This project calculates a risk score (0–1000) for blockchain wallets to evaluate their potential financial risk. It uses on-chain data to analyze wallet behavior, portfolio diversity, and recent activity patterns.

The scoring model is designed for:

Risk assessment in DeFi lending

Portfolio monitoring for institutional users

Fraud or anomaly detection in blockchain analytics

How the Risk Score Works
Each wallet is scored based on three main factors:

Portfolio Size (50%)

Total USD value of the wallet’s tokens

Larger portfolios generally indicate better resilience but also higher complexity

Protocol Diversification (30%)

Number of unique DeFi protocols the wallet interacts with

Over-diversification increases operational risk, while low diversification increases dependency risk

Recent On-chain Activity (20%)

Frequency and recency of transactions

Dormant wallets may have reactivation/liquidity risk; overly active wallets may be speculative

These features are scaled between 0 and 1 and then combined with weights to produce a score between 0 (high risk) and 1000 (low risk).

Why Covalent API was Used
We chose Covalent API because it provides a complete wallet-level snapshot in a single request:

✅ Aggregates all token balances & protocol interactions
✅ Covers inactive wallets (unlike protocol-specific APIs)
✅ Scales easily for large wallet lists
✅ Reduces complexity vs. querying multiple subgraphs (Compound V2, V3, Aave, etc.)

Why Not Compound V2/V3 Subgraphs?
They only provide protocol-specific lending/borrowing data

Would miss wallets that don’t interact with Compound

Requires separate queries for V2 & V3, increasing complexity and API calls

Not suitable for a holistic risk model covering the entire portfolio
