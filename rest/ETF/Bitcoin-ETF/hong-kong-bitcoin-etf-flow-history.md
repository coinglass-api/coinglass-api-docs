# ETF - Bitcoin ETF - Hong Kong ETF Flows History


```
GET /api/hk-etf/bitcoin/flow-history
```


This endpoint provides historical data on ETF flow activity for Bitcoin ETFs in the Hong Kong market.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |



**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "timestamp": 1714435200000,                     // Date (timestamp in milliseconds)
      "flow_usd": 247866000,                          // Total capital inflow (USD)
      "price_usd": 63842.4,                           // BTC price on that date (USD)
      "etf_flows": [                                  // ETF capital flow details
        {
          "etf_ticker": "CHINAAMC",                   // ETF ticker
          "flow_usd": 123610690                       // Capital inflow for this ETF (USD)
        },
        {
          "etf_ticker": "HARVEST",                    // ETF ticker
          "flow_usd": 63138000                        // Capital inflow for this ETF (USD)
        },
        {
          "etf_ticker": "BOSERA&HASHKEY",             // ETF ticker
          "flow_usd": 61117310                        // Capital inflow for this ETF (USD)
        }
      ]
    }
  ]
}

```

