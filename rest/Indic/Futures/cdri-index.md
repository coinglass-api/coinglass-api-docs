# Indic - Futures - CDRI Index


```
GET /api/futures/cdri-index/history 
```


This endpoint provides historical CDRI (CoinGlass Derivatives Risk Index) data.

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
      "time": 1646438400000,
      "cdri_index_value": 50
    },
    {
      "time": 1646524800000,
      "cdri_index_value": 47
    },
  ]
}

```

