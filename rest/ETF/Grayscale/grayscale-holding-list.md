# ETF - Grayscale - Holdings List


```
GET /api/grayscale/holdings-list
```


This endpoint provides a list of holdings managed by Grayscale Investments.

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
      "symbol": "ETH",                                  // Token symbol, 
      "primary_market_price": 29.89,                    // Price in the primary market 
      "secondary_market_price": 29.71,                  // Price in the secondary market 
      "premium_rate": -0.6,                             // Premium rate (%),
      "holdings_amount": 2630007.61026,                 // Current holding amount (in tokens)
      "holdings_usd": 4290752215.8347797,               // Total market value of holdings in USD
      "holdings_amount_change_30d": 0,                  // Change in holding amount over the past 30 days (in tokens)
      "holdings_amount_change_7d": 0,                   // Change in holding amount over the past 7 days (in tokens)
      "holdings_amount_change1d": 0,                    // Change in holding amount over the past 1 day (in tokens)
      "close_time": 1721422800000,                      // Market close timestamp (milliseconds)
      "update_time": 1745203812007                      // Data update timestamp (milliseconds)
    },
    {
      "symbol": "ETC",                                  // Token symbol, e.g., ETC = Ethereum Classic
      "primary_market_price": 11.99,                    // Price in the primary market
      "secondary_market_price": 6.63,                   // Price in the secondary market
      "premium_rate": -44.7,                            // Premium rate, currently at a significant discount
      "holdings_amount": 11181376.733556,               // Current holding amount (in tokens)
      "holdings_usd": 181440200.2554132,                // Total market value of holdings in USD
      "holdings_amount_change_30d": -20697.669828,      // Change in holding amount over the past 30 days
      "holdings_amount_change_7d": -4596.123672,        // Change in holding amount over the past 7 days
      "holdings_amount_change1d": 0,                    // Change in holding amount over the past 1 day
      "close_time": 1744923600000,                      // Market close timestamp
      "update_time": 1745203812168                      // Data update timestamp
    }
  ]
}

```

