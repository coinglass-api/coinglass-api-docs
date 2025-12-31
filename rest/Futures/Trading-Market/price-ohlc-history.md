# Futures - Trading Market - Price History (OHLC)


```
GET /api/futures/price/history
```


This endpoint provides historical open, high, low, and close (OHLC) price data for cryptocurrencies over specified timeframes.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                                                       |
| ---------- | ------- | --------- | ----------------------------------------------------------------------------------------------------------------- |
| exchange   | string  | YES       |  Futures exchange names (e.g., Binance, OKX) .Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| symbol     | string  | YES       | Trading pair (e.g., BTCUSDT). Check supported pairs through the 'supported-exchange-pair' API.                    |
| interval   | string  | YES       | Data aggregation time interval. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w.              |
| limit      | integer | YES       | Number of results per request. Default: 1000, Maximum: 1000.                                                      |
| start_time | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                            |
| end_time   | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                              |


**Response Data:**

```json
{
  "code": "0",
  "data": [
    {
      "time": 1745366400000,
      "open": "93404.9",
      "high": "93864.9",
      "low": "92730",
      "close": "92858.2",
      "volume_usd": "1166471854.3026"
    },
    {
      "time": 1745370000000,
      "open": "92858.2",
      "high": "93464.8",
      "low": "92552",
      "close": "92603.8",
      "volume_usd": "871812560.3437"
    },
    ...
 ]
}    
    
    
```

