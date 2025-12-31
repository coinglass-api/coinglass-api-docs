# 基础介绍

### 基础地址

`wss://open-ws.coinglass.com/ws-api`

### 连接方式

要建立连接，请使用以下地址并附带您的 API Key：

```
wss://open-ws.coinglass.com/ws-api?cg-api-key={your_api_key}
```

### 连接管理

* 如果发生网络问题，系统将自动断开连接。
* 为了保持连接的稳定性，建议每 20 秒发送一次 'ping' 消息，并预期收到 'pong' 响应。

### 订阅

如需订阅某个频道，请发送以下消息：

```json
{
    "method": "subscribe",
    "channels": ["liquidationOrders"]
}
```

### 取消订阅

如需取消订阅某个频道，请发送以下消息：

```json
{
    "method": "unsubscribe",
    "channels": ["liquidationOrders"]
}
```

### 响应示例

当收到数据时，响应格式如下所示：

```json
{
    "channel": "liquidationOrders",
    "data": [
        {
            "baseAsset": "BTC",
            "exName": "Binance",
            "price": 56738.00,
            "side": 2,
            "symbol": "BTCUSDT",
            "time": 1725416318379,
            "volUsd": 3858.18400
        }
    ]
}
```

***

该格式可确保在使用 WebSocket API 交互时的清晰性与易用性。


# 爆仓订单

强平订单快照流提供市场交易对的强平订单信息。

***以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

<br />

# 实时强平订单推送

## 频道: `liquidationOrders`

如需订阅 liquidationOrders 频道，请发送以下消息：

```json
{
    "method": "subscribe",
    "channels": ["liquidationOrders"]
}
```

### 返回示例

接收到数据后，返回内容如下所示：

```json
{
    "channel": "liquidationOrders",
    "data": [
        {
            "baseAsset": "BTC",
            "exName": "Binance",
            "price": 56738.00,
            "side": 2, //side=1   Long liquidation     side=2   Short liquidation
            "symbol": "BTCUSDT",
            "time": 1725416318379,
            "volUsd": 3858.18400
        }
    ]
}
```


# 合约成交订单

合约成交订单流会提供某一交易对的实时成交数据。

***以下API等级可用：*** [API 等级](https://www.coinglass.com/zh/pricing)：

| API 等级 | 爱好版 | 创业版 | 标准版 | 专业版 | 企业版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

```text
# Real-Time Futures Trade Orders Push

## Channel: `futures_trades@``{exchange}`_`{symbol}`@``{minVol}`

To subscribe to the `futures_trades` channel, send the following message: 




```

```json
{
    "method": "subscribe",
    "channels": ["futures_trades@Binance_BTCUSDT@10000"]
}
```

### 返回示例

接收到数据后，返回内容如下所示：

```json
{
    "channel": "futures_trades@Binance_BTCUSDT@10000",
    "data": [
        {
            "baseAsset": "BTC",
            "exName": "Binance",
            "price": 56738.00,
            "side": 2,//side=1  sell.   side=2   buy   
            "symbol": "BTCUSDT",
            "time": 1725416318379,
            "volUsd": 3858.18400
        }
    ]
}
```