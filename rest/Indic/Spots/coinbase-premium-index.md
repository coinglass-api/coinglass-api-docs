# Indic - Spots - Coinbase Premium Index


```
GET /api/coinbase-premium-index
```


This endpoint provides the Coinbase Bitcoin Premium Index, which indicates the price difference between Bitcoin on Coinbase Pro and Binance.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |

<br />


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                                          |
| ---------- | ------- | --------- | ---------------------------------------------------------------------------------------------------- |
| interval   | string  | YES       | Data aggregation time interval. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w. |
| limit      | integer | NO        | Number of results per request. Default: 1000, Maximum: 1000.                                         |
| start_time | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                               |
| end_time   | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                 |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1658880000,         // Timestamp (in seconds)
      "premium": 5.55,            // Premium amount (USD)
      "premium_rate": 0.0261      // Premium rate (e.g., 0.0261 = 2.61%)

    },
    {
       "time": 1658880000,         // Timestamp (in seconds)
       "premium": 5.55,            // Premium amount (USD)
       "premium_rate": 0.0261      // Premium rate (e.g., 0.0261 = 2.61%)

    }
  ]
}
```

