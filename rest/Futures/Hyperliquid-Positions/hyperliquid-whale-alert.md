# Futures - Hyperliquid Positions - Hyperliquid Whale Alert


```
GET /api/hyperliquid/whale-alert
```


This endpoint provides real-time whale alerts on Hyperliquid, highlighting positions with a notional value over $1 million.(Returns up to approximately 200 most recent records)

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |

<br />

<br />

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "user": "0x3fd4444154242720c0d0c61c74a240d90c127d33", // User address
      "symbol": "ETH",                                     // Symbol
      "position_size": 12700,                              // Position size (positive: long, negative: short)
      "entry_price": 1611.62,                              // Entry price
      "liq_price": 527.2521,                               // Liquidation price
      "position_value_usd": 21003260,                      // Position value (USD)
      "position_action": 2,                                // Position action type (1: open, 2: close)
      "create_time": 1745219517000                         // Entry time (timestamp in milliseconds)
    },
    {
      "user": "0x1cadadf0e884ac5527ae596a4fc1017a4ffd4e2c",
      "symbol": "BTC",
      "position_size": 33.54032,
      "entry_price": 87486.2,
      "liq_price": 44836.8126,
      "position_value_usd": 2936421.4757,
      "position_action": 2,
      "create_time": 1745219477000
    }
  ]
}

```

