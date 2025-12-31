# 合约 - Hyperliquid 仓位 - Hyperliquid 用户仓位


```
GET /api/hyperliquid/user-position
```


该接口提供 Hyperliquid 用户持仓数据，包括 保证金、可提现余额以及当前持有的资产仓位。

***缓存 / 更新频率:*** 实时.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

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
| 名称           | 类型     | 必填  | 描述   |
| ------------ | ------ | --- | ---- |
| user_address | string | YES | 用户地址 |

