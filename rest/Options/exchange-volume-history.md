# Options - Exchange Volume History


```
GET /api/option/exchange-vol-history
```


This endpoint provides historical trading volume data for options across different exchanges

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name   | Type   | Mandatory | Description                                                                                                                                                     |
| ------ | ------ | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| symbol | string | YES       | Trading coin (e.g., BTC,ETH).                                                                                                                                   |
| unit   | string | YES       | Specify the unit for the returned data. Supported values depend on the symbol. If symbol is BTC, choose between USD or BTC. For ETH, choose between USD or ETH. |


**Response Data:**

```json
{
  "code": "0",                                
  "msg": "success",                            
  "data": [
    {
      "time_list": [1691460000000, ...],       // Array of timestamps (in milliseconds)
      "price_list": [29140.9, ...],            // Array of prices corresponding to each timestamp
      "data_map": {                            // Volume data by exchange
        "huobi": [15167.03527, ...],           // Volume data from Huobi exchange
        "gate": [23412.723, ...],              // Volume data from Gate exchange
        ...
      }
    }
  ]
}

```

