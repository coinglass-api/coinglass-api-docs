# ETF - Ethereum ETF - ETF Flows History


```
GET /api/etf/ethereum/flow-history
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
      "timestamp": 1721692800000,
      "flow_usd": 106600000,
      "price_usd": 3438.09,
      "etf_flows": [
        {
          "etf_ticker": "ETHA",
          "flow_usd": 266500000
        },
        {
          "etf_ticker": "FETH",
          "flow_usd": 71300000
        },
      ]
    }
  ]
}

```

