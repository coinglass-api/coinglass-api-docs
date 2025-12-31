# Spots - Trading market - Supported Coins


```
GET /api/spot/supported-coins
```


This endpoint allows you to query all the supported spot coins on CoinGlass.

***Cache / Update Frequency:*** every 1 minutes for all the API plans.

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
    "BTC",
    "ETH",
    "USDT",
    "BNB",
    "SOL",
    "USDC",
    ...
  ]
}
```

