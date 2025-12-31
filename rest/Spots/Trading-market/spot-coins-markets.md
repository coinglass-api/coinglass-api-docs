# Spots - Trading market - Coins Markets


```
GET /api/spot/coins-markets
```


This endpoint provides performance-related metrics for all available spot coins

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name     | Type    | Mandatory | Description                             |
| -------- | ------- | --------- | --------------------------------------- |
| per_page | integer | NO        |  Number of results per page.            |
| page     | integer | NO        | Page number for pagination, default: 1. |


**Response Data:**

```json
{
  "code": "0", 
  "msg": "success", 
  "data": [
    {
      "symbol": "BTC", // Token symbol, e.g., BTC for Bitcoin
      "current_price": 87500, // Current price in USD

      "market_cap": 1735007745495.3037, // Market capitalization in USD

      // Price changes in USD over various time intervals
      "price_change_5m": 101.5, // Price change in last 5 minutes
      "price_change_15m": 46.18, // Price change in last 15 minutes
      "price_change_30m": -77.22, // Price change in last 30 minutes
      "price_change_1h": 12.56, // Price change in last 1 hour
      "price_change_4h": 147.75, // Price change in last 4 hours
      "price_change_12h": 147.75, // Price change in last 12 hours
      "price_change_24h": 2799.99, // Price change in last 24 hours
      "price_change_1w": 2989.69, // Price change in last 1 week

      // Price changes in percentage over various time intervals
      "price_change_percent_5m": 0.12, // % change in last 5 minutes
      "price_change_percent_15m": 0.05, // % change in last 15 minutes
      "price_change_percent_30m": -0.09, // % change in last 30 minutes
      "price_change_percent_1h": 0.01, // % change in last 1 hour
      "price_change_percent_4h": 0.17, // % change in last 4 hours
      "price_change_percent_12h": 0.17, // % change in last 12 hours
      "price_change_percent_24h": 3.31, // % change in last 24 hours
      "price_change_percent_1w": 3.54, // % change in last 1 week

      // Total trading volume in USD over various time intervals
      "volume_usd_1h": 129491564.6994, // Total volume in last 1 hour
      "volume_usd_5m": 11056683.8336, // Total volume in last 5 minutes
      "volume_usd_15m": 50625331.2542, // Total volume in last 15 minutes
      "volume_usd_30m": 80070296.0794, // Total volume in last 30 minutes
      "volume_usd_4h": 580775143.5162, // Total volume in last 4 hours
      "volume_usd_12h": 2663308247.353, // Total volume in last 12 hours
      "volume_usd_24h": 3719093876.3834, // Total volume in last 24 hours
      "volume_usd_1w": 16801739001.0272, // Total volume in last 1 week

      // Trading volume change in USD compared to the previous same interval
      "volume_change_usd_1h": -35317032.6336,
      "volume_change_usd_5m": -110911976.2243,
      "volume_change_usd_15m": -59017725.7105,
      "volume_change_usd_30m": -39864985.2519,
      "volume_change_usd_4h": -1084757627.3629,
      "volume_change_usd_12h": 1624238611.116,
      "volume_change_usd_24h": 1967797576.5416,
      "volume_change_usd_1w": -23396586539.5365,

      // Percentage change in trading volume over various time intervals
      "volume_change_percent_1h": -21.43,
      "volume_change_percent_5m": -90.93,
      "volume_change_percent_15m": -53.83,
      "volume_change_percent_30m": -33.24,
      "volume_change_percent_4h": -65.13,
      "volume_change_percent_12h": 156.32,
      "volume_change_percent_24h": 112.36,
      "volume_change_percent_1w": 3.54,

      // Buy-side trading volume in USD (aggressive buy orders)
      "buy_volume_usd_1h": 55687151.2164,
      "buy_volume_usd_5m": 4634327.6087,
      "buy_volume_usd_15m": 20222399.059,
      "buy_volume_usd_30m": 33140975.4441,
      "buy_volume_usd_4h": 278174843.6339,
      "buy_volume_usd_12h": 1410854413.4688,
      "buy_volume_usd_24h": 1923920264.0666,
      "buy_volume_usd_1w": 8116673333.4846,

      // Sell-side trading volume in USD (aggressive sell orders)
      "sell_volume_usd_1h": 73804413.4829,
      "sell_volume_usd_5m": 6422356.2248,
      "sell_volume_usd_15m": 30402932.1951,
      "sell_volume_usd_30m": 46929320.6352,
      "sell_volume_usd_4h": 302600299.8822,
      "sell_volume_usd_12h": 1252453833.8841,
      "sell_volume_usd_24h": 1795173612.3167,
      "sell_volume_usd_1w": 8685065667.5425,

      // Net flow (buy volume - sell volume), representing market sentiment
      "volume_flow_usd_1h": -18117262.2665,
      "volume_flow_usd_5m": -1788028.6161,
      "volume_flow_usd_15m": -10180533.1361,
      "volume_flow_usd_30m": -13788345.1911,
      "volume_flow_usd_4h": -24425456.2483,
      "volume_flow_usd_12h": 158400579.5847,
      "volume_flow_usd_24h": 128746651.7499,
      "volume_flow_usd_1w": -568392334.0579
    }
  ]
}

```

