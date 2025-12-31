# Futures - Order Book - Large Orderbook History


```
GET /api/futures/orderbook/large-limit-order-history
```


This endpoint provides completed historical large limit orders from the order book for futures trading (thresholds: BTC ≥ 1M, ETH ≥ 500K, Other ≥ 50K)

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                                        |
| ---------- | ------- | --------- | -------------------------------------------------------------------------------------------------- |
| exchange   | string  | YES       | Exchange name (e.g., Binance). Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| symbol     | string  | YES       | Trading pair (e.g., BTCUSDT). Check supported pairs through the 'supported-exchange-pair' API.     |
| start_time | integer | YES       | Start timestamp in milliseconds (e.g., 1723625037000).                                             |
| end_time   | integer | YES       | End timestamp in milliseconds (e.g., 1723626037000).                                               |
| state      | integer | YES       | Status of the order —  1for ''In Progress''  2 for "Finish"  3 for "Revoke"                        |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "id": 2895605135,
      "exchange_name": "Binance",               // Exchange name
      "symbol": "BTCUSDT",                      // Trading pair
      "base_asset": "BTC",                      // Base asset
      "quote_asset": "USDT",                    // Quote asset
      "price": 89205.9,                         // Order price
      "start_time": 1745287309000,              // Order start time (milliseconds)
      "start_quantity": 25.779,                 // Initial order quantity
      "start_usd_value": 2299638.8961,          // Initial order value (USD)
      "current_quantity": 25.779,               // Remaining quantity
      "current_usd_value": 2299638.8961,        // Remaining value (USD)
      "current_time": 1745287309000,            // Current timestamp (milliseconds)
      "executed_volume": 0,                     // Executed volume
      "executed_usd_value": 0,                  // Executed value (USD)
      "trade_count": 0,                         // Number of trades executed
      "order_side": 1,                          // Order side: 1 = Sell, 2 = Buy
      "order_state": 2,                         // Order state: 0 = Not started, 1 = Open, 2 = Filled, 3 = Cancelled
      "order_end_time": 1745287328000           // Order end time (milliseconds)
    }
    ....
  ]
}

```

