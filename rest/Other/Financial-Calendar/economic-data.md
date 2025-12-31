# Other - Financial Calendar - Economic Data


```
GET /api/calendar/economic-data
```


This endpoint provides data for the economic data

***Cache / Update Frequency:*** 10 minutes for all the API plans.

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |

<br />

**Response Data**

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
      "importance_level": 1, //1,2,3
      "has_exact_publish_time": 1
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
| Name       | Type    | Mandatory | Description                                                                                            |
| ---------- | ------- | --------- | ------------------------------------------------------------------------------------------------------ |
| start_time | integer | NO        | Start timestamp in milliseconds. The maximum supported range is up to 15 days before the current time. |
| end_time   | integer | NO        | End timestamp in milliseconds. The maximum supported range is up to 15 days after the current time.    |
| language   | string  | NO        | Supported language :  'en' or  'zh'                                                                    |

