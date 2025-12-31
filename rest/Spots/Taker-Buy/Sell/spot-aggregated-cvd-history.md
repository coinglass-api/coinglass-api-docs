# Spots - Taker Buy/Sell - Aggregated Cumulative Volume Delta (CVD)


```
GET /api/spot/aggregated-cvd/history
```


This endpoint provides historical CVD data for a single cryptocurrency within one spot exchange, aggregated across multiple trading pairs.

**Cache / Update Frequency:** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name          | Type    | Mandatory | Description                                                                                                                        |
| ------------- | ------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| exchange_list | string  | YES       | Comma-separated exchange names (e.g., "binance, okx, bybit"). Retrieve supported exchanges via the 'supported-exchange-pairs' API. |
| symbol        | string  | YES       | Trading pair (e.g., BTC). Retrieve supported coins via the 'support-coins' API.                                                    |
| interval      | string  | YES       | Time interval for data aggregation.
Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w
                           |
| limit         | integer | NO        | Number of results per request. Default: 1000, Maximum: 4500                                                                        |
| start_time    | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).  The starting timestamp from which CVD calculation begins.                  |
| end_time      | integer | NO        | 
End timestamp in milliseconds (e.g., 1641522717000).                                                                              |
| unit          | string  | NO        | Unit for the returned data, choose between 'usd' or 'coin'.  Default: 'usd'                                                        |


**Response Data:**

```json
{
  "code": "0",
  "data": [
    {
      "time": 1762254000000,
      "agg_taker_buy_vol": 461937243.0899,
      "agg_taker_sell_vol": 415687343.2719,
      "cum_vol_delta": 46249899.818
    },
    {
      "time": 1762257600,
      "agg_taker_buy_vol": 390296231.4588,
      "agg_taker_sell_vol": 469137635.9107,
      "cum_vol_delta": -32591504.6339
    },
    {
      "time": 1762261200,
      "agg_taker_buy_vol": 461378798.1884,
      "agg_taker_sell_vol": 450407935.7885,
      "cum_vol_delta": -21620642.234
    },
  ]
}
```

