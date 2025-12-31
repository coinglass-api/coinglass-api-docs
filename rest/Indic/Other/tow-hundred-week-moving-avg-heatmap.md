# Indic - Other - 200-Week Moving Avg Heatmap


```
GET /api/index/200-week-moving-average-heatmap
```


This endpoint provides data for the 200-Week Moving Avg Heatmap

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
      "timestamp": 1325203200000,          // Timestamp (in milliseconds)
      "price": 4.31063509000584,           // Current price
      "moving_average_1440": 4.143619070636635, // 200-week moving average (1440 represents the period)
      "moving_average_1440_ip": 0,         // Position of the moving average (IP indicator)
    }
  ]
}

```

