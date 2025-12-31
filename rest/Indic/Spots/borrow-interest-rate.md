# Indic - Spots - Borrow Interest Rate


```
GET /api/borrow-interest-rate/history
```


This endpoint provides daily borrowing interest rates for cryptocurrencies.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |

<br />


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                                          |
| ---------- | ------- | --------- | ---------------------------------------------------------------------------------------------------- |
| exchange   | string  | YES       | Exchange name  support:Binance ,OKX,Bybit                                                            |
| symbol     | string  | YES       | Trading coin (e.g., BTC). Retrieve supported coins via the 'supported-coins' API.                    |
| interval   | string  | YES       | Data aggregation time interval. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w. |
| limit      | integer | NO        | Number of results per request. Default: 1000, Maximum: 1000.                                         |
| start_time | integer | NO        |  Start timestamp in milliseconds (e.g., 1641522717000).                                              |
| end_time   | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                 |


**Response Data:**

```json
{
  "code": "0",                             
  "msg": "success",                         
  "data": [
    {
      "time": 1741636800,                  // Timestamp (in seconds)
      "interest_rate": 0.002989            // daily Interest rate
    },
    {
      "time": 1741640400,                  // Timestamp (in seconds)
      "interest_rate": 0.002989            // daily Interest rate
    }
  ]
}

```

