# Spots - Order book - Orderbook Heatmap


```
GET /api/spot/orderbook/history
```


This endpoint provides historical order book depth data for spot trading, supporting heatmap visualization.

***Cache / Update Frequency:*** Real time for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ❌       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name       | Type   | Mandatory | Description                                                                                                               |
| ---------- | ------ | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| exchange   | string | YES       | Spot exchange names (e.g., Binance, OKX) .Retrieve supported exchanges via the 'supported-exchange-pair' API.             |
| symbol     | string | YES       | Trading pair (e.g., BTCUSDT). Retrieve supported pairs via the 'supported-exchange-pair' API.                             |
| interval   | string | YES       | Time intervals for data aggregation. Supported values: 1m、3m、5m、15m、30m、1h、4h、6h、8h、12h、1d.                               |
| limit      | string | NO        | Number of results per request. Default: 100, Maximum: 100.  Historical range – 1m: 3 days, 5m: 15 days, others: 150 days. |
| start_time | string | NO        | Start timestamp in milliseconds (e.g., 1641522717000).                                                                    |
| end_time   | string | NO        | End timestamp in milliseconds (e.g., 1641522717000).                                                                      |


**Response Data:**

```json
{
    "code": "0",
    "msg": "success",
    "data": [
        [
            1723611600,
            [
                [
                    56420, //Price
                    4.777 //Quantity
                ],
                [
                    40300,
                    2.191
                ]
            ],
            [
                [
                    56420,
                    4.777
                ],
                [
                    40300,
                    2.191
                ]
            ]
        ]
    ],
    "success": true
}
```

