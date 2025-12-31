# ETF - 灰度基金 - 灰度溢價歷史


```
GET /api/grayscale/premium-history
```


該接口提供灰度投資信託（如 GBTC、ETHE 等）相對於其淨值（NAV）的歷史溢價或折價率數據。

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "primary_market_price": [     // 一級市場價格列表
        0.14,
        0.14
        // ...
      ],
      "date_list": [                // 日期列表（時間戳）
        1380171600000,
        1380258000000
        // ...
      ],
      "secondary_market_price_list": [  // 二級市場價格列表
        0.57,
        0.53
        // ...
      ],
      "premium_rate_list": [          // 溢價率列表
        19.37,
        15.59
        // ...
      ]
    },
    // 其他資料項...
  ]
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                                                   |
| ------ | ------ | --- | -------------------------------------------------------------------- |
| symbol | string | YES | 支持的幣種。: ETC, LTC, BCH, SOL, XLM, LINK, ZEC, MANA, ZEN, FIL, BAT, LPT |

