# Futures - Long-Short Ratio - Net Position (v2)


```
GET /api/futures/v2/net-position/history
```


This endpoint provides the historical net position data for futures, including the net_long_change and net_short_change values.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name       | Type    | Mandatory | Description                                                                                             |
| ---------- | ------- | --------- | ------------------------------------------------------------------------------------------------------- |
| exchange   | string  | YES       | Currently available for Binance exchange only.                                                          |
| symbol     | string  | YES       | Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'supported-exchange-pair' API.           |
| interval   | string  | YES       | Time interval for data aggregation. Supported values: 1m, 3m, 5m, 15m, 30m, 1h, 4h, 6h, 8h, 12h, 1d, 1w |
| limit      | integer | NO        | Number of results per request. Default: 1000, Maximum: 1000                                             |
| start_time | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                  |
| end_time   | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                    |


**Response Data:**

```json
{
  "code": "0",
  "data": [
    {
      "net_long_change": -478.43,
      "net_short_change": 0,
      "time": 1751652000000
    },
    {
      "net_long_change": -776.79,
      "net_short_change": 0,
      "time": 1751655600000
    },
}
```

