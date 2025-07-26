## Scoring Method

1. Each selected feature is **normalized to a 0–1 scale** using Min-Max scaling.  
2. A **weighted sum** combines the features to compute the risk score:

```python
risk_df["risk_score"] = (
    0.5 * risk_df["total_value_usd_scaled"] +
    0.3 * risk_df["protocol_count_scaled"] +
    0.2 * risk_df["activity_score_scaled"]
) * 1000



