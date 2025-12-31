# ETF - Bitcoin ETF - ETF Price History


```
GET /api/etf/bitcoin/price/history
```


This endpoint provides historical price data for Bitcoin Exchange-Traded Funds (ETFs), including open, high, low, and close (OHLC) prices, along with trading volume for each data point.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description                                |
| ------ | ------ | --------- | ------------------------------------------ |
| ticker | string | YES       | ETF ticker symbol (e.g., GBTC, IBIT).      |
| range  | string | YES       | Time range for the data (e.g., 1d,7d,all). |


**Response Data:**

```json
{
  "code": "0",
  "message": "success",
  "data": [
    {
      "time": 1731056460000,   // timestamp in milliseconds
      "open": 60.47,                // Opening price
      "high": 60.47,                // Highest price
      "low": 60.47,                 // Lowest price
      "close": 60.47,               // Closing price
      "volume": 100                // Trading volume
    },
    ...
  ]
}

```

