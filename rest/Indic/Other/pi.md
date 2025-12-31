# Indic - Other - Pi Cycle Top Indicator


```
GET /api/index/pi-cycle-indicator
```


This endpoint provides data for the Pi Cycle Top Indicator, including the 111-day moving average (ma110), the 350-day moving average multiplied by 2 (ma350Mu2), and the price at specific timestamps.

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
      "ma_110": 0.07,                     // 110-day moving average price
      "timestamp": 1282003200000,        // Timestamp (milliseconds)
      "ma_350_mu_2": 0.14,               // 2x value of 350-day moving average
      "price": 0.07                      // Daily price
    },
    {
      "ma_110": 0.069,                   // 110-day moving average price
      "timestamp": 1282089600000,        // Timestamp (milliseconds)
      "ma_350_mu_2": 0.138,              // 2x value of 350-day moving average
      "price": 0.068                     // Daily price
    }
  ]
}

```

