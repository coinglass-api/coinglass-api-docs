# Futures - Liquidation - Coin Liquidation Heatmap Model3


```
GET /api/futures/liquidation/aggregated-heatmap/model3
```


This endpoint provides aggregated liquidation levels on a heatmap chart, calculated based on market data and liquidation leverage levels.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ❌        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description                                                                              |
| ------ | ------ | --------- | ---------------------------------------------------------------------------------------- |
| symbol | string | YES       | Trading coin (e.g., BTC). Retrieve supported coins via the 'supported-coins' API.        |
| range  | string | YES       | Time range for data aggregation. Supported values: 12h, 24h, 3d, 7d, 30d, 90d, 180d, 1y. |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": {
    "y_axis": [47968.54, 48000.00, 48031.46], // Y-axis price levels
    "liquidation_leverage_data": [
      [5, 124, 2288867.26], // Each array: [X-axis index, Y-axis index, liquidation leverage]
      [6, 123, 318624.82],
      [7, 122, 1527940.12]
    ],
    "price_candlesticks": [
      [
        1722676500, // Timestamp (seconds)
        "61486",    // Open price
        "61596.4",  // High price
        "61434.4",  // Low price
        "61539.9",  // Close price
        "63753192.1129" // Trading volume (USD)
      ],
      [
        1722676800,
        "61539.9",
        "61610.0",
        "61480.0",
        "61590.5",
        "42311820.8720"
      ]
    ]
  }
}
```

