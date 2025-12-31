# Futures - Liquidation - Coin Liquidation Map


```
GET /api/futures/liquidation/aggregated-map
```


This endpoint provides a mapped visualization of aggregated liquidation events for coins, calculated based on market data and liquidation leverage levels.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ❌        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description                                                                       |
| ------ | ------ | --------- | --------------------------------------------------------------------------------- |
| symbol | string | YES       | Trading coin (e.g., BTC). Retrieve supported coins via the 'supported-coins' API. |
| range  | string | YES       | Time range for data aggregation. Supported values: 1d, 7d, 30d.                   |


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
          null,
          null
        ]
      ],
      ...  
    }
  }
}
```

