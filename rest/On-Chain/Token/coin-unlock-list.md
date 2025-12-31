# On-Chain - Token - Token Unlock List


```
GET /api/coin/unlock-list
```


This endpoint returns token unlock data and upcoming unlock schedules.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |

<br />

```json
{
  "code": "0", // response code
  "data": [ // token list
    {
      "symbol": "GT", // token symbol
      "name": "GateToken", // token name
      "symbol_logo_url": "https://cdn.coinglasscdn.com/static/img/coins/gt.jpg", // logo url
      "price": 10.377, // last price
      "price_change_percent_24h": 2.67, // 24h change %
      "market_cap": 1217683606.698, // market cap
      "total_supply": 300000000, // total supply
      "fully_diluted_valuation": 3115642754.097, // FDV
      "total_locked": 74868300, // locked tokens
      "circulating_supply": 117344474, // circulating supply
      "total_unlocked": 162691500, // unlocked tokens
      "next_unlock_date": 1765152000000, // next unlock time
      "next_unlock_tokens": 48600, // next unlock amount
      "next_unlock_of_circulating": 0.041416522093745974, // % of circulating
      "next_unlock_of_supply": 0.0162 // % of total supply
    },
    ....
  ]
}

```

 **Parameters:**
| Name     | Type    | Mandatory | Description                             |
| -------- | ------- | --------- | --------------------------------------- |
| per_page | integer | NO        | Number of results per page.             |
| page     | integer | NO        | Page number for pagination, default: 1. |

