# ETF - Bitcoin ETF - ETF Premium/Discount History


```
GET /api/etf/bitcoin/premium-discount/history
```


This endpoint provides historical data on the premium or discount rates of Bitcoin Exchange-Traded Funds (ETFs), including Net Asset Value (NAV), market price, and premium/discount percentages for each ETF ticker.

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
      "timestamp": 1706227200000,                 // Date (timestamp in milliseconds)
      "list": [
        {
          "ticker": "GBTC",                       // ETF ticker
          "nav_usd": 37.51,                        // Net Asset Value (USD)
          "market_price_usd": 37.51,               // Market price (USD)
          "premium_discount_details": 0            // Premium/Discount percentage
        },
        {
          "ticker": "IBIT",                       // ETF ticker
          "nav_usd": 23.94,                        // Net Asset Value (USD)
          "market_price_usd": 23.99,               // Market price (USD)
          "premium_discount_details": 0.22         // Premium/Discount percentage
        },
        {
          "ticker": "FBTC",                       // ETF ticker
          "nav_usd": 36.720807,                    // Net Asset Value (USD)
          "market_price_usd": 36.75,               // Market price (USD)
          "premium_discount_details": 0.0795       // Premium/Discount percentage
        }
      ]
    }
  ]
}

```

