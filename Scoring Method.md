Scoring Method:-----

1. Each selected feature is normalized to a 0–1 scale using Min-Max scaling.
2. A weighted sum combines the features to compute the risk score:

  risk_df["risk_score"] = (
    0.5 * risk_df["total_value_usd_scaled"] +
    0.3 * risk_df["protocol_count_scaled"] +
    0.2 * risk_df["activity_score_scaled"]
) * 1000

3. 50% weight → Total Value (most important for financial resilience)
4. 30% weight → Protocol Count (diversification risk)
5.  20% weight → Activity Score (behavioral risk)
  Finally, the score is scaled between 0 and 1000, where:
   0 → very high risk
   1000 → very low risk

This method is simple, interpretable, and easy to extend with more features in the future.

