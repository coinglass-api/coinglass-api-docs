# Futures - Long-Short Ratio - Exchange Taker Buy/Sell Ratio


```
GET /api/futures/taker-buy-sell-volume/exchange-list
```


This endpoint provides the long/short ratio of aggregated taker buy/sell volumes across exchanges.

***Cache / Update Frequency:*** 1 second for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description                                                                        |
| ------ | ------ | --------- | ---------------------------------------------------------------------------------- |
| symbol | string | YES       | Trading coin (e.g., BTC).  Retrieve supported coins via the 'supported-coins' API. |
| range  | string | YES       | Time range for the data (e.g., 5m, 15m, 30m, 1h, 4h,12h, 24h).                     |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": {
    "symbol": "BTC", // Token symbol
    "buy_ratio": 51.01, // Buy ratio (%)
    "sell_ratio": 48.99, // Sell ratio (%)
    "buy_vol_usd": 1112108532.1688, // Total buy volume (USD)
    "sell_vol_usd": 1068220541.0417, // Total sell volume (USD)
    "exchange_list": [ // Buy/sell data per exchange
      {
        "exchange": "Binance", // Exchange name
        "buy_ratio": 49.22, // Buy ratio (%)
        "sell_ratio": 50.78, // Sell ratio (%)
        "buy_vol_usd": 240077939.5811, // Buy volume (USD)
        "sell_vol_usd": 247674925.1653 // Sell volume (USD)
      },
      {
        "exchange": "OKX", // Exchange name
        "buy_ratio": 50.84, // Buy ratio (%)
        "sell_ratio": 49.16, // Sell ratio (%)
        "buy_vol_usd": 108435724.6214, // Buy volume (USD)
        "sell_vol_usd": 104834502.5904 // Sell volume (USD)
      }
    ]
  }
}

```

