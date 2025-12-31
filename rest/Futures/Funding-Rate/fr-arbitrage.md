# Futures - Funding Rate - Arbitrage


```
GET /api/futures/funding-rate/arbitrage
```


This endpoint provides funding rate arbitrage data across exchanges for futures cryptocurrencies.

***Cache / Update Frequency:*** 20 second for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name          | Type    | Mandatory | Description                                                               |
| ------------- | ------- | --------- | ------------------------------------------------------------------------- |
| usd           | integer | YES       | Investment principal for arbitrage (e.g., 10000).                         |
| exchange_list | string  | NO        | List of exchange names to retrieve data from (e.g.,  'Binance,OKX,Bybit') |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "symbol": "SUPRA", // Token symbol
      "buy": { //  (lower funding rate)
        "exchange": "MEXC", // Exchange name
        "open_interest_usd": 848218.2833, // Open interest in USD on the exchange
        "funding_rate_interval": 4, // Funding rate interval (hours)
        "funding_rate": -0.994 // Current funding rate (%)
      },
      "sell": { //  (higher funding rate)
        "exchange": "Gate.io", // Exchange name
        "open_interest_usd": 448263.5072, // Open interest in USD on the exchange
        "funding_rate_interval": 4, // Funding rate interval (hours)
        "funding_rate": 0.005 // Current funding rate (%)
      },
      "apr": 2187.81, // Annual Percentage Rate (APR, %)
      "funding": 0.999, // Funding rate difference (between long and short)
      "fee": 0.03, // Total trading fee (both sides)
      "spread": -0.09, // Price spread between platforms (%)
      "next_funding_time": 1745222400000 // Next funding settlement time (timestamp in milliseconds)
    }
  ]
}

```

