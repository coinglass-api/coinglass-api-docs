# Indic - Other - Tow Year Ma Multiplier


```
GET /api/index/2-year-ma-multiplier
```


This endpoint provides data for the Tow Year Ma Multiplier

***Cache / Update Frequency:*** every day for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |



**Response Data:**

```json
{
  "code": "0",                              
  "msg": "success",                         
  "data": [
    {
      "timestamp": 1282003200000,               // Timestamp (in milliseconds)
      "price": 0.07,                            // Current price
      "moving_average_730": 0.07,               // 2-year moving average (730 represents the period)
      "moving_average_730_multiplier_5": 0.35000000000000003, // 5 times the 2-year moving average (Multiplier)
    }
  ]
}

```

