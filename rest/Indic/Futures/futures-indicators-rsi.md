# Indic - Futures - Pair RSI


```
GET /api/futures/indicators/rsi
```


This endpoint provides RSI values for trading pairs .

***Cache / Update Frequency:*** Real time for all the API plans..

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |

<br />

**Response Data**

```json
{
  "code": "0",
  "data": [
    {
      "time": 1759287600000,
      "rsi_value": 59.32633395
    },
    {
      "time": 1759291200000,
      "rsi_value": 60.90396216
    },
}

```

 **Parameters:**
| Name        | Type    | Mandatory | Description                                                                                                    |
| ----------- | ------- | --------- | -------------------------------------------------------------------------------------------------------------- |
| exchange    | string  | YES       | Futures exchange names (e.g., Binance, OKX) .Retrieve supported exchanges via the 'support-exchange-pair' API. |
| symbol      | string  | YES       |  Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'support-exchange-pair' API.                   |
| interval    | string  | YES       | Time interval for data aggregation.  Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w       |
| limit       | string  | NO        | Number of results per request.  Default: 1000, Maximum: 4500                                                   |
| start_time  | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                         |
| end_time    | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                           |
| window      | integer | NO        | Window size — defines the number of data points used for indicator calculation (e.g., 14 for RSI).             |
| series_type | string  | NO        | Price type used in calculation. Supported values: open, high, low, close. Default: close.                      |

