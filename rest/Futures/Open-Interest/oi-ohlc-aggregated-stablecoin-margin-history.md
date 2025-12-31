# Futures - Open Interest - Aggregated Stablecoin Margin History (OHLC)


```
GET /api/futures/open-interest/aggregated-stablecoin-history
```


This endpoint provides aggregated stablecoin-margined open interest data in OHLC (open, high, low, close) candlestick format.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |

&#x20;


 **Parameters:**
| Name          | Type    | Mandatory | Description                                                                                                                     |
| ------------- | ------- | --------- | ------------------------------------------------------------------------------------------------------------------------------- |
| exchange_list | string  | YES       | Comma-separated exchange names (e.g., "Binance,OKX,Bybit"). Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| symbol        | string  | YES       | Trading coin (e.g., BTC).Retrieve supported coins via the 'supported-coins' API.                                                |
| interval      | string  | YES       | Time interval for data aggregation.Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w                          |
| limit         | integer | NO        | Number of results per request. Default: 1000, Maximum: 1000                                                                     |
| start_time    | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                                          |
| end_time      | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                                            |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 2644845344000, // Timestamp (ms)
      "open": "2644845344",   // Open interest at interval start
      "high": "2692643311",   // Highest open interest during interval
      "low": "2576975597",    // Lowest open interest during interval
      "close": "2608846475"   // Open interest at interval end
    },
    {
      "time": 2608846475000, // Timestamp (ms)
      "open": "2608846475",  // Open interest at interval start
      "high": "2620807645",  // Highest open interest during interval
      "low": "2327236202",   // Lowest open interest during interval
      "close": "2340177420"  // Open interest at interval end
    },
    ....
  ]
}

```

