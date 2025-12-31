# Indic - Futures - Futures Basis


```
GET /api/futures/basis/history
```


This endpoint provides historical futures basis data, including open and close basis rates and their corresponding annualized percentage changes over time.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans          | Hobbyist | Startup  | Standard | Professional | Enterprise |
| :------------- | :------- | :------- | :------- | :----------- | :--------- |
| Available      | ✅        | ✅        | ✅        | ✅            | ✅          |
| interval Limit | ​`>=4h`  | ​`>=30m` | No Limit | No Limit     | No Limit   |


 **Parameters:**
| Name       | Type   | Mandatory | Description                                                                                                      |
| ---------- | ------ | --------- | ---------------------------------------------------------------------------------------------------------------- |
| exchange   | string | YES       | Futures exchange names (e.g., Binance, OKX) .Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| symbol     | string | YES       | Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'supported-exchange-pair' API.                    |
| interval   | string | YES       | Data aggregation time interval. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w.             |
| limit      | string | NO        | Number of results per request. Default: 1000, Maximum: 1000.                                                     |
| start_time | string | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                           |
| end_time   | string | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                             |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "time": 1741629600000,            // Timestamp (in milliseconds)
      "open_basis": 0.0504,             // Opening basis (%) - the basis at the start of the interval
      "close_basis": 0.0445,            // Closing basis (%) - the basis at the end of the interval
      "open_change": 39.5,              // Percentage change in basis at opening compared to previous period
      "close_change": 34.56             // Percentage change in basis at closing compared to previous period
    },
    {
      "time": 1741633200000,            // Timestamp (in milliseconds)
      "open_basis": 0.0446,             // Opening basis (%)
      "close_basis": 0.03,              // Closing basis (%)
      "open_change": 34.65,             // Opening basis change (%)
      "close_change": 23.74             // Closing basis change (%)
    }
  ]
}

```

