# 🔐 Authentication

All requests to the CoinGlass API require authentication using a unique, user-specific API Key.

Requests without a valid API Key or missing headers will be rejected with an authentication error.

<br />

🧾 **How to Get an API Key**

To get started, log in to your account and generate your API Key from your [API Key Dashboard](https://www.coinglass.com/account).

✅ **Example Usage**

```json curl
curl -X GET "https://open-api-v4.coinglass.com/api/futures/supported-coins" \
  -H "accept: application/json" \
  -H "CG-API-KEY: YOUR_API_KEY"
```

<br />

📦 **Header Requirement**

Every request must include the following HTTP header:

CG-API-KEY: your\_api\_key\_here

If this header is missing or the API Key is invalid, the request will be denied with a 401 Unauthorized error. ❗

<br />

**Response Headers:**

<br />

* `API-KEY-MAX-LIMIT`: Indicates the maximum allowed request limit for your API key (per minute).
* `API-KEY-USE-LIMIT`: Shows the current usage count of your API key (requests made in the current time period).