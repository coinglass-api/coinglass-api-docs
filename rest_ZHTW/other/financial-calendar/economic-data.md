# 其他 - 財經日曆 - 經濟數據


```
GET /api/calendar/economic-data
```


該接口提供經濟數據

***快取 / 更新頻率:*** 每 10 分鐘更新一次

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
      "calendar_name": "Seasonally adjusted industrial output (MoM)(May)",
      "country_code": "SK",
      "country_name": "Korea",
      "data_effect": "Minor Impact",
      "forecast_value": "-0.1%",
      "revised_previous_value": "",
      "previous_value": "-0.9%",
      "publish_timestamp": 1751238000000,
      "published_value": "-2.9%",
      "importance_level": 1,// 1,2,3
      "has_exact_publish_time": 1  //1代表有具體公佈時間， 2代表沒有具體公佈時間
    },
    {
      "calendar_name": "Industrial Output(YoY)(May)",
      "country_code": "SK",
      "country_name": "Korea",
      "data_effect": "Minor Impact",
      "forecast_value": "2.6%",
      "revised_previous_value": "",
      "previous_value": "4.9%",
      "publish_timestamp": 1751238000000,
      "published_value": "0.2%",
      "importance_level": 1,  //1,2,3
      "has_exact_publish_time": 1
    },
}
```

 **Parameters:**
| 名称         | 类型      | 必填 | 描述                                 |
| ---------- | ------- | -- | ---------------------------------- |
| start_time | integer | NO | 開始時間戳（以毫秒為單位）。支援的最大範圍為目前時間之前 15 天。 |
| end_time   | integer | NO | 結束時間戳（以毫秒為單位）。支援的最大範圍為目前時間之後 15 天。 |
| language   | string  | NO | 支援語言：'en' 或 'zh'                   |

