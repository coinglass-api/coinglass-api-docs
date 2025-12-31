# Futures - Trading Market - Supported Coins


```
GET /api/futures/supported-coins
```


This endpoint allows you to query all the supported coins on CoinGlass

***Cache / Update Frequency:*** every 1 minutes for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |

##

**Response Data:**

```json
{
  "code": "0",
  "msg": "success",
  "data": [
      "BTC",
      "ETH",
      "SOL",
      "XRP",
      ...
  ]
}
```

