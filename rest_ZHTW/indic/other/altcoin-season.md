# 指標 - 其他指標 - 山寨幣季節指數


```
GET /api/index/altcoin-season
```


該接口提供山寨幣季節指數數據

***快取 / 更新頻率:*** 1天更新一次

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "data": [
    {
      "timestamp": 1491177600000,
      "altcoin_index": 96,
      "altcoin_marketcap": 0
    },
    {
      "timestamp": 1491264000000,
      "altcoin_index": 100,
      "altcoin_marketcap": 0
    },
    {
      "timestamp": 1491350400000,
      "altcoin_index": 96,
      "altcoin_marketcap": 0
    },
}

```

