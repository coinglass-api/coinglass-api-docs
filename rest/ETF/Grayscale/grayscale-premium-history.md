# ETF - Grayscale - Premium History


```
GET /api/grayscale/premium-history
```


This endpoint provides historical premium/discount data for Grayscale Investment Trusts relative to their NAV.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ✅        | ✅       | ✅        | ✅            | ✅          |

# Respones Data

```json
{
  "code": "0",
  "msg": "success",
  "data": [
     {
      "primary_market_price": [     // Primary market price list
        0.14,
        0.14
        // ...
      ],
      "date_list": [                // Date list (timestamps)
        1380171600000,
        1380258000000
        // ...
      ],
      "secondary_market_price_list": [  // Secondary market price list
        0.57,
        0.53
        // ...
      ],
      "premium_rate_list": [          // Premium rate list
        19.37,
        15.59
        // ...
      ]
    },
      ....
  ]
}

```

 **Parameters:**
| Name   | Type   | Mandatory | Description                                                                    |
| ------ | ------ | --------- | ------------------------------------------------------------------------------ |
| symbol | string | YES       | Supported values: ETC, LTC, BCH, SOL, XLM, LINK, ZEC, MANA, ZEN, FIL, BAT, LPT |

