# 指标 - 其他指标 - 比特币泡沫指数


```
GET /api/index/bitcoin/bubble-index
```


该接口提供比特币泡沫指数接口

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "msg": "success",
  "data": [
    {
      "price": 0.0495,                          // 当前价格
      "bubble_index": -29.59827206,             // 泡沫指数
      "google_trend_percent": 0.0287,           // Google 趋势百分比
      "mining_difficulty": 181.543,             // 挖矿难度
      "transaction_count": 235,                 // 交易数量
      "address_send_count": 390,                // 地址发送数量
      "tweet_count": 0,                         // 推特数量
      "date_string": "2010-07-17"               // 日期字符串
    },
    {
      "price": 0.0726,                          // 当前价格
      "bubble_index": -29.30591863,             // 泡沫指数
      "google_trend_percent": 0.0365,           // Google 趋势百分比
      "mining_difficulty": 181.543,             // 挖矿难度
      "transaction_count": 248,                 // 交易数量
      "address_send_count": 424,                // 地址发送数量
      "tweet_count": 0,                         // 推特数量
      "date_string": "2010-07-18"               // 日期字符串
    }
  ]
}

```

