# ETF - 灰度基金 - 灰度溢价历史


```
GET /api/grayscale/premium-history
```


该接口提供灰度投资信托（如GBTC、ETHE等）相对于其净值（NAV）的历史溢价或折价率数据。

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "primary_market_price": [     // 一级市场价格列表
        0.14,
        0.14
        // ...
      ],
      "date_list": [                // 日期列表（时间戳）
        1380171600000,
        1380258000000
        // ...
      ],
      "secondary_market_price_list": [  // 二级市场价格列表
        0.57,
        0.53
        // ...
      ],
      "premium_rate_list": [          // 溢价率列表
        19.37,
        15.59
        // ...
      ]
    },
    // 其他数据项...
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                                                   |
| ------ | ------ | --- | -------------------------------------------------------------------- |
| symbol | string | YES | 支持的币种 : ETC, LTC, BCH, SOL, XLM, LINK, ZEC, MANA, ZEN, FIL, BAT, LPT |

