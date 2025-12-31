# 指標 - 合約指標 - CGDI 指數


```
GET /api/futures/cgdi-index/history
```


此端點提供 CGDI（CoinGlass 衍生品指數） 的歷史數據。

***快取 / 更新頻率:*** 即時更新.\\

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
      "time": 1704067200000,
      "cgdi_index_value": 1000
    },
    {
      "time": 1704153600000,
      "cgdi_index_value": 1053.2551
    },
  ]
}
```

