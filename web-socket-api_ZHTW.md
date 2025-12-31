# 基礎介紹

### 基礎地址

`wss://open-ws.coinglass.com/ws-api`

### 連接方式

要建立連線，請使用以下地址並附帶您的 API Key：

```
wss://open-ws.coinglass.com/ws-api?cg-api-key={your_api_key}
```

### 連線管理

* 若發生網路問題，系統將自動中斷連線。
* 為了保持連線的穩定性，建議每 20 秒發送一次 ping 訊息，並預期收到 pong 回應。

### 訂閱

若需訂閱某個頻道，請發送以下訊息：

```json
{
    "method": "subscribe",
    "channels": ["liquidationOrders"]
}
```

### 取消訂閱

若需取消訂閱某個頻道，請發送以下訊息：

```json
{
    "method": "unsubscribe",
    "channels": ["liquidationOrders"]
}
```

### 回應範例

當收到資料時，回應格式如下所示：

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

此格式可確保在使用 WebSocket API 互動時的清晰性與易用性。

# 爆倉訂單

強平訂單快照流提供市場交易對的強平訂單數據。

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
| :----- | :-- | :-- | :-- | :-- | :-- |
| 可用性    | ❌   | ❌   | ✅   | ✅   | ✅   |

<br />

# 實時強平訂單推送

## 頻道: `liquidationOrders`

若需訂閱 liquidationOrders 頻道，請發送以下訊息：

```json
{
    "method": "subscribe",
    "channels": ["liquidationOrders"]
}
```

### 返回範例

接收到數據後，返回內容如下所示：

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

# 合約成交訂單

合約成交訂單流會提供某一交易對的即時成交數據。

***該接口以下 API 等級可用：*** [API 等級](https://www.coinglass.com/zh-TW/pricing)：

| API 等級 | 業餘版 | 創業版 | 標準版 | 專業版 | 企業版 |
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

### 返回範例

接收到數據後，返回內容如下所示：

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