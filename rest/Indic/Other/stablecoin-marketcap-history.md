# Indic - Other - StableCoin MarketCap History


```
GET /api/index/stableCoin-marketCap-history
```


This endpoint provides data for the StableCoin MarketCap History

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
      "data_list": [4611285.1141, ...],         // List of values
      "price_list": [, ...],                    // List of prices
      "time_list": [1636588800, ...]            // List of timestamps
    }
  ]
}

```

