# On-Chain - Exchange data - Exchange Balance List


```
GET /api/exchange/balance/list
```


This endpoint provides exchange-level asset balance data, including total holdings and percentage changes over 1-day, 7-day, and 30-day periods.

***Cache / Update Frequency:*** every 1 hour for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description                            |
| ------ | ------ | --------- | -------------------------------------- |
| symbol | string | YES       | Trading coin eg. BTC , ETH , USDT(ETH) |


**Response Data:**

```json
{
  "code": "0",                                  
  "msg": "success",                            
  "data": [
    {
      "exchange_name": "Coinbase",               // Exchange name
      "total_balance": 716590.351233,            // Total balance
      "balance_change_1d": 638.797302,           // Balance change in 24 hours
      "balance_change_percent_1d": 0.09,         // Balance change percentage in 24 hours (%)
      "balance_change_7d": 799.967408,           // Balance change in 7 days
      "balance_change_percent_7d": 0.11,         // Balance change percentage in 7 days (%)
      "balance_change_30d": -29121.977486,       // Balance change in 30 days
      "balance_change_percent_30d": -3.91        // Balance change percentage in 30 days (%)
    },
    {
      "exchange_name": "Binance",                // Exchange name
      "total_balance": 582344.497738,            // Total balance
      "balance_change_1d": 505.682778,           // Balance change in 24 hours
      "balance_change_percent_1d": 0.09,         // Balance change percentage in 24 hours (%)
      "balance_change_7d": -3784.88544,          // Balance change in 7 days
      "balance_change_percent_7d": -0.65,        // Balance change percentage in 7 days (%)
      "balance_change_30d": 3753.870055,         // Balance change in 30 days
      "balance_change_percent_30d": 0.65         // Balance change percentage in 30 days (%)
    }
  ]
}

```

