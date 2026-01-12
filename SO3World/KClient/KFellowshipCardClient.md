English | [中文](./KFellowshipCardClient.zh-CN.md)

# KFellowshipCardClient

Fellowship card client for managing friendship cards.

Notes:

- Obtained via `GetFellowshipCardClient()`

## Methods

[`ApplyFellowshipCard`](#KFellowshipCardClient_ApplyFellowshipCard)
[`GetFellowshipCardInfo`](#KFellowshipCardClient_GetFellowshipCardInfo)

---

* <h4 id="KFellowshipCardClient_ApplyFellowshipCard">ApplyFellowshipCard</h4>

Requests fellowship card information.

 > (`void`) KFellowshipCardClient:ApplyFellowshipCard(`number` dwPlayerID)

* <h4 id="KFellowshipCardClient_GetFellowshipCardInfo">GetFellowshipCardInfo</h4>

Gets fellowship card information.

 > (`table` tCardInfo) KFellowshipCardClient:GetFellowshipCardInfo(`number` dwPlayerID)

---

## Shielded Methods

The following methods are blocked in addon environment and cannot be used:

| Method | Description |
|--------|-------------|
| `SetSignature` | ⚠️ Blocked - Set personal signature |
