# 合約數據 - 持倉 - 幣種交易所持倉歷史


```
GET /api/futures/open-interest/exchange-history-chart
```


該接口用於獲取某一加密貨幣在多個交易所的歷史持倉量數據，適用於圖表展示。

***快取 / 更新頻率:***  每 10 秒鐘更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版    | 創業版      | 標準版 | 專業版 | 企業版 |
| :----- | :----- | :------- | :-- | :-- | :-- |
| 可用性    | ✅      | ✅        | ✅   | ✅   | ✅   |
| 颗粒度    | `>=4h` | ​`>=30m` | 無限制 | 無限制 | 無限制 |

### 回應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": {
    "time_list": [1721649600000, ...], // 時間戳列表（毫秒）
    "price_list": [67490.3, ...], // 價格列表（與 time_list 對應）

    "data_map": { // 各交易所未平倉合約資料
      "Binance": [8018229234, ...], // Binance 未平倉合約（與 time_list 對應）
      "Bitmex": [395160842, ...] // BitMEX 未平倉合約（與 time_list 對應）
      // ...
    }
  }
}

```

 **Parameters:**
| 名称     | 类型     | 必填  | 描述                                         |
| ------ | ------ | --- | ------------------------------------------ |
| symbol | string | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。 |
| range  | string | YES | 數據時間間隔。支持的取值包括 ：all，1m，15m，1h，4h，12h       |
| unit   | string | NO  | 返回數據的單位，可選值為 'usd' 或 'coin'。               |

