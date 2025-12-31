# 指標 - 其他指標 - 期權持倉 VS 合約持倉


```
GET /api/index/option-vs-futures-oi-ratio
```


該接口提供期權持倉 VS 合約持倉數據

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
      "btc_option_vs_futures_radio": 45.1,
      "eth_option_vs_futures_radio": 21.92,
      "timestamp": 1592956800000
    },
    {
      "btc_option_vs_futures_radio": 45.15,
      "eth_option_vs_futures_radio": 23.16,
      "timestamp": 1593043200000
    },
    {
      "btc_option_vs_futures_radio": 47.27,
      "eth_option_vs_futures_radio": 23.65,
      "timestamp": 1593129600000
    },
}

```

