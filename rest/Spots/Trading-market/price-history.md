# Spots - Trading market - Price OHLC History


```
GET /api/spot/price/history
```


This endpoint provides historical open, high, low, and close (OHLC) price data for cryptocurrencies over specified timeframes.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |


 **Parameters:**
| Name       | Type   | Mandatory | Description                                                                                                   |
| ---------- | ------ | --------- | ------------------------------------------------------------------------------------------------------------- |
| exchange   | string | YES       | spot exchange names (e.g., Binance, OKX) .Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| symbol     | string | YES       | Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'supported-exchange-pair' API.                 |
| interval   | string | YES       | Data aggregation time interval. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w.          |
| limit      | string | NO        | Number of results per request. Default: 1000, Maximum: 1000.                                                  |
| start_time | string | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                        |
| end_time   | string | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                          |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1741690800000,
      "open": 81808.25,//open price
      "high": 82092.34, //high price
      "low": 81400,//low price
      "close": 81720.34,//close price
      "volume_usd": 96823535.5724
    },
    {
      "time": 1741694400000,
      "open": 81720.33,
      "high": 81909.69,
      "low": 81017,
      "close": 81225.5,
      "volume_usd": 150660424.1863
    },
```

