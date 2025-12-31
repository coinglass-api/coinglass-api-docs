# 指标 - 其他指标 - 比特币 RHODL 比值


```
GET /api/index/bitcoin-rhodl-ratio
```


该接口提供比特币 RHODL 比值数据

***缓存 / 更新频率:*** 1天更新一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",
  "data": [
    {
      "price": 0.07,
      "rhodl_ratio": 0.19768584894587235,
      "timestamp": 1282003200000
    },
    {
      "price": 0.068,
      "rhodl_ratio": 0.3765371066876411,
      "timestamp": 1282089600000
    },
    {
      "price": 0.0667,
      "rhodl_ratio": 0.55947437296653,
      "timestamp": 1282176000000
    },
}

```

