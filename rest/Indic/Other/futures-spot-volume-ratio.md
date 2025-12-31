# Indic - Other - Futures vs Spot Volume Ratio


```
GET /api/futures_spot_volume_ratio
```


This endpoint provides time-series data for the futures-to-spot trading volume ratio, including timestamp, volume ratio, futures trading volume (USD), and spot trading volume (USD).

**Cache / Update Frequency:** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name          | Type    | Mandatory | Description                                                                                             |
| ------------- | ------- | --------- | ------------------------------------------------------------------------------------------------------- |
| exchange_list | string  | YES       | List of exchange names to retrieve data from (e.g.,  'Binance, OKX, Bybit')                             |
| symbol        | string  | YES       | Trading coin (e.g., BTC).Retrieve supported coins via the 'support-coins' API.                          |
| interval      | string  | YES       | Time interval for data aggregation.Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w. |
| limit         | integer | NO        | Number of results per request.Default: 1000, Maximum: 1000.                                             |
| start_time    | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                  |
| end_time      | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                    |


**Response Data:**

```json
{
  "code": "0",
  "data": [
  {
    "time": 1766588040000,        // timestamp (ms)
    "futures_spot_vol_ratio": 16.9974, // futures / spot volume ratio
    "futures_vol_usd": 59900899.685,   // futures volume (USD)
    "spot_vol_usd": 3524120.4165       // spot volume (USD)
  },
  {
    "time": 1766588100000,        // timestamp (ms)
    "futures_spot_vol_ratio": 9.0887,  // futures / spot volume ratio
    "futures_vol_usd": 24469968.832,   // futures volume (USD)
    "spot_vol_usd": 2692346.1708       // spot volume (USD)
  }
]
}
```

