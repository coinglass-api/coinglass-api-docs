# Futures - Liquidation - Liquidation Max Pain


```
GET /api/futures/liquidation/max-pain
```


This endpoint provides key liquidation “max-pain” price for major cryptocurrencies, indicating potential pressure zones between current and liquidation prices.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ❌        | ✅            | ✅          |


 **Parameters:**
| Name  | Type   | Mandatory | Description                                                                           |
| ----- | ------ | --------- | ------------------------------------------------------------------------------------- |
| range | string | NO        | Time interval for data aggregation. Supported values: 12h, 24h, 48h, 3d, 7d, 14d, 30d |


**Response Data:**

```json
{
  "code": "0",
  "data": [
    {
      "symbol": "BTC",
      "price": 110625.1, //symbol price
      "long_max_pain_liq_level": 75677278.26,//long max pain liquidation level
      "long_max_pain_liq_price": 113046.71, //long max pain luquidation price
      "short_max_pain_liq_level": 44617473.19,
      "short_max_pain_liq_price": 109748.37
    
    {
      "symbol": "ETH",
      "price": 3914.14,
      "long_max_pain_liq_level": 34406421.23,
      "long_max_pain_liq_price": 3955.722,
      "short_max_pain_liq_level": 44375943.61,
      "short_max_pain_liq_price": 3820.002
    },
    {
      "symbol": "SOL",
      "price": 195.1,
      "long_max_pain_liq_level": 12467317.12,
      "long_max_pain_liq_price": 199.468,
      "short_max_pain_liq_level": 12927647.29,
      "short_max_pain_liq_price": 190.186
    },
    ....
  ]
}

```

