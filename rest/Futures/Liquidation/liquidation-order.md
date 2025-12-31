# Futures - Liquidation - Liquidation Order


```
GET /api/futures/liquidation/order
```


This endpoint provides liquidation order data from the past 7 days, including exchange, trading pair, and liquidation amount details.

***Cache / Update Frequency:*** 1 second for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name                   | Type    | Mandatory | Description                                                                                             |
| ---------------------- | ------- | --------- | ------------------------------------------------------------------------------------------------------- |
| exchange               | string  | YES       | Exchange name (e.g., Binance, OKX). Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| symbol                 | string  | YES       | Trading coin (e.g., BTC). Retrieve supported coins via the 'supported-coins' API.                       |
| min_liquidation_amount | string  | YES       | Minimum threshold for liquidation events.  Max 200 records per request.                                 |
| start_time             | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                  |
| end_time               | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                    |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "exchange_name": "BINANCE", // Exchange name
      "symbol": "BTCUSDT", // Trading pair symbol
      "base_asset": "BTC", // Base asset
      "price": 87535.9, // Liquidation price
      "usd_value": 205534.2932, // Transaction amount (USD)
      "side": 2, // Order direction (1: Buy, 2: Sell)
      "time": 1745216319263 // Timestamp
    },
    {
      "exchange_name": "BINANCE", // Exchange name
      "symbol": "BTCUSDT", // Trading pair symbol
      "base_asset": "BTC", // Base asset
      "price": 87465.2, // Liquidation price
      "usd_value": 15918.6664, // Transaction amount (USD)
      "side": 2, // Order direction (1: Buy, 2: Sell)
      "time": 1745215647165 // Timestamp
    }
  ]
}

```

