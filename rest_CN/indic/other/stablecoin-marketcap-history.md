# 指标 - 其他指标 - 稳定币市值历史


```
GET /api/index/stableCoin-marketCap-history
```


该接口提供稳定币市值历史

***缓存 / 更新频率:*** 每天一次.

***该接口以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ✅   | ✅   | ✅   | ✅   | ✅   |

### 响应数据

```json
{
  "code": "0",                             
  "msg": "success",                        
  "data": [
    {
      "data_list": [4611285.1141, ...],         // 数值列表
      "price_list": [, ...],                    // 价格列表
      "time_list": [1636588800, ...]            // 时间戳列表
    }
  ]
}

```

