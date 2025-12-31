# Futures - Taker Buy/Sell - Pair Taker Buy/Sell History


```
GET /api/futures/v2/taker-buy-sell-volume/history
```


This endpoint provides historical data for the long/short ratio of taker buy and sell volumes in futures markets.

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
  "data": [
    {
      "time": 1750183200000,
      "taker_buy_volume_usd": "414120141.0714",
      "taker_sell_volume_usd": "350417509.655"
    },
    {
      "time": 1750186800000,
      "taker_buy_volume_usd": "882509979.6914",
      "taker_sell_volume_usd": "808715578.4428"
    },
    {
      "time": 1750190400000,
      "taker_buy_volume_usd": "572589140.5759",
      "taker_sell_volume_usd": "571005164.3247"
    },
}

```

