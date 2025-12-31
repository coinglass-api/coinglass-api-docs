# Futures - Taker Buy/Sell - Footprint History (90d)


```
GET /api/futures/volume/footprint-history
```


This endpoint provides historical footprint chart data for futures markets, including buy and sell volumes at each price level.

**Cache / Update Frequency:** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ❌        | ✅            | ✅          |


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                                             |
| ---------- | ------- | --------- | ------------------------------------------------------------------------------------------------------- |
| exchange   | string  | YES       | Futures exchange names (Supported Binance, OKX,Bybit,Hyperliquid)                                       |
| symbol     | string  | YES       | Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'support-exchange-pair' API.             |
| interval   | string  | YES       | Time interval for data aggregation. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w |
| limit      | integer | NO        | Number of results per request. Default: 1000, Maximum: 1000                                             |
| start_time | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                  |
| end_time   | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                    |


**Response Data:**

```json
{
  "code": "0",  // code (0 = success)
  "data": [
    [
      1757808000,  // Timestamp (seconds)
      [
        [
          115765,        // Price start
          115770,        // Price end
          3.223,         // Taker buy volume 
          9.906,         // Taker sell volume 
          373118.1958,   // Taker buy volume (quote currency)
          1146773.5391,  // Taker sell volume (quote currency)
          373118.1958,   // Taker buy volume (USDT)
          1146773.5391,  // Taker sell volume (USDT)
          193,           // Taker buy trade count
          153            // Taker sell trade count
        ],
        [
          115770,
          115775,
          3.315,         // Taker buy volume
          0.528,         // Taker sell volume
          383782.5569,   // Taker buy volume (quote currency)
          61127.0686,    // Taker sell volume (quote currency)
          383782.5569,   // Taker buy volume (USDT)
          61127.0686,    // Taker sell volume (USDT)
          40,            // Taker buy trade count
          64             // Taker sell trade count
        ]
      ]
    ]
  ]
}
```

