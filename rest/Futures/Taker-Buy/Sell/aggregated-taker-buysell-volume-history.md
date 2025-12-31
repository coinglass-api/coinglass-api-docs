# Futures - Taker Buy/Sell - Coin Taker Buy/Sell History


```
GET /api/futures/aggregated-taker-buy-sell-volume/history
```


This endpoint provides historical data for the long/short ratio of aggregated taker buy and sell volumes for futures cryptocurrencies.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |

&#x20;


 **Parameters:**
| Name          | Type    | Mandatory | Description                                                                                              |
| ------------- | ------- | --------- | -------------------------------------------------------------------------------------------------------- |
| exchange_list | string  | YES       | exchange_list: List of exchange names to retrieve data from (e.g., 'Binance,OKX,Bybit')                  |
| symbol        | string  | YES       | Trading pair (e.g., BTC). Retrieve supported coins via the 'supported-coins' API.                        |
| interval      | string  | YES       | Time interval for data aggregation.  Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w |
| limit         | integer | NO        | Number of results per request.  Default: 1000, Maximum: 1000                                             |
| start_time    | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                   |
| end_time      | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                     |
| unit          | string  | NO        | Unit for the returned data, choose between 'usd' or 'coin'.                                              |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1741622400000, // Timestamp in milliseconds
      "aggregated_buy_volume_usd": 968834542.3787, // Aggregated buy volume (USD)
      "aggregated_sell_volume_usd": 1054582654.8138 // Aggregated sell volume (USD)
    },
    {
      "time": 1741626000000,
      "aggregated_buy_volume_usd": 1430620763.2041,
      "aggregated_sell_volume_usd": 1559166911.2821
    },
    {
      "time": 1741629600000,
      "aggregated_buy_volume_usd": 1897261721.0129,
      "aggregated_sell_volume_usd": 2003812276.7812
    }
  ]
}

```

