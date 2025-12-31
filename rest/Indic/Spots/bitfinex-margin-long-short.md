# Indic - Spots - Bitfinex Margin Long/Short


```
GET /api/bitfinex-margin-long-short
```


This endpoint provides data on margin long and short positions from Bitfinex.

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
| symbol     | string  | YES       | BTC,ETH                                                                                              |
| limit      | integer | NO        | Number of results per request. Default: 1000, Maximum: 1000.                                         |
| interval   | string  | YES       | Data aggregation time interval. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w. |
| start_time | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                               |
| end_time   | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                 |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1658880000,              // Timestamp, representing the data's corresponding time point
      "long_quantity": 104637.94,       // Long position quantity
      "short_quantity": 2828.53        // Short position quantity
    },
    {
      "time": 1658966400,              // Timestamp, representing the data's corresponding time point
      "long_quantity": 105259.46,       // Long position quantity
      "short_quantity": 2847.84        // Short position quantity
    }
    // More data entries...
  ]
}

```

