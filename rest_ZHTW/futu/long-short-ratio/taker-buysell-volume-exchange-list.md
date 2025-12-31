# 合約數據 - 多空比 - 幣種主動買賣比


```
GET /api/futures/taker-buy-sell-volume/exchange-list
```


該接口提供聚合多個交易所中幣種的主動買賣成交量比數據。

***快取 / 更新頻率:*** 每 1 秒鐘更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": {
    "symbol": "BTC", // 幣種
    "buy_ratio": 51.01, // 買入比例（%）
    "sell_ratio": 48.99, // 賣出比例（%）
    "buy_vol_usd": 1112108532.1688, // 總買入金額（美元）
    "sell_vol_usd": 1068220541.0417, // 總賣出金額（美元）
    "exchange_list": [ // 各個交易所的買賣資料
      {
        "exchange": "Binance", // 交易所名稱
        "buy_ratio": 49.22, // 買入比例（%）
        "sell_ratio": 50.78, // 賣出比例（%）
        "buy_vol_usd": 240077939.5811, // 買入金額（美元）
        "sell_vol_usd": 247674925.1653 // 賣出金額（美元）
      },
      {
        "exchange": "OKX", // 交易所名稱
        "buy_ratio": 50.84, // 買入比例（%）
        "sell_ratio": 49.16, // 賣出比例（%）
        "buy_vol_usd": 108435724.6214, // 買入金額（美元）
        "sell_vol_usd": 104834502.5904 // 賣出金額（美元）
      }
    ]
  }
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                         |
| ------ | ------ | --- | ------------------------------------------ |
| symbol | string | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。 |
| range  | string | YES | 數據時間間隔。支持的取值包括：5m、15m、30m、1h、4h、12h、24h    |

