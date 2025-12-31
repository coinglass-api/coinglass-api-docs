# Futures - Liquidation - Coin Liquidation History


```
GET /api/futures/liquidation/aggregated-history
```


This endpoint provides aggregated historical data for both long and short liquidations of a coin across multiple exchanges.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |

<br />


 **Parameters:**
| Name          | Type    | Mandatory | Description                                                                                              |
| ------------- | ------- | --------- | -------------------------------------------------------------------------------------------------------- |
| exchange_list | string  | YES       | List of exchange names to retrieve data from (e.g.,  'Binance, OKX, Bybit')                              |
| symbol        | string  | YES       | Trading coin (e.g., BTC). Retrieve supported coins via the 'supported-coins' API.                        |
| interval      | string  | YES       | Time interval for data aggregation. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w. |
| limit         | integer | NO        | Number of results per request. Default: 1000, Maximum: 1000.                                             |
| start_time    | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                   |
| end_time      | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                     |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1658966400000, // Timestamp (milliseconds) 
      "aggregated_long_liquidation_usd": 5916885.14234,//aggregated Long position liquidation amount (USD)
      "aggregated_short_liquidation_usd": 12969583.87632 //aggregated Short position liquidation amount (USD)
    },
    {
      "time": 1659052800000,  // Timestamp (milliseconds)
      "aggregated_long_liquidation_usd": 5345708.23191, //aggregated Long position liquidation amount (USD)
      "aggregated_short_liquidation_usd": 6454875.54909 //aggregated Short position liquidation amount (USD)
    },
  ]
}


```

