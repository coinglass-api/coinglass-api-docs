# Futures - Trading Market - Exchange Rank


```
GET /api/futures/indicators/rsi
```


This endpoint provides a ranking list of futures exchanges on CoinGlass.

***Cache / Update Frequency:*** every 1 minutes for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |

<br />

**Response Data**

```json
{
  "code": "0",
  "data": [
    {
      "exchange": "Binance",
      "open_interest_usd": 27564494330,
      "volume_usd": 54150896832,
      "liquidation_usd_24h": 58774453.06516198
    },
    {
      "exchange": "OKX",
      "open_interest_usd": 8586569027,
      "volume_usd": 22670494849,
      "liquidation_usd_24h": 19276388.77685
    },
  ]
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

