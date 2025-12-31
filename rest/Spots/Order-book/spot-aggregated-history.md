# Spots - Order book - Coin Orderbook Bid&Ask(±range)


```
GET /api/spot/orderbook/aggregated-ask-bids-history
```


This endpoint provides historical data of the aggregated order book for spot trading, including total bid/ask volumes within a specific price range.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |


 **Parameters:**
| Name          | Type    | Mandatory | Description                                                                                          |
| ------------- | ------- | --------- | ---------------------------------------------------------------------------------------------------- |
| exchange_list | string  | YES       | List of exchange names to retrieve data from (e.g., 'ALL', or 'Binance, OKX, Bybit')                 |
| symbol        | string  | YES       | Trading coin (e.g., BTC). Retrieve supported coins via the 'supported-coins' API.                    |
| interval      | string  | YES       | Data aggregation time interval. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w. |
| limit         | integer | NO        | Number of results per request. Default: 1000, Maximum: 1000.                                         |
| start_time    | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                               |
| end_time      | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                 |
| range         | string  | NO        | Depth percentage (e.g., 0.25, 0.5, 0.75, 1, 2, 3, 5, 10).                                            |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "aggregated_bids_usd": 12679537.0806,         // Aggregated long amount (USD)
      "aggregated_bids_quantity": 197.99861,        // Aggregated long quantity
      "aggregated_asks_usd": 10985519.9268,         // Aggregated short amount (USD)
      "aggregated_asks_quantity": 170.382,          // Aggregated short quantity
      "time": 1714003200000                         // Timestamp (milliseconds)
    },
    {
      "aggregated_bids_usd": 18423845.1947,
      "aggregated_bids_quantity": 265.483,
      "aggregated_asks_usd": 17384271.5521,
      "aggregated_asks_quantity": 240.785,
      "time": 1714089600000
    }
  ]
}

```

