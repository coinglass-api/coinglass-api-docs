# Spots - Trading market - Pairs Markets


```
GET /api/spot/pairs-markets
```


This endpoint provides performance-related metrics for all available spot trading pairs

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description                                                                       |
| ------ | ------ | --------- | --------------------------------------------------------------------------------- |
| symbol | string | YES       | Trading coin (e.g., BTC). Retrieve supported coins via the 'supported-coins' API. |


**Response Data:**

```json
{
  "code": "0",                        
  "msg": "success",                      
  "data": [
    {
      "symbol": "BTC/USDT",                // Trading pair
      "exchange_name": "Binance",          // Exchange name
      "current_price": 87503.55,           // Current price

      "price_change_1h": 99.55,            // Price change in the past 1 hour
      "price_change_percent_1h": 0.11,     // Price change percentage in the past 1 hour
      "volume_usd_1h": 54425251.2426,      // Trading volume in the past 1 hour (USD)
      "buy_volume_usd_1h": 29304086.0661,  // Buy volume in the past 1 hour (USD)
      "sell_volume_usd_1h": 25121165.1759, // Sell volume in the past 1 hour (USD)
      "volume_change_usd_1h": -24851651.918,   // Volume change in the past 1 hour (USD)
      "volume_change_percent_1h": -31.35,  // Volume change percentage in the past 1 hour
      "net_flows_usd_1h": 4182920.8902,    // Net inflow in the past 1 hour (USD)

      "price_change_4h": 209.56,           // Price change in the past 4 hours
      "price_change_percent_4h": 0.24,     // Price change percentage in the past 4 hours
      "volume_usd_4h": 264625587.5144,     // Trading volume in the past 4 hours (USD)
      "buy_volume_usd_4h": 137768056.2376, // Buy volume in the past 4 hours (USD)
      "sell_volume_usd_4h": 126857531.2762, // Sell volume in the past 4 hours (USD)
      "volume_change_4h": -526166190.0218, // Volume change in the past 4 hours (USD)
      "volume_change_percent_4h": -66.54,  // Volume change percentage in the past 4 hours
      "net_flows_usd_4h": 10910524.9614,   // Net inflow in the past 4 hours (USD)

      "price_change_12h": 2925.55,         // Price change in the past 12 hours
      "price_change_percent_12h": 3.46,    // Price change percentage in the past 12 hours
      "volume_usd_12h": 1212930000.2011,   // Trading volume in the past 12 hours (USD)
      "buy_volume_usd_12h": 662857153.6506, // Buy volume in the past 12 hours (USD)
      "sell_volume_usd_12h": 550072846.5499, // Sell volume in the past 12 hours (USD)
      "volume_change_12h": 842092388.1946, // Volume change in the past 12 hours (USD)
      "volume_change_percent_12h": 227.08, // Volume change percentage in the past 12 hours
      "net_flows_usd_12h": 112784307.1007, // Net inflow in the past 12 hours (USD)

      "price_change_24h": 2735.79,         // Price change in the past 24 hours
      "price_change_percent_24h": 3.23,    // Price change percentage in the past 24 hours
      "volume_usd_24h": 1585522232.603,    // Trading volume in the past 24 hours (USD)
      "buy_volume_usd_24h": 843617569.7248, // Buy volume in the past 24 hours (USD)
      "sell_volume_usd_24h": 741904662.8776, // Sell volume in the past 24 hours (USD)
      "volume_change_24h": 873336140.8197, // Volume change in the past 24 hours (USD)
      "volume_change_percent_24h": 122.63, // Volume change percentage in the past 24 hours
      "net_flows_usd_24h": 101712906.8472, // Net inflow in the past 24 hours (USD)

      "price_change_1w": 3057.83,          // Price change in the past 1 week
      "price_change_percent_1w": 3.62,     // Price change percentage in the past 1 week
      "volume_usd_1w": 6808077059.7062,    // Trading volume in the past 1 week (USD)
      "buy_volume_usd_1w": 3374037733.8429, // Buy volume in the past 1 week (USD)
      "sell_volume_usd_1w": 3434039325.8627, // Sell volume in the past 1 week (USD)
      "volume_change_usd_1w": -11208235126.1193, // Volume change in the past 1 week (USD)
      "volume_change_percent_1w": -62.21,  // Volume change percentage in the past 1 week
      "net_flows_usd_1w": -60001592.0198   // Net inflow in the past 1 week (USD)
    }
  ]
}

```

