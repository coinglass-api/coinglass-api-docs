# 🔐 身份验证

所有对 CoinGlass API 的请求都需要使用唯一且与用户绑定的 API Key 进行身份验证。

如果请求中缺少有效的 API Key 或请求头不完整，将会被拒绝，并返回身份验证错误。

<br />

🧾 **如何获取 API Key**

请登录您的账号，并在 [ API Key 管理页面](https://www.coinglass.com/zh/account)生成您的 API Key 以开始使用。.

✅ **示例用法**

```json curl
curl -X GET "https://open-api-v4.coinglass.com/api/futures/supported-coins" \
  -H "accept: application/json" \
  -H "CG-API-KEY: YOUR_API_KEY"
```

<br />

📦 **请求头要求：**

每一个请求必须包含以下 HTTP 请求头：

CG-API-KEY: '你的API Key'

如果缺少该请求头，或提供的 API Key 无效，请求将被拒绝，并返回 401 Unauthorized（未授权）错误。❗

<br />

**请求限制：**

响应头：

* `API-KEY-MAX-LIMIT`：表示您的 API 密钥允许的最大请求限制（每分钟）。
* `API-KEY-USE-LIMIT`：显示您的 API 密钥的当前使用次数（当前时间段内发出的请求次数）。