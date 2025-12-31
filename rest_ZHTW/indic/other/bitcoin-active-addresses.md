# 指標 - 其他指標 - 比特幣活躍地址


```
GET /api/index/bitcoin-active-addresses
```


該接口提供比特幣活躍地址

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
      "timestamp": 1282003200000,
      "price": 0.07,
      "active_address_count": 494
    },
    {
      "timestamp": 1282089600000,
      "price": 0.068,
      "active_address_count": 726
    },
    {
      "timestamp": 1282176000000,
      "price": 0.0667,
      "active_address_count": 470
    },
}

```

