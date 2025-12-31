# 其他 - 新闻、快讯 - 快讯


```
GET /api/newsflash/list
```


这个接口提供实时快讯列表（最多返回近1000条快讯）

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
      "newsflash_picture": "",//快讯图片
      "newsflash_title": "Binance：Alpha 2.0的ELIZAOS交易开始时间已被推迟", //快讯标题
      "newsflash_content": "<p>BlockBeats 消息新的上线时间将另行通知。</p>",//快讯内容
      "source_name": "BLOCKBEATS",  //快讯来源名称
      "source_website_logo": "https://cdn.coinglasscdn.com/news/block_beats.png",//快讯来源logo
      "newsflash_release_time": 1762482906000 //快讯发布时间
    },
    {
      "newsflash_title": "特朗普加密顾问、Bitcoin Magazine主席：DeFi借贷信用危机或演化为加密流动性危机，或将蔓延至CeFi领域",
      "newsflash_content": "Odaily星球日报请保持安全并避免交易对手风险。”",
      "source_name": "ODAILY",
      "source_website_logo": "https://cdn.coinglasscdn.com/news/odaily.png",
      "newsflash_release_time": 1762482628000
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
| language   | string | NO | 支持的语言： 'zh' 、'zh-tw'           |
| page       | string | NO | 当前页码                           |
| per_page   | string | NO | 每页返回条数                         |

