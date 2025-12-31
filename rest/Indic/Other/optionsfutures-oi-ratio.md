# Indic - Other - Options/Futures OI Ratio


```
GET /api/index/option-vs-futures-oi-ratio
```


This endpoint provides data for the options/futures oi ratio

***Cache / Update Frequency:*** 1 day for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |

<br />

**Response Data**

```json
{
  "code": "0",
  "data": [
    {
      "btc_option_vs_futures_radio": 45.1,
      "eth_option_vs_futures_radio": 21.92,
      "timestamp": 1592956800000
    },
    {
      "btc_option_vs_futures_radio": 45.15,
      "eth_option_vs_futures_radio": 23.16,
      "timestamp": 1593043200000
    },
    {
      "btc_option_vs_futures_radio": 47.27,
      "eth_option_vs_futures_radio": 23.65,
      "timestamp": 1593129600000
    },
}

```

