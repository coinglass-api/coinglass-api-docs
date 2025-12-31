# Futures - Liquidation - Pair Liquidation Map


```
GET /api/futures/liquidation/map
```


This endpoint provides a mapped visualization of liquidation events for trading pairs, calculated based on market data and liquidation leverage levels.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ❌        | ✅            | ✅          |


 **Parameters:**
| Name     | Type   | Mandatory | Description                                                                                        |
| -------- | ------ | --------- | -------------------------------------------------------------------------------------------------- |
| exchange | string | YES       | Exchange name (e.g., Binance). Retrieve supported exchanges via the 'supported-exchange-pair' API. |
| symbol   | string | YES       | Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'supported-exchange-pair' API.      |
| range    | string | YES       | Time range for data aggregation. Supported values: 1d, 7d, 30d.                                    |


**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": 
  {
    "data": 
    {
      "48935": //liquidation price
      [
        [
          48935,//liquidation price
          1579370.77,//Liquidation Level
          25,//Leverage Ratio
          null
        ]
      ],
      ...  
    }
  }
}
```

