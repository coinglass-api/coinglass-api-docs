# Indic - Other - Bitcoin Short Term Holder Realized Price


```
GET /api/index/bitcoin-sth-realized-price
```


This endpoint provides data for the bitcoin short term holder realized price

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
      "timestamp": 1325376000000,
      "price": 4.61211781,
      "sth_realized_price": 4.8958766225
    },
    {
      "timestamp": 1325462400000,
      "price": 5.13201225,
      "sth_realized_price": 4.8806352365
    },
    {
      "timestamp": 1325548800000,
      "price": 5.21773083,
      "sth_realized_price": 4.8736945702
    },
}

```

