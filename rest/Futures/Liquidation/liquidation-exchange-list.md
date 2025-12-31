# Futures - Liquidation - Liquidation Exchange List


```
GET /api/futures/liquidation/exchange-list
```


This endpoint provides liquidation data for a specific coin across all exchanges.

***Cache / Update Frequency:*** 10 second for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description                                                                        |
| ------ | ------ | --------- | ---------------------------------------------------------------------------------- |
| symbol | string | NO        | Trading coin (e.g., BTC).  Retrieve supported coins via the 'supported-coins' API. |
| range  | string | YES       | Time range for data aggregation.  Supported values: 1h, 4h, 12h, 24h.              |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "exchange": "All", // Total data from all exchanges
      "liquidation_usd": 14673519.81739075, // Total liquidation amount (USD)
      "long_liquidation_usd": 451394.17404598, // Long position liquidation amount (USD)
      "short_liquidation_usd": 14222125.64334477 // Short position liquidation amount (USD)
    },
    {
      "exchange": "Bybit", // Exchange name
      "liquidation_usd": 4585290.13404, // Total liquidation amount (USD)
      "long_liquidation_usd": 104560.13885, // Long position liquidation (USD)
      "short_liquidation_usd": 4480729.99519 // Short position liquidation (USD)
    }
  ]
}

```

