# Futures - Trading Market - Supported Exchange and Pairs


```
GET /api/futures/supported-exchange-pairs
```


Check the supported exchange and trading pairs in the API documentation

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
  "msg": "success",
  "data": {
    "Binance": [ // exchange name
      {
        "instrument_id": "BTCUSD_PERP",// futures pair
        "base_asset": "BTC",// base asset
        "quote_asset": "USD"// quote asset
      },
      {
        "instrument_id": "BTCUSD_250627",
        "base_asset": "BTC",
        "quote_asset": "USD"
      },
      ....
      ],
    "Bitget": [
      {
        "instrument_id": "BTCUSDT_UMCBL",
        "base_asset": "BTC",
        "quote_asset": "USDT"
      },
      {
        "instrument_id": "ETHUSDT_UMCBL",
        "base_asset": "ETH",
        "quote_asset": "USDT"
      },
      ...
      ]
      ...
   }
}
```

 **Parameters:**
| Name     | Type   | Mandatory | Description                                                                   |
| -------- | ------ | --------- | ----------------------------------------------------------------------------- |
| exchange | string | NO        | Filters the results to return only trading pairs from the specified exchange. |

