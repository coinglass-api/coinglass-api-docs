# On-Chain - Exchange data - Exchange Balance Chart


```
GET /api/exchange/balance/chart
```


This endpoint provides historical chart data of exchange asset balances over time, along with corresponding price data.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description               |
| ------ | ------ | --------- | ------------------------- |
| symbol | string | YES       | Trading coin eg. BTC, ETH |


**Response Data:**

```json
{
  "code": "0",                                 
  "msg": "success",                            
  "data": [
    {
      "time_list": [1691460000000, ...],       // Array of timestamps (in milliseconds)
      "price_list": [29140.9, ...],            // Array of prices corresponding to each timestamp
      "data_map": {                            // Balance data by exchange
        "huobi": [15167.03527, ...],           // Balance data from Huobi exchange
        "gate": [23412.723, ...],              // Balance data from Gate exchange
        ...
      }
    }
  ]
}

```

