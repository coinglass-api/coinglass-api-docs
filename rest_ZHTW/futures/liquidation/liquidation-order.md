# 合約數據 - 爆倉與清算 - 爆倉訂單


```
GET /api/futures/liquidation/order
```


該接口提供過去 7 天內的爆倉訂單數據，包含交易所、交易對及爆倉金額等詳細數據。

***快取 / 更新頻率:*** 每 1 秒鐘更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "exchange_name": "BINANCE", // 交易所名稱
      "symbol": "BTCUSDT",       // 交易對
      "base_asset": "BTC",       // 幣種
      "price": 87535.9,          // 爆倉價格
      "usd_value": 205534.2932,  // 成交金額（美元）
      "side": 2,                 // 訂單方向（1：買入，2：賣出）
      "time": 1745216319263      // 時間戳（毫秒）
    },
    {
      "exchange_name": "BINANCE",
      "symbol": "BTCUSDT",
      "base_asset": "BTC",
      "price": 87465.2,
      "usd_value": 15918.6664,
      "side": 2,
      "time": 1745215647165
    }
  ]
}

```

 **Parameters:**
| 名称                     | 类型      | 必填  | 描述                                                           |
| ---------------------- | ------- | --- | ------------------------------------------------------------ |
| exchange               | string  | YES | 交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。  |
| symbol                 | string  | YES | 交易幣種（例如：BTC）。透過 support-coins API 獲取支持的幣種。                   |
| min_liquidation_amount | string  | YES | 爆倉訂單的最小金額閾值。每個請求最多返回 200 條記錄                                 |
| start_time             | integer | NO  | 起始時間戳，單位為毫秒（例如：1746776387000）。                               |
| end_time               | integer | NO  | 結束時間戳，單位為毫秒（例如：1746776587000）。                               |

