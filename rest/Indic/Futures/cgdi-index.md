# Indic - Futures - CGDI Index


```
GET /api/futures/cgdi-index/history  
```


This endpoint provides historical CGDI (CoinGlass Derivatives Index) data

***Cache / Update Frequency:*** every 1 minutes for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |

<br />

**Response Data**

```json
{
  "code": "0",
  "data": [
    {
      "time": 1704067200000,
      "cgdi_index_value": 1000
    },
    {
      "time": 1704153600000,
      "cgdi_index_value": 1053.2551
    },
  ]
}

```

