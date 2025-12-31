# Futures - Long-Short Ratio - Top Position Ratio History


```
GET /api/futures/top-long-short-position-ratio/history
```


This endpoint provides historical data for the long/short position ratio of top traders.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |

&#x20;


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                                                      |
| ---------- | ------- | --------- | ---------------------------------------------------------------------------------------------------------------- |
| exchange   | string  | YES       | Futures exchange names (e.g., Binance, OKX) .Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| symbol     | string  | YES       | Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'supported-exchange-pair' API.                    |
| interval   | string  | YES       | Time interval for data aggregation.  Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w         |
| limit      | integer | NO        | Number of results per request.  Default: 1000, Maximum: 1000                                                     |
| start_time | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                           |
| end_time   | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                             |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1741615200000, // Timestamp (in milliseconds)
      "top_position_long_percent": 64.99, // Long position percentage of top positions (%)
      "top_position_short_percent": 35.01, // Short position percentage of top positions (%)
      "top_position_long_short_ratio": 1.86 // Long/Short ratio of top positions
    },
    {
      "time": 1741618800000, // Timestamp (in milliseconds)
      "top_position_long_percent": 64.99, // Long position percentage of top positions (%)
      "top_position_short_percent": 35.01, // Short position percentage of top positions (%)
      "top_position_long_short_ratio": 1.86 // Long/Short ratio of top positions
    }
  ]
}

```

