# Realtime Metrics Websocket Documentation

## Overview

This API provides a WebSocket interface for subscribing to real-time updates on system metrics including memory and CPU usage for a set of servers identified as:
- server01
- server02
- server03
- server04
- server05

You can connect to the server using websocket protocol on:

```http
wss://lps-monitoring.up.railway.app/realtime
```

## Message Format

Client should communicate with the server using JSON-formatted messages. Each message must adhere to the `MetricMessage` type format.

## MetricMessage

```json
{
    "type": "memory" | "cput" | "all",
    "machine": "server01",
    "subscribe": true | false
}
```

## Protocol

Upon sending subscription request for any event type, you should receive a replicate reply with `success` status.

For example:

```json
> {"type": "memory", "machine": "server01", "subscribe": true}
< {"type": "memory", "machine": "server01", "subscribe": true, "success": true}
```

Then you should receive a stream of events every 1 second until you unsubscribe.

## Metrics

### All

```json
{
    "machine": "server02",
    "timestamp": 1704375235932,
    "memory": {
        "total": 6,
        "free": 5.68,
        "used": 0.32,
        "usedPercentage": 5.29,
        "freePercentage": 94.71
    },
    "cpu": [
        {
            "id": 0,
            "usage": 4.19
        },
        {
            "id": 1,
            "usage": 17.91
        },
        {
            "id": 2,
            "usage": 10.27
        },
        {
            "id": 3,
            "usage": 82
        }
    ]
}
```

### Memory

```json
{
    "machine": "server02",
    "timestamp": 1704375282966,
    "memory": {
        "total": 6,
        "free": 5.67,
        "used": 0.33,
        "usedPercentage": 5.46,
        "freePercentage": 94.54
    }
}
```

### CPU

```json
{
    "machine": "server02",
    "timestamp": 1704375318995,
    "cpu": [
        {
            "id": 0,
            "usage": 87.61
        },
        {
            "id": 1,
            "usage": 47.44
        },
        {
            "id": 2,
            "usage": 77.26
        },
        {
            "id": 3,
            "usage": 41.03
        }
    ]
}
```
