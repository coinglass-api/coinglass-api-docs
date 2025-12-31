# 現貨 - 訂單簿 - 大額訂單簿


```
GET /api/spot/orderbook/large-limit-order
```


該接口提供現貨交易中當前訂單簿中的大額限價掛單數據。

***快取 / 更新頻率:*** 即時更新.

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
      "id": 2536823422,
      "exchange_name": "Binance",            // 交易所名稱
      "symbol": "BTCUSDT",                   // 交易對
      "base_asset": "BTC",                   // 基礎幣種
      "quote_asset": "USDT",                 // 計價幣種

      "limit_price": 56932,                  // 委託價格
      "start_time": 1722964242000,           // 委託開始時間（毫秒）
      "start_quantity": 28.39774,            // 初始數量
      "start_usd_value": 1616740.1337,       // 初始價值（USD）

      "current_quantity": 18.77405,          // 當前剩餘數量
      "current_usd_value": 1068844.21,       // 當前剩餘價值（USD）
      "current_time": 1722964272000,         // 當前時間（毫秒）

      "executed_volume": 0,                  // 成交數量
      "executed_usd_value": 0,               // 成交價值（USD）
      "trade_count": 0,                      // 成交筆數

      "order_side": 2,                       // 委託方向：1-賣單，2-買單
      "order_state": 1                       // 委託狀態：1-掛單中，2-已完成，3-已撤銷
    }
  ]
}

```

 **Parameters:**
| 名称       | 类型     | 必填  | 描述                                                           |
| -------- | ------ | --- | ------------------------------------------------------------ |
| exchange | string | YES | 交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。  |
| symbol   | string | YES | 交易對（例如：BTCUSDT）。可透過 support-exchange-pair 接口查詢支持的交易對。        |

