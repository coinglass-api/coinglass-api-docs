# Getting Started

### Base URL

`wss://open-ws.coinglass.com/ws-api`

### Connection

To connect, use the following URL with your API key:

```
wss://open-ws.coinglass.com/ws-api?cg-api-key={your_api_key}
```

### Connection Handling

* The system will automatically disconnect if there are network issues.
* To maintain a stable connection, it is recommended to send a `'ping'` message every 20 seconds. Expect a `'pong'` response.

### Subscription

To subscribe to a channel, send the following message:

```json
{
    "method": "subscribe",
    "channels": ["liquidationOrders"]
}
```

### Unsubscription

To unsubscribe from a channel, send the following message:

```json
{
    "method": "unsubscribe",
    "channels": ["liquidationOrders"]
}
```

### Response Example

Upon receiving data, the response will look like this:

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

This format ensures clarity and ease of use when interacting with the WebSocket API.


# Liquidation Order

The liquidation order snapshot streams provide information on forced liquidation orders for market symbols.

<span style={{ color: "red", fontSize: "24px", fontWeight: "bold" }}># Required Account Level: Standard Edition and Above</span>

# Real-Time Liquidation Orders Push

## Channel: `liquidationOrders`

To subscribe to the `liquidationOrders` channel, send the following message:

```json
{
    "method": "subscribe",
    "channels": ["liquidationOrders"]
}
```

### Response Example

Upon receiving data, the response will look like this:

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


# Futures Trade Order

The futures trade order streams provide real-time information on executed futures trades for market symbols.

<span style={{ color: "red", fontSize: "24px", fontWeight: "bold" }}># Required Account Level: Standard Edition and Above</span>

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

### Response Example

Upon receiving data, the response will look like this:

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

<br />

### Response Example

Upon receiving data, the response will look like this: