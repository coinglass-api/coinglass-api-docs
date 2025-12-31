# ❗ Errors & Rate Limits

📡  **API Response Status Codes**

The CoinGlass API uses standard HTTP status codes to indicate the success or failure of your requests. Refer to the table below for a quick understanding of common response codes:

| Status Code | Description                                |
| :---------- | :----------------------------------------- |
| 0           | Successful Request                         |
| 400         | Missing or invalid parameters              |
| 401         | Invalid or missing API key                 |
| 404         | The requested resource does not exist      |
| 405         | Unsupported HTTP method                    |
| 408         | The request took too long to complete      |
| 422         | Parameters valid but not acceptable        |
| 429         | Rate limit exceeded                        |
| 500         | An unexpected error occurred on the server |

🚦 **Rate Limits**

The rate limit is depending on the paid plan that you're subscribed to. [this page](https://www.coinglass.com/pricing)

<br />

Response Headers:

API-KEY-MAX-LIMIT: Indicates the maximum allowed request limit for your API key (per minute).
API-KEY-USE-LIMIT: Shows the current usage count of your API key (requests made in the current time period).