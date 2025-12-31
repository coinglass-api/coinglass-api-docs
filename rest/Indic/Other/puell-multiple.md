# Indic - Other - Puell-Multiple


```
GET /api/index/puell-multiple
```


This endpoint provides the Puell-Multiple index, which includes data on buy and sell quantities, the price, and the Puell-Multiple value at specific timestamps.

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
      "timestamp": 1282003200000,           // Timestamp (in milliseconds)
      "price": 0.07,                         // Price on the given day
      "puell_multiple": 1                   // Puell Multiple value
    },
    {
      "timestamp": 1282089600000,           // Timestamp (in milliseconds)
      "price": 0.068,                        // Price on the given day
      "puell_multiple": 1.0007745933384973  // Puell Multiple value
    }
    ...
  ]
}

```

