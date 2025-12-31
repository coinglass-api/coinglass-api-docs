# 合约 - 多空比 - 币种主动买卖比


```
GET /api/futures/taker-buy-sell-volume/exchange-list
```


该接口提供聚合多个交易所中币种的主动买卖成交量比数据。

***缓存 / 更新频率:*** 1秒钟一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": {
    "symbol": "BTC", // 币种
    "buy_ratio": 51.01, // 买入比例（%）
    "sell_ratio": 48.99, // 卖出比例（%）
    "buy_vol_usd": 1112108532.1688, // 总买入金额（美元）
    "sell_vol_usd": 1068220541.0417, // 总卖出金额（美元）
    "exchange_list": [ // 各个交易所的买卖数据
      {
        "exchange": "Binance", // 交易所名称
        "buy_ratio": 49.22, // 买入比例（%）
        "sell_ratio": 50.78, // 卖出比例（%）
        "buy_vol_usd": 240077939.5811, // 买入金额（美元）
        "sell_vol_usd": 247674925.1653 // 卖出金额（美元）
      },
      {
        "exchange": "OKX", // 交易所名称
        "buy_ratio": 50.84, // 买入比例（%）
        "sell_ratio": 49.16, // 卖出比例（%）
        "buy_vol_usd": 108435724.6214, // 买入金额（美元）
        "sell_vol_usd": 104834502.5904 // 卖出金额（美元）
      }
    ]
  }
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                          |
| ------ | ------ | --- | ------------------------------------------- |
| symbol | string | YES | 交易币种（例如：BTC）。可通过 support-coins 接口获取支持的币种列表。 |
| range  | string | YES | 数据的时间范围（例如：5m、15m、30m、1h、4h、12h、24h）。       |

