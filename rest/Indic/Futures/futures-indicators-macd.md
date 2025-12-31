# Indic - Futures - Moving Average Convergence Divergence (MACD)


```
GET /api/futures/indicators/macd
```


This endpoint provides Moving Average Convergence Divergence (MACD) for trading pairs .

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
      "time": 1759352400000,
      "macd_value": 1200.54
    },
    {
      "time": 1759356000000,
      "macd_value": 1175.91
    },
}

```

 **Parameters:**
| Name          | Type    | Mandatory | Description                                                                                                    |
| ------------- | ------- | --------- | -------------------------------------------------------------------------------------------------------------- |
| exchange      | string  | YES       | Futures exchange names (e.g., Binance, OKX) .Retrieve supported exchanges via the 'support-exchange-pair' API. |
| symbol        | string  | YES       |  Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'support-exchange-pair' API.                   |
| interval      | string  | YES       | Time interval for data aggregation.  Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w       |
| limit         | string  | NO        | Number of results per request.  Default: 1000, Maximum: 4500                                                   |
| start_time    | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                         |
| end_time      | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                           |
| series_type   | string  | NO        | Price type used in calculation. Supported values: open, high, low, close. Default: close.                      |
| fast_window   | integer | NO        | Fast period window size used for indicator calculation (e.g., 12 for MACD).                                    |
| slow_window   | integer | NO        | Slow period window size used for indicator calculation (e.g., 26 for MACD).                                    |
| signal_window | integer | NO        | Signal line window size used to smooth the fast–slow difference (e.g., 9 for MACD).                            |

