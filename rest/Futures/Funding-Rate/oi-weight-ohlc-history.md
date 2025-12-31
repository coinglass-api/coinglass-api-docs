# Futures - Funding Rate - OI Weight History (OHLC)


```
GET /api/futures/funding-rate/oi-weight-history
```


This endpoint provides open interest-weighted funding rate data in OHLC (open, high, low, close) candlestick format for futures cryptocurrencies.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |

&#x20;


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                                             |
| ---------- | ------- | --------- | ------------------------------------------------------------------------------------------------------- |
| symbol     | string  | YES       | Trading coin (e.g., BTC). Retrieve supported coins via the 'supported-coins' API.                       |
| interval   | string  | YES       | Time interval for data aggregation. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w |
| limit      | integer | NO        | Number of results per request. Default: 1000, Maximum: 1000                                             |
| start_time | integer | NO        | Start timestamp in seconds (e.g., 1641522717000).                                                       |
| end_time   | integer | NO        | End timestamp in seconds (e.g., 1641522717000).                                                         |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1658880000000, // Timestamp (milliseconds)
      "open": "0.004603",     // Opening funding rate
      "high": "0.009388",     // Highest funding rate
      "low": "-0.005063",     // Lowest funding rate
      "close": "0.009229"     // Closing funding rate
    },
    {
      "time": 1658966400000, // Timestamp (milliseconds)
      "open": "0.009229",     // Opening funding rate
      "high": "0.01",         // Highest funding rate
      "low": "0.007794",      // Lowest funding rate
      "close": "0.01"         // Closing funding rate
    }
  ]
}
```

