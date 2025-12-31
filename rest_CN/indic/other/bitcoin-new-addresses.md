# 指标 - 其他指标 - 比特币新地址


```
GET /api/index/bitcoin-new-addresses
```


该接口提供比特币新地址数据

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
      "timestamp": 1282003200000,
      "price": 0.07,
      "new_address_count": 331
    },
    {
      "timestamp": 1282089600000,
      "price": 0.068,
      "new_address_count": 415
    },
    {
      "timestamp": 1282176000000,
      "price": 0.0667,
      "new_address_count": 316
    },
}

```

