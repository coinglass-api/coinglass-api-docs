# ETF - Bitcoin ETF - ETF History


```
GET /api/etf/bitcoin/history
```


This endpoint provides historical data for Bitcoin Exchange-Traded Funds (ETFs), including key information such as market price, Net Asset Value (NAV), premium/discount percentage, shares outstanding, and net assets for each ETF ticker.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description                           |
| ------ | ------ | --------- | ------------------------------------- |
| ticker | string | YES       | ETF ticker symbol (e.g., GBTC, IBIT). |


**Response Data:**

```json
{
  "code": "0",                                
  "msg": "success",                          
  "data": [
    {
      "assets_date": 1706486400000,           // Net asset date (timestamp in milliseconds)
      "btc_holdings": 496573.8166,            // BTC holdings
      "market_date": 1706486400000,           // Market price date (timestamp in milliseconds)
      "market_price": 38.51,                  // Market price (USD)
      "name": "Grayscale Bitcoin Trust",      // ETF name
      "nav": 38.57,                           // Net Asset Value per share (USD)
      "net_assets": 21431132778.35,           // Total net assets (USD)
      "premium_discount": -0.16,              // Premium/discount percentage
      "shares_outstanding": 555700100,        // Total shares outstanding
      "ticker": "GBTC"                        // ETF ticker
    }
  ]
}

```

