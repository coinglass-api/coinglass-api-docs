# 指标 - 其他指标 - 比特币长期持有者平均持仓成本


```
GET /api/index/bitcoin-lth-realized-price
```


该接口提供比特币长期持有者平均持仓成本数据

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

