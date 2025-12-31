# ETF - XRP ETF - ETF Flows History


```
GET /api/etf/xrp/flow-history
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
      "timestamp": 1763078400000,
      "flow_usd": 243050000,
      "price_usd": 2.3212,
      "etf_flows": [
        {
          "etf_ticker": "XRPC",
          "flow_usd": 243050000
        },
        {
          "etf_ticker": "XRPZ"
        },
        {
          "etf_ticker": "XRP"
        },
        {
          "etf_ticker": "GXRP"
        }
      ]
    },
  ]
}

```

