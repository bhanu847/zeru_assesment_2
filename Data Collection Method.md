## Data Collection Method

We use the **Covalent API** to fetch **wallet-level on-chain data**.

For each wallet, we retrieve:  
- **Token balances in USD** (to measure portfolio size)  
- **Token and protocol metadata** (to calculate diversification)  
- **Last activity timestamps** (to assess recent engagement)  

The API aggregates data from the **entire Ethereum blockchain**, so we don’t have to query individual protocols.  

The results are **structured JSON responses**, which are then converted into a **pandas DataFrame** for further processing and normalization.  

This approach is **scalable** because:  
- **One API call** can handle many wallets efficiently.  
- It provides a **complete portfolio view**, not limited to a single DeFi protocol like Compound or Aave.  

