# Futures - Funding Rate - Cumulative Exchange List


```
GET /api/futures/funding-rate/accumulated-exchange-list
```


This endpoint provides cumulative funding rate data from exchanges.

***Cache / Update Frequency:*** 1 hour for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name  | Type   | Mandatory | Description                                       |
| ----- | ------ | --------- | ------------------------------------------------- |
| range | string | YES       | Time range for the data (e.g.,1d, 7d, 30d, 365d). |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "symbol": "BTC", // Symbol
      "stablecoin_margin_list": [ // Accumulated funding rate for USDT/USD margin mode
        {
          "exchange": "BINANCE", // Exchange name
          "funding_rate": 0.001873 // Accumulated funding rate
        },
        {
          "exchange": "OKX", // Exchange name
          "funding_rate": 0.00775484 // Accumulated funding rate
        }
      ],

      "token_margin_list": [ // Accumulated funding rate for coin-margined mode
        {
          "exchange": "BINANCE", // Exchange name
          "funding_rate": -0.003149 // Accumulated funding rate
        }
      ]
    }
  ]
}

```

