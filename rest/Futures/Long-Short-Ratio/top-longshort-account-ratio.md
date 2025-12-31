# Futures - Long-Short Ratio - Top Account Ratio History


```
GET /api/futures/top-long-short-account-ratio/history
```


This endpoint provides historical data for the long/short account ratio of top traders.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |


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
      "top_account_long_percent": 73.3, // Long position percentage of top accounts (%)
      "top_account_short_percent": 26.7, // Short position percentage of top accounts (%)
      "top_account_long_short_ratio": 2.75 // Long/Short ratio of top accounts
    },
    {
      "time": 1741618800000, // Timestamp (in milliseconds)
      "top_account_long_percent": 74.18, // Long position percentage of top accounts (%)
      "top_account_short_percent": 25.82, // Short position percentage of top accounts (%)
      "top_account_long_short_ratio": 2.87 // Long/Short ratio of top accounts
    }
  ]
}

```

