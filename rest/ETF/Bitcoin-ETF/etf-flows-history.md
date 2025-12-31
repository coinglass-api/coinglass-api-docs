# ETF - Bitcoin ETF - ETF Flows History


```
GET /api/etf/bitcoin/flow-history
```


This endpoint provides historical flow data for Bitcoin Exchange-Traded Funds (ETFs), including daily net inflows and outflows in USD, closing prices, and flow breakdowns by individual ETF tickers.

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
      "timestamp": 1704931200000,                   // Date (timestamp in milliseconds)
      "flow_usd": 655300000,                         // Total daily capital flow (USD)
      "price_usd": 46663,                            // BTC current price (USD)
      "etf_flows": [                                 // ETF capital flow breakdown
        {
          "etf_ticker": "GBTC",                      // ETF ticker
          "flow_usd": -95100000                      // Capital outflow (USD)
        },
        {
          "etf_ticker": "IBIT",                      // ETF ticker
          "flow_usd": 111700000                      // Capital inflow (USD)
        },
        {
          "etf_ticker": "FBTC",                      // ETF ticker
          "flow_usd": 227000000                      // Capital inflow (USD)
        }
      ]
    }
  ]
}

```

