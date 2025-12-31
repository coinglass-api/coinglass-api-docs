# ETF - Solana ETF - ETF Flows History


```
GET /api/etf/solana/flow-history
```


This endpoint provides a list of key status information regarding the history of ETF flows.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |



**Response Data:**

```json
{
  "code": "0",
  "data": [
    {
      "timestamp": 1762473600000,
      "flow_usd": 12700000,
      "price_usd": 155.2,
      "etf_flows": [
        {
          "etf_ticker": "BSOL",
          "flow_usd": 11700000
        },
        {
          "etf_ticker": "VSOL"
        },
        {
          "etf_ticker": "FSOL"
        },
        {
          "etf_ticker": "TSOL"
        },
        {
          "etf_ticker": "GSOL",
          "flow_usd": 1000000
        }
      ]
    },
  ]
}

```

