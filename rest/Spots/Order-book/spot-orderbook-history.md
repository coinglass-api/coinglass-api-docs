# Spots - Order book - Pair Orderbook Bid&Ask(±range)


```
GET /api/spot/orderbook/ask-bids-history
```


This endpoint provides historical data of the order book for spot trading, including total bid/ask volumes within a specific price range.

***Cache / Update Frequency:*** every 5 seconds for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                                          |
| ---------- | ------- | --------- | ---------------------------------------------------------------------------------------------------- |
| exchange   | string  | YES       | Exchange name (e.g., Binance). Retrieve supported exchanges via the 'supported-exchange-pair' API.   |
| symbol     | string  | YES       | Trading pair (e.g., BTCUSDT). Check supported pairs through the 'supported-exchange-pair' API.       |
| interval   | string  | YES       | Data aggregation time interval. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w. |
| limit      | integer | NO        | Number of results per request. Default: 1000, Maximum: 1000.                                         |
| start_time | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                               |
| end_time   | integer | NO        |  End timestamp in milliseconds (e.g., 1641522717000).                                                |
| range      | string  | NO        | Depth percentage (e.g., 0.25, 0.5, 0.75, 1, 2, 3, 5, 10).                                            |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "bids_usd": 81639959.9338,        // Total long position amount (USD)
      "bids_quantity": 1276.645,        // Total long quantity
      "asks_usd": 78533053.6862,        // Total short position amount (USD)
      "asks_quantity": 1217.125,        // Total short quantity
      "time": 1714003200000             // Timestamp (in milliseconds)
    },
    {
      "bids_usd": 62345879.8821,
      "bids_quantity": 980.473,
      "asks_usd": 65918423.4715,
      "asks_quantity": 1021.644,
      "time": 1714089600000
    }
  ]
}

```

