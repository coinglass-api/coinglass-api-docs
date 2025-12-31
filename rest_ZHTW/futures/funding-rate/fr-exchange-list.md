# 合約數據 - 資金費率 - 幣種資金費率－交易所列表


```
GET /api/futures/funding-rate/exchange-list
```


該接口提供各交易所的幣種資金費率數據。

***快取 / 更新頻率:*** 每 10 秒鐘更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版    | 創業版      | 標準版 | 專業版 | 企業版 |
| :----- | :----- | :------- | :-- | :-- | :-- |
| 可用性    | ✅      | ✅        | ✅   | ✅   | ✅   |
| 颗粒度    | `>=4h` | ​`>=30m` | 無限制 | 無限制 | 無限制 |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "symbol": "BTC", // 幣種
      "stablecoin_margin_list": [ // USDT/USD 保證金模式
        {
          "exchange": "Binance", // 交易所
          "funding_rate_interval": 8, // 資金費率結算週期（小時）
          "funding_rate": 0.007343, // 當前資金費率
          "next_funding_time": 1745222400000 // 下次資金費率結算時間（毫秒）
        },
        {
          "exchange": "OKX", // 交易所
          "funding_rate_interval": 8, // 資金費率結算週期（小時）
          "funding_rate": 0.00736901950628, // 當前資金費率
          "next_funding_time": 1745222400000 // 下次資金費率結算時間（毫秒）
        }
      ],
      "token_margin_list": [ // 幣本位保證金模式
        {
          "exchange": "Binance", // 交易所
          "funding_rate_interval": 8, // 資金費率結算週期（小時）
          "funding_rate": -0.001829, // 當前資金費率
          "next_funding_time": 1745222400000 // 下次資金費率結算時間（毫秒）
        }
      ]
    }
  ]
}

```

