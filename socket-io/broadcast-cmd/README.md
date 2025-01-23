# Broadcast Event with Socket.io

## Overview

This document defines the `broadcast` event used in real-time communication via Socket.io. It explains the event structure, supported commands, and examples for client-server interaction.

---

## Event: `broadcast`

### Description

Handles broadcasting commands and data to a specific room.

---

### Parameters

| Name   | Type   | Required | Description                                                                        |
| ------ | ------ | -------- | ---------------------------------------------------------------------------------- |
| `room` | string | Yes      | The target room to broadcast the event.                                            |
| `cmd`  | string | Yes      | The command to execute in the room.                                                |
| `data` | object | Yes      | The payload associated with the command. The structure depends on the `cmd` value. |

---

### Supported `cmd` Values

| **`cmd`**             | **Description**       | **`data` Structure**                   |
| --------------------- | --------------------- | -------------------------------------- |
| `1. voiceStreamStart` | VoiceStream 전송 시작 | `{ userId: string, timestamp: string}` |
| `2. voiceStreamStop`  | VoiceStream 전송 종료 | `{ userId: string, timestamp: string}` |

---

### Example Payloads

#### 1. `voiceStreamStart`

```json
{
  "room": "31f15c3d-decc-451a-84a8-31c16452ab75",
  "cmd": "voiceStreamStart",
  "data": {
    "userId": "779c9f7d-b6a1-4c2b-a933-a2505867855a",
    "timestamp": "2025-01-07T08:05:09.146Z"
  }
}
```

#### 2. `voiceStreamStop`

```json
{
  "room": "31f15c3d-decc-451a-84a8-31c16452ab75",
  "cmd": "voiceStreamStop",
  "data": {
    "userId": "779c9f7d-b6a1-4c2b-a933-a2505867855a",
    "timestamp": "2025-01-07T08:05:09.146Z"
  }
}
```
