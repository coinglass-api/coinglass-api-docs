# 指標 - 其他指標 - 比特幣長期持有者平均持倉成本


```
GET /api/index/bitcoin-lth-realized-price
```


該接口提供比特幣長期持有者平均持倉成本數據

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
      "timestamp": 1325376000000,
      "price": 4.61211781,
      "lth_realized_price": 4.938
    },
    {
      "timestamp": 1325462400000,
      "price": 5.13201225,
      "lth_realized_price": 4.937
    },
    {
      "timestamp": 1325548800000,
      "price": 5.21773083,
      "lth_realized_price": 4.946
    },
}

```

