# Futures - Order Book - Large Orderbook


```
GET /api/futures/orderbook/large-limit-order
```


This endpoint provides large open limit orders from the current order book for futures trading.(thresholds: BTC ≥ 1M, ETH ≥ 500K, Other ≥ 50K)

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name     | Type   | Mandatory | Description                                                                                        |
| -------- | ------ | --------- | -------------------------------------------------------------------------------------------------- |
| exchange | string | YES       | Exchange name (e.g., Binance). Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| symbol   | string | YES       | Trading pair (e.g., BTCUSDT). Retrieve supported pair via the 'supported-exchange-pair' API.       |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data":[
  {
    "id": 2868159989,
    "exchange_name": "Binance",            // Exchange name
    "symbol": "BTCUSDT",                   // Trading pair
    "base_asset": "BTC",                   // Base asset
    "quote_asset": "USDT",                 // Quote asset

    "price": 56932,                  // Order price
    "start_time": 1722964242000,           // Order start time (ms)
    "start_quantity": 28.39774,            // Initial order quantity
    "start_usd_value": 1616740.1337,       // Initial USD value

    "current_quantity": 18.77405,          // Current remaining quantity
    "current_usd_value": 1068844.21,       // Current USD value
    "current_time": 1722964272000,         // Current time (ms)

    "executed_volume": 0,                  // Executed volume
    "executed_usd_value": 0,               // Executed USD value
    "trade_count": 0,                      // Number of trades

    "order_side": 2,                       // Order side: 1 - Sell, 2 - Buy
    "order_state": 1                       // Order state: 1 - Open, 2 - Filled, 3      - Canceled
    }
   ]
}
```

