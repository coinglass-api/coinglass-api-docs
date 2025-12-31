# 其他 - 财经日历 - 经济数据


```
GET /api/calendar/economic-data
```


该接口提供经济数据

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
      "calendar_name": "全国经济信心指数(至0711)",
      "country_code": "CAN",
      "country_name": "加拿大",
      "data_effect": "影响较小",
      "forecast_value": "",
      "revised_previous_value": "",
      "previous_value": "52.10",
      "publish_timestamp": 1752494400000,
      "published_value": "52",
      "importance_level": 1,  // 1,2,3
      "has_exact_publish_time": 1
    },
    {
      "calendar_name": "5月批发销售(月率)",
      "country_code": "CAN",
      "country_name": "加拿大",
      "data_effect": "利多加元",
      "forecast_value": "-0.4%",
      "revised_previous_value": "",
      "previous_value": "-2.3%",
      "publish_timestamp": 1752496200000,
      "published_value": "0.1%",
      "importance_level": 2,   // 1,2,3
      "has_exact_publish_time": 1
    },
```

 **Parameters:**
| 名称         | 类型      | 必填 | 描述                                 |
| ---------- | ------- | -- | ---------------------------------- |
| start_time | integer | NO | 开始时间戳（以毫秒为单位）。支持的最大范围为当前时间之前 15 天。 |
| end_time   | integer | NO | 结束时间戳（以毫秒为单位）。支持的最大范围为当前时间之后 15 天。 |
| language   | string  | NO | 支持的语言：'en' 或 'zh'                  |

