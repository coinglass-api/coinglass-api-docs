# 其他 - 新闻、快讯 - 新闻


```
GET /api/article/list
```


这个接口提供实时新闻列表（最多返回近1000条新闻）

***缓存 / 更新频率:*** 实时更新.

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
      "article_picture": "https://www.chaincatcher.com/upload/image/20251107/1762481312628-595379.webp",   //新闻封面
      "article_title": "ANT.FUN 创始人 Shaun：稳定币与 AGI 融合将催生「金融超级 App」", //新闻标题
      "article_content": "<p style=来大规模使用。</p>",  //新闻内容
      "source_name": "chaincatcher", //新闻来源 
      "source_website_logo":   "https://cdn.coinglasscdn.com/static/news/chaincatcher.png",  //新闻来源 logo
      "article_release_time": 1762481371000  // 新闻发布时间
    },
    {
      "article_picture": "https://uploads.panewslab.com/2025z/00cf2969-73c7-44ff-8fee-54706d79cf8e",
      "article_title": "币安人生发币者：市值最高冲到5亿美金，但我只赚了4000",
      "article_content": "<p>2025 年 10诸公共解。</p>",
      "source_name": "PANews",
      "source_website_logo": "https://cdn.coinglasscdn.com/news/panews.png",
      "article_release_time": 1762480819000
    },
    ...
  ]
}
```

 **Parameters:**
| 名称         | 类型     | 必填 | 描述                             |
| ---------- | ------ | -- | ------------------------------ |
| start_time | string | NO | 起始时间戳（单位：毫秒，例如：1641522717000）。 |
| end_time   | string | NO | 结束时间戳（单位：毫秒，例如：1641522717000）。 |
| language   | string | NO | 支持的语言：'en' 、 'zh' 、'zh-tw'     |
| page       | string | NO | 当前页码                           |
| per_page   | string | NO | 每页返回条数                         |

