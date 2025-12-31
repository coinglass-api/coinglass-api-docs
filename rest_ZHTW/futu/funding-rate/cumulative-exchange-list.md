# 合約數據 - 資金費率 - 累計資金費率－交易所列表


```
GET /api/futures/funding-rate/accumulated-exchange-list
```


該接口提供各交易所的幣種累計資金費率數據。

***快取 / 更新頻率:*** 每 1小時更新一次

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
      "stablecoin_margin_list": [ // USDT/USD 保證金模式的累計資金費率
        {
          "exchange": "BINANCE", // 交易所名稱
          "funding_rate": 0.001873 // 累計資金費率
        },
        {
          "exchange": "OKX", // 交易所名稱
          "funding_rate": 0.00775484 // 累計資金費率
        }
      ],
      "token_margin_list": [ // 幣本位保證金模式的累計資金費率
        {
          "exchange": "BINANCE", // 交易所名稱
          "funding_rate": -0.003149 // 累計資金費率
        }
      ]
    }
  ]
}

```

 **Parameters:**
| 名称    | 类型     | 必填  | 描述                               |
| ----- | ------ | --- | -------------------------------- |
| range | string | YES | 資料時間間隔。支援的取值包括：1d, 7d, 30d, 365d |

