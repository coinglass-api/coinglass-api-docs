# Spots - Taker Buy/Sell - Pair Taker Buy/Sell History


```
GET /api/spot/taker-buy-sell-volume/history
```


This endpoint provides historical data for the long/short ratio of taker buy and sell volumes in spot markets.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup | Standard | Professional | Enterprise |
| :------------- | :------- | :------ | :------- | :----------- | :--------- |
| Available      | ✅        | ✅       | ✅        | ✅            | ✅          |
| interval Limit | `>=4h`   | `>=30m` | No Limit | No Limit     | No Limit   |


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                                              |
| ---------- | ------- | --------- | -------------------------------------------------------------------------------------------------------- |
| exchange   | string  | YES       | Exchange name (e.g., Binance). Retrieve supported exchanges via the 'supported-exchange-pair' API.       |
| symbol     | string  | YES       | Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'supported-exchange-pair' API.            |
| interval   | string  | YES       | Time interval for data aggregation.  Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w |
| limit      | integer | NO        | Number of results per request.  Default: 1000, Maximum: 1000                                             |
| start_time | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                   |
| end_time   | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                     |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1741622400000, // Timestamp in milliseconds
      "taker_buy_volume_usd": "10551.033", // Taker buy volume (USD)
      "taker_sell_volume_usd": "11308" // Taker sell volume (USD)
    },
    {
      "time": 1741626000000,
      "taker_buy_volume_usd": "15484.245",
      "taker_sell_volume_usd": "16316.118"
    },
    {
      "time": 1741629600000,
      "taker_buy_volume_usd": "20340.501",
      "taker_sell_volume_usd": "18977.660"
    }
  ]
}

```

