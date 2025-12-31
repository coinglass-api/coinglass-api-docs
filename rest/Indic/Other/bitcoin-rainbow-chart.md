# Indic - Other - Bitcoin-Rainbow-Chart


```
GET /api/index/bitcoin/rainbow-chart
```


This endpoint provides data for the Bitcoin Rainbow Chart

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
    [
      0.07,                                 // Current price
      0.033065,                             // Minimum value of shadow
      0.044064,                             // First layer
      0.059892,                             // Second layer
      0.082219,                             // Third layer
      0.110996,                             // Fourth layer
      0.149845,                             // Fifth layer
      0.205865,                             // Sixth layer
      0.283454,                             // Seventh layer
      0.380525,                             // Eighth layer
      0.517626,                             // Ninth layer
      1282003200000                        // Timestamp
    ]
  ]
}

```

