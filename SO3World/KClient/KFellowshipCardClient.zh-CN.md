[English](./KFellowshipCardClient.md) | 中文

# KFellowshipCardClient（好友名片客户端）

好友名片客户端，用于管理好友名片。

说明：

- 通过 `GetFellowshipCardClient()` 获取

## 方法

[`ApplyFellowshipCard`](#KFellowshipCardClient_ApplyFellowshipCard)
[`GetFellowshipCardInfo`](#KFellowshipCardClient_GetFellowshipCardInfo)

---

* <h4 id="KFellowshipCardClient_ApplyFellowshipCard">ApplyFellowshipCard</h4>

请求获取好友名片信息。

 > (`void`) KFellowshipCardClient:ApplyFellowshipCard(`number` dwPlayerID)

* <h4 id="KFellowshipCardClient_GetFellowshipCardInfo">GetFellowshipCardInfo</h4>

获取好友名片信息。

 > (`table` tCardInfo) KFellowshipCardClient:GetFellowshipCardInfo(`number` dwPlayerID)

---

## 被屏蔽的方法

以下方法在 addon 环境中被屏蔽，无法使用：

| 方法 | 说明 |
|------|------|
| `SetSignature` | ⚠️ 被屏蔽 - 设置个性签名 |
