# 指標 - 其他指標 - 穩定幣市值歷史


```
GET /api/index/stableCoin-marketCap-history
```


該接口提供穩定幣市值歷史。

***快取 / 更新頻率:*** 每 1天更新一次

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
      "data_list": [4611285.1141, ...],         // 數值列表
      "price_list": [, ...],                    // 價格列表
      "time_list": [1636588800, ...]            // 時間戳列表
    }
  ]
}

```

