# 其他 - 财经日历 - 央行动态


```
GET /api/calendar/central-bank-activities
```


此接口提供央行动态数据

***缓存 / 更新频率:*** 每 10 分钟更新一次

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
      "calendar_name": "欧洲央行在辛特拉举行中央银行论坛",
      "country_code": "PT",
      "country_name": "葡萄牙",
      "publish_timestamp": 1751213100000,
      "importance_level": 3, // 1,2,3
      "has_exact_publish_time": 2
    },
    {
      "calendar_name": "亚特兰大联储主席博斯蒂克就美国经济前景发表讲话",
      "country_code": "USA",
      "country_name": "美国",
      "publish_timestamp": 1751288400000,
      "importance_level": 3, // 1,2,3
      "has_exact_publish_time": 1
    },
}
```

 **Parameters:**
| 名称         | 类型      | 必填 | 描述                                  |
| ---------- | ------- | -- | ----------------------------------- |
| start_time | integer | NO | 开始时间戳（以毫秒为单位）。支持的最大范围为当前时间往前推 15 天。 |
| end_time   | integer | NO | 结束时间戳（以毫秒为单位）。支持的最大范围为当前时间往后推 15 天。 |

