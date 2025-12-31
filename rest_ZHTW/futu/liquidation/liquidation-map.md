# 合約數據 - 爆倉與清算 - 交易對清算地圖


```
GET /api/futures/liquidation/map
```


該接口提供交易對清算地圖數據。

***快取 / 更新頻率:*** 即時更新.

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ❌   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": {
    "data": {
      "48935": [
        [
          48935, // 清算價格
          1579370.77, // 清算強度
          25, // 杠杆倍數
          "h2"
        ]
      ]
    }
  }
}

```

 **Parameters:**
| 名称       | 类型     | 必填  | 描述                                                           |
| -------- | ------ | --- | ------------------------------------------------------------ |
| exchange | string | YES | 交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。  |
| symbol   | string | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。                   |
| range    | string | YES | 數據時間間隔。支持的取值包括：1d,7d,30d                                     |

