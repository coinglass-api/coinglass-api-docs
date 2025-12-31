# Indic - Other - Crypto Fear & Greed Index


```
GET /api/index/fear-greed-history
```


This endpoint provides data for the Crypto Fear & Greed Index

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
      "data_list": [4611285.1141, ...],         // Fear and Greed Index values
      "price_list": [4788636.51145, ...],         // Corresponding price data
      "time_list": [1636588800, ...]        // Timestamps
    }
  ]
}

```

