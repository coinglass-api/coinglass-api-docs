# Options - Option Max Pain


```
GET /api/option/max-pain
```


This endpoint provides the max pain price for options.

***Cache / Update Frequency:*** every 1 minute for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |

&#x20;


 **Parameters:**
| Name     | Type   | Mandatory | Description                                   |
| -------- | ------ | --------- | --------------------------------------------- |
| symbol   | string | YES       | Trading coin (e.g., BTC,ETH).                 |
| exchange | string | YES       | Exchange name (e.g., Deribit, Binance, OKX).  |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "date": "250422",                                   // Date (YYMMDD format)
      "call_open_interest_market_value": 1616749.22,      // Call option market value (USD)
      "put_open_interest": 512.5,                         // Put option open interest (contracts)
      "put_open_interest_market_value": 49687.62,         // Put option market value (USD)
      "max_pain_price": "84000",                          // Max pain price
      "call_open_interest": 953.7,                        // Call option open interest (contracts)
      "call_open_interest_notional": 83519113.56,         // Call option notional value (USD)
      "put_open_interest_notional": 44881569.13           // Put option notional value (USD)
    },
    {
      "date": "250423",                                   // Date (YYMMDD format)
      "call_open_interest_market_value": 2274700.52,      // Call option market value (USD)
      "put_open_interest": 1204.3,                        // Put option open interest (contracts)
      "put_open_interest_market_value": 374536.01,        // Put option market value (USD)
      "max_pain_price": "85000",                          // Max pain price
      "call_open_interest": 1302.2,                       // Call option open interest (contracts)
      "call_open_interest_notional": 114040373.53,        // Call option notional value (USD)
      "put_open_interest_notional": 105465691.73          // Put option notional value (USD)
    }
  ]
}

```

