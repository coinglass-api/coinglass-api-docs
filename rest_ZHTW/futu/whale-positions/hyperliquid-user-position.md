# 合約數據 - Hyperliquid 倉位 - Hyperliquid 使用者倉位


```
GET /api/hyperliquid/user-position
```


該接口提供 Hyperliquid 使用者持倉資料，包括 保證金、可提現餘額 以及 目前持有的資產倉位。

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "data": {
    "margin_summary": {
      "account_value": 179250588.896754,
      "total_ntl_pos": 679947383.29435,
      "total_raw_usd": -500696794.397596,
      "total_margin_used": 131236726.65887
    },
    "cross_margin_summary": {
      "account_value": 179250588.896754,
      "total_ntl_pos": 679947383.29435,
      "total_raw_usd": -500696794.397596,
      "total_margin_used": 131236726.65887
    },
    "cross_maintenance_margin_used": 19278725.276478,
    "withdrawable": 46429612.237884,
    "asset_positions": [
      {
        "type": "oneWay",
        "position": {
          "coin": "BTC",
          "szi": 1000,
          "leverage": {
            "type": "cross",
            "value": 5
          },
          "entry_px": 91506.7,
          "position_value": 86265000,
          "unrealized_pnl": -5643767.29312,
          "return_on_equity": -0.3083797767,
          "max_leverage": 5,
          "cum_funding": {
            "all_time": -104732.177706,
            "since_open": 87958.233078,
            "since_change": 84811.539668
          }
        }
      },
      }
    ]
  }
}
```

 **Parameters:**
| 名称           | 类型     | 必填  | 描述    |
| ------------ | ------ | --- | ----- |
| user_address | string | YES | 使用者位址 |

