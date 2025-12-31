# 其他 - 财经日历 - 财经事件


```
GET /api/calendar/financial-events
```


此接口提供财经事件的数据

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
      "calendar_name": "美国总统特朗普发表讲话", //描述
      "country_name": "",  //国家code
      "publish_timestamp": 1751394600000,  //公布时间
      "importance_level": 2,// 重要等级 1,2,3
      "has_exact_publish_time": 1 //1代表有具体公布时间， 2代表没有具体公布时间
    },
    {
      "calendar_name": "美国财长贝森特发表讲话",
      "country_code": "USA",
      "country_name": "美国",
      "publish_timestamp": 1751563800000,
      "importance_level": 3, //1,2,3
      "has_exact_publish_time": 1
    },
}
```

 **Parameters:**
| 名称         | 类型      | 必填 | 描述                                  |
| ---------- | ------- | -- | ----------------------------------- |
| start_time | integer | NO | 开始时间戳（以毫秒为单位）。支持的最大范围为当前时间往前推 15 天。 |
| end_time   | integer | NO | 结束时间戳（以毫秒为单位）。支持的最大范围为当前时间往后推 15 天。 |

