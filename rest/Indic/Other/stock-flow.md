# Indic - Other - Stock-to-Flow Model


```
GET /api/index/stock-flow
```


This endpoint provides data for the Stock-to-Flow model, including the price and the number of days remaining until the next halving event for specific timestamps.

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
      "timestamp": 1282003200000,       // Timestamp (in milliseconds)
      "price": 0.07,                     // Price on the given day
      "next_halving": 834               // Days remaining until the next halving
    },
    {
      "timestamp": 1282089600000,       // Timestamp (in milliseconds)
      "price": 0.068,                    // Price on the given day
      "next_halving": 833               // Days remaining until the next halving
    }

  ]
}

```

