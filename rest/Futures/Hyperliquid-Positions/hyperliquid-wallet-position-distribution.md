# Futures - Hyperliquid Positions - Hyperliquid Wallet Positions Distribution


```
GET /api/hyperliquid/wallet/position-distribution
```


This endpoint provides real-time Hyperliquid wallet position distribution data, grouped by position size tiers, including address counts, long/short position values, sentiment indicators, and profit/loss distribution.

**Cache / Update Frequency:** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ✅        | ✅            | ✅          |



**Response Data:**

```json
{
  "code": "0",
  "data": [
  {
    "group_name": "Shrimp", // position tier label
    // shrimp | fish | dolphin | apex_predator | small_whale | whale | tidal_whale | leviathan

    "all_address_count": 260180, // total addresses
    "position_address_count": 20966, // addresses with positions
    "position_address_percent": 8.06, // position address %

    "bias_score": 0.99, // long/short bias score

    "bias_remark": "very_bullish", // sentiment label
    // bearish | slightly_bearish | indecisive | bullish | very_bullish

    "minimum_amount": 0, // min position range
    "maximum_amount": 250, // max position range

    "long_position_usd": 6270051.698175, // long position value
    "short_position_usd": 2382603.196539, // short position value
    "long_position_usd_percent": 72.46, // long value %
    "short_position_usd_percent": 27.54, // short value %

    "position_usd": 8652654.894714, // total position value

    "profit_address_count": 6680, // profitable addresses
    "loss_address_count": 14276, // losing addresses
    "profit_address_percent": 31.88, // profit %
    "loss_address_percent": 68.12 // loss %
   }
  ]
}
```

<br />

