# 現貨 - 訂單簿 - 大額訂單簿歷史


```
GET /api/spot/orderbook/large-limit-order-history
```


該接口提供現貨交易中已完成的大額限價掛單的歷史數據。

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
      "id": 2895605135,
      "exchange_name": "Binance",               // 交易所名稱
      "symbol": "BTCUSDT",                      // 交易對
      "base_asset": "BTC",                      // 基礎幣種
      "quote_asset": "USDT",                    // 計價幣種
      "price": 89205.9,                         // 委託價格
      "start_time": 1745287309000,              // 委託開始時間 (毫秒)
      "start_quantity": 25.779,                 // 初始委託數量
      "start_usd_value": 2299638.8961,          // 初始委託價值 (USD)
      "current_quantity": 25.779,               // 當前剩餘數量
      "current_usd_value": 2299638.8961,        // 當前剩餘價值 (USD)
      "current_time": 1745287309000,            // 當前時間 (毫秒)
      "executed_volume": 0,                     // 累計成交量
      "executed_usd_value": 0,                  // 累計成交價值 (USD)
      "trade_count": 0,                         // 累計成交筆數
      "order_side": 1,                          // 委託方向：1-賣單，2-買單
      "order_state": 2,                         // 委託狀態：0-未開始，1-掛單中，2-已完成，3-已撤銷
      "order_end_time": 1745287328000           // 完成或撤銷訂單的結束時間 (毫秒)
    },
    ...
  ]
}

```

 **Parameters:**
| 名称         | 类型     | 必填  | 描述                                                           |
| ---------- | ------ | --- | ------------------------------------------------------------ |
| exchange   | string | YES | 交易所名稱（例如：Binance、OKX）。可透過 support-exchange-pair 接口獲取支持的交易所。  |
| symbol     | string | YES | 交易對（例如：BTCUSDT）。可透過 support-exchange-pair 接口查詢支持的交易對。        |
| start_time | string | YES | 起始時間戳，單位為毫秒（例如：1746776387000）。                               |
| end_time   | string | YES | 結束時間戳，單位為毫秒（例如：1746776587000）。                               |
| state      | string | YES | 訂單狀態說明如下：1：進行中（In Progress） 2：已完成（Finish） 3：已撤銷（Revoke）      |

