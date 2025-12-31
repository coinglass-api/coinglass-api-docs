# Indic - Other - Exchanges Assets Transparency


```
GET /api/exchange_assets_transparency/list
```


This endpoint provides transparency data of exchange assets, including total balances, inflows, balance changes, open interest, leverage, and trading volume.

***Cache / Update Frequency:*** 1 hour

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |



**Response Data:**

```json
{
  "code": "0",                         // Status code
  "data": [
    {
      "exchange_name": "Binance",       //Exchange name
      "exchange_logo_url": "https://cdn.coinglasscdn.com/static/exchanges/270.png",  //Exchange Logo
      "balance_usd": 178382444198.04,   // Total balance
      "balance_change_usd_24h": -4244709940.9,  // 24h change
      "balance_change_usd_7d": 183489103818.63, // 7d change
      "inflow_usd_24h": 1104357008.908988,      // 24h inflow
      "inflow_usd_7d": 870098130.1614555,       // 7d inflow
      "open_interest": 28940016260,             // Open interest
      "average_leverage": 0.1622,               // Avg leverage
      "volume_usd": 114901619432                // Volume
    },
    {
      "exchange_name": "Bitfinex",              //Exchange Name
      "exchange_logo_url": "https://cdn.coinglasscdn.com/static/exchanges/bitfinex.jpg", //Exchange Logo
      "balance_usd": 25836820506.17,            // Total balance
      "balance_change_usd_24h": -164420313.45,  // 24h change
      "balance_change_usd_7d": 26135897993.59,  // 7d change
      "inflow_usd_24h": 225181636.35856062,     // 24h inflow
      "inflow_usd_7d": 706172180.891416,        // 7d inflow
      "open_interest": 732439767,               // Open interest
      "average_leverage": 0.0283,               // Avg leverage
      "volume_usd": 68891576                    // Volume
    }
  ]
}
```

