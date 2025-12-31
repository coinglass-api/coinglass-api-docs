# Spots - Order book - Large Orderbook


```
GET /api/spot/orderbook/large-limit-order
```


This endpoint provides large open limit orders from the current order book for spot trading.(thresholds: BTC ≥ 350K, ETH ≥ 250K, Other ≥ 10K)

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name     | Type   | Mandatory | Description                                                                                        |
| -------- | ------ | --------- | -------------------------------------------------------------------------------------------------- |
| exchange | string | YES       | Exchange name (e.g., Binance). Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| symbol   | string | YES       | Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'supported-exchange-pair' API.      |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "id": 2536823422,
      "exchange_name": "Binance",                // Exchange name
      "symbol": "BTCUSDT",                       // Trading pair
      "base_asset": "BTC",                       // Base asset
      "quote_asset": "USDT",                     // Quote asset
      "price": 20000,                            // Order price
      "start_time": 1742615617000,               // Order start time (timestamp)
      "start_quantity": 109.42454,               // Initial quantity
      "start_usd_value": 2188490.8,              // Initial order value in USD
      "current_quantity": 104.00705,             // Current remaining quantity
      "current_usd_value": 2080141,              // Current remaining value in USD
      "current_time": 1745287267958,             // Current update time (timestamp)
      "executed_volume": 0,                      // Executed volume
      "executed_usd_value": 0,                   // Executed value in USD
      "trade_count": 0,                          // Number of executed trades
      "order_side": 2,                           // Order side: 1 = Buy, 2 = Sell
      "order_state": 1                           // Order state: 1 = Active, 2 = Completed
    }
  ]
}

```

