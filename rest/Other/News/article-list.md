# Other - News - News


```
GET /api/article/list
```


This endpoint provides an instant news (up to nearly 1000 news items).

***Cache / Update Frequency:*** Real-time updates

***This endpoint is available on the following*** [API plans](https://www.coinglass.com/pricing)：

| Plans     | Hobbyist | Startup | Standard | Professional | Enterprise |
| :-------- | :------- | :------ | :------- | :----------- | :--------- |
| Available | ❌        | ✅       | ✅        | ✅            | ✅          |


 **Parameters:**
| Name       | Type    | Mandatory | Description                                            |
| ---------- | ------- | --------- | ------------------------------------------------------ |
| start_time | integer | NO        | Start timestamp in milliseconds (e.g., 1641522717000). |
| end_time   | integer | NO        | End timestamp in milliseconds (e.g., 1641522717000).   |
| language   | string  | NO        | Supported languages: 'en', 'zh', 'zh-tw'               |
| page       | integer | NO        | Current page number                                    |
| per_page   | integer | NO        | Number of items returned per page                      |


**Response Data:**

```json
{
  "code": "0",
  "data": [
    {
      "article_picture":  "https://images.cointelegraph.com/images/528_aHR0cHM6Ly9zMy5jb2ludGVsZWdyYXBoLmNvbS91cGxvYWRzLzIwMjUtMDIvMDE5NTNkOTUtOTEyYi03MTE4LWE3NTEtNDRjNDExZWUzNmMy.jpg",  //Article Picture
      "article_title": "Crypto ETFs ‘punching above weight’ as almost half of ETF investers plan buys", // Article Title
      "article_content": "<p>Nearly h \n</blockquote> <!---->",  //Article Content
      "source_name": "COINTELEGRAPH",   // Source Name
      "source_website_logo": "https://cdn.coinglasscdn.com/news/coin_telegraph.png",   //Source Website Logo
      "article_release_time": 1762482358000, //Article Release Time
      "article_description": "<p>Bloomberg ETF analyst Eric Balchunas said it was “shocking” to see Schwab’s findings that crypto ETF investments could be on par with those in bond ETFs.</p>" // Article Description
    },

    {
      "article_picture": "https://images.cointelegraph.com/images/528_aHR0cHM6Ly9zMy5jb2ludGVsZWdyYXBoLmNvbS91cGxvYWRzLzIwMjUtMTEvMDE5YTViM2MtODFkOC03NWFhLTg2MjEtOGEyYmZjMDJhZDk0.jpg",
      "article_title": "Bitcoin at $100K is ‘speed bump’ to $56K, but data signals no signs of panic",
      "article_content": "<p data-ct-non-bby 2030.</p> <!---->",
      "source_name": "COINTELEGRAPH",
      "source_website_logo": "https://cdn.coinglasscdn.com/news/coin_telegraph.png",
      "article_release_time": 1762478945000,
      "article_description": "<p>Bloomberg analyst Mike McGlone says Bitcoin hitting $100,000 is “a speed bump” to $56,000, but other analysts say Bitcoin has bottomed out.</p>"
    },
  ]
}
```

