# ETF - Bitcoin ETF - ETF NetAssets History


```
GET /api/etf/bitcoin/net-assets/history
```


This endpoint provides historical data on the net assets of Bitcoin Exchange-Traded Funds (ETFs).

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description                           |
| ------ | ------ | --------- | ------------------------------------- |
| ticker | string | NO        | ETF ticker symbol (e.g., GBTC, IBIT). |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "net_assets_usd": 51671409241.39,         // Net asset value (USD)
      "change_usd": 655300000,                  // Daily capital change (USD)
      "timestamp": 1704931200000,               // Date (timestamp in milliseconds)
      "price_usd": 46337.8                      // BTC price on that date (USD)
    },
    {
      "net_assets_usd": 51874409241.39,         // Net asset value (USD)
      "change_usd": 203000000,                  // Daily capital change (USD)
      "timestamp": 1705017600000,               // Date (timestamp in milliseconds)
      "price_usd": 42788.9                      // BTC price on that date (USD)
    }
  ]
}

```

