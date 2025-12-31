# Futures - Open Interest - Exchange History Chart


```
GET /api/futures/open-interest/exchange-history-chart
```


This endpoint retrieves historical open interest data for a specific cryptocurrency across exchanges, formatted for chart display.

***Cache / Update Frequency:*** 10 second for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |

<br />


 **Parameters:**
| Name   | Type   | Mandatory | Description                                                                         |
| ------ | ------ | --------- | ----------------------------------------------------------------------------------- |
| symbol | string | YES       | Trading coin (e.g., BTC).  Check supported coins through the 'supported-coins' API. |
| range  | string | YES       | Time range for the data (e.g., all, 1m, 15m, 1h, 4h, 12h).                          |
| unit   | string | NO        | Unit for the returned data, choose between 'usd' or 'coin'.                         |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": {
    "time_list": [1721649600000, ...], // List of timestamps (in milliseconds)
    "price_list": [67490.3, ...], // List of prices corresponding to each timestamp

    "data_map": { // Open interest data of futures from each exchange
      "Binance": [8018229234, ...], // Binance open interest (corresponds to time_list)
      "Bitmex": [395160842, ...] // BitMEX open interest (corresponds to time_list)
      // ...
    }
  }
}

```

