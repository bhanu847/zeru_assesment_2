## Feature Selection Rationale

We selected **three key features** that best represent a wallet’s financial behavior and risk:

1. **Total Value in USD**  
   - Reflects the **financial strength** of the wallet.  
   - Larger portfolios tend to be **more resilient** but also introduce **complexity risk**.

2. **Protocol Count**  
   - Measures **diversification** across DeFi protocols.  
   - **Over-diversification** increases operational risk, while **low diversification** increases dependency risk.

3. **Recent Activity Score**  
   - Captures how **active or dormant** a wallet is.  
   - **Dormant wallets** may pose **reactivation/liquidity risks**, while **hyperactive wallets** may indicate **speculative behavior**.

These features are **interpretable, easy to scale, and collectively provide a balanced view** of a wallet’s risk profile.
