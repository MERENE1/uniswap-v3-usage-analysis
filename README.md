
# Uniswap v3 — Usage & Activity Analysis

This project analyzes on-chain usage of **Uniswap v3 on Ethereum**, focusing on protocol activity rather than revenue.

The goal is to understand how consistently the protocol is used over time, using transparent on-chain data.

---

## 📊 Key Metrics
- **Trading Volume (USD)** — proxy for protocol usage
- **Active Wallets** — number of unique addresses interacting daily

---

## 🔍 Key Insights
- Trading volume is highly volatile and closely follows market conditions.
- Active wallets are significantly more stable than volume.
- Periods of declining volume do not necessarily coincide with drops in user activity.

This suggests that Uniswap v3 usage is **stickier than volume alone would imply**.

---

## 🧠 Methodology
- Data source: `dex.trades` (Dune Analytics)
- Scope: Uniswap v3 on Ethereum mainnet
- Time aggregation: daily
- Filters:
  - Successful trades only
  - Trades with non-zero USD value

**Note:** Wallets represent addresses, not unique users.


#dashboard
https://dune.com/akp_m/uniswap-v3-protocol-health?utm_source=share&utm_medium=copy&utm_campaign=dashboard

---

## 🧾 SQL
The core query aggregates daily protocol usage metrics:

```sql
-- see sql/uniswap_v3_daily_metrics.sql

#------------------------------------------------------------------------------------------------------------
