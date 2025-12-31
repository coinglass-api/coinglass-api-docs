# Indic - Other - Bitcoin Profitable Days


```
GET /api/index/bitcoin/profitable-days
```


This endpoint provides data for the Bitcoin Profitable Days

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
      "side": 1,                              // Trade direction, 1 represents buy, 0 represents sell
      "timestamp": 1282003200000,             // Timestamp (in milliseconds)
      "price": 0.07                           // Price
    },
    {
      "timestamp": 1282089600000,             // Timestamp (in milliseconds)
      "price": 0.068,                         // Price
      "side": 1                               // Trade direction, 1 represents buy, 0 represents sell
    }
  ]
}

```

