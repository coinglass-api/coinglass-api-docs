# Futures - Funding Rate - Exchange List


```
GET /api/futures/funding-rate/exchange-list
```


This endpoint provides funding rate data from exchanges.

***Cache / Update Frequency:*** 20 second for all the API plans.

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
      "symbol": "BTC", // Symbol
      "stablecoin_margin_list": [ // USDT/USD margin mode
        {
          "exchange": "Binance", // Exchange
          "funding_rate_interval": 8, // Funding rate interval (hours)
          "funding_rate": 0.007343, // Current funding rate
          "next_funding_time": 1745222400000 // Next funding time (milliseconds)
        },
        {
          "exchange": "OKX", // Exchange
          "funding_rate_interval": 8, // Funding rate interval (hours)
          "funding_rate": 0.00736901950628, // Current funding rate
          "next_funding_time": 1745222400000 // Next funding time (milliseconds)
        }
      ],
      "token_margin_list": [ // Coin-margined mode
        {
          "exchange": "Binance", // Exchange
          "funding_rate_interval": 8, // Funding rate interval (hours)
          "funding_rate": -0.001829, // Current funding rate
          "next_funding_time": 1745222400000 // Next funding time (milliseconds)
        }
      ]
    }
  ]
}

```

