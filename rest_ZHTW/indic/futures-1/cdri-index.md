# 指標 - 合約指標 - CDRI 指數


```
GET /new-endpoint
```


此端點提供 CDRI（CoinGlass 衍生品風險指數） 的歷史數據。

***快取 / 更新頻率:*** 即時更新

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 響應數據

```json
{
  "code": "0",
  "data": [
    {
      "time": 1646438400000,
      "cdri_index_value": 50
    },
    {
      "time": 1646524800000,
      "cdri_index_value": 47
    },
  ]
}
```

