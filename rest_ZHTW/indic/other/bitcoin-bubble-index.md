# 指標 - 其他指標 - 比特幣泡沫指數


```
GET /api/index/bitcoin/bubble-index
```


該接口提供比特幣泡沫指數接口。

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "price": 0.0495,                          // 當前價格
      "bubble_index": -29.59827206,             // 泡沫指數
      "google_trend_percent": 0.0287,           // Google 趨勢百分比
      "mining_difficulty": 181.543,             // 挖礦難度
      "transaction_count": 235,                 // 交易數量
      "address_send_count": 390,                // 地址發送數量
      "tweet_count": 0,                         // 推特數量
      "date_string": "2010-07-17"               // 日期字串
    },
    {
      "price": 0.0726,                          // 當前價格
      "bubble_index": -29.30591863,             // 泡沫指數
      "google_trend_percent": 0.0365,           // Google 趨勢百分比
      "mining_difficulty": 181.543,             // 挖礦難度
      "transaction_count": 248,                 // 交易數量
      "address_send_count": 424,                // 地址發送數量
      "tweet_count": 0,                         // 推特數量
      "date_string": "2010-07-18"               // 日期字串
    }
  ]
}

```

