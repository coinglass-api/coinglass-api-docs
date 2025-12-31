# Options - Options Info


```
GET /api/option/info
```


This endpoint provides detailed information about open interest and trading volume for options across different exchanges

***Cache / Update Frequency:*** every 30 seconds for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |

<br />


 **Parameters:**
| Name   | Type   | Mandatory | Description                    |
| ------ | ------ | --------- | ------------------------------ |
| symbol | string | YES       | Trading coin (e.g., BTC,ETH).  |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "exchange_name": "All",                           // Exchange name
      "open_interest": 361038.78,                       // Open interest (contracts)
      "oi_market_share": 100,                           // Market share (%)
      "open_interest_change_24h": 2.72,                 // 24h open interest change (%)
      "open_interest_usd": 31623069708.138245,          // Open interest value (USD)
      "volume_usd_24h": 2764676957.0569425,             // 24h trading volume (USD)
      "volume_change_percent_24h": 303.1                // 24h volume change (%)
    },
    {
      "exchange_name": "Deribit",                       // Exchange name
      "open_interest": 262641.9,                        // Open interest (contracts)
      "oi_market_share": 72.74,                         // Market share (%)
      "open_interest_change_24h": 2.57,                 // 24h open interest change (%)
      "open_interest_usd": 23005403973.349,             // Open interest value (USD)
      "volume_usd_24h": 2080336672.709                  // 24h trading volume (USD)
    }
  ]
}

```

