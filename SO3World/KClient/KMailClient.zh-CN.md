[English](./KMailClient.md) | 中文

# KMailClient（邮件客户端）

邮件客户端对象，用于管理邮件操作。

说明：

- 通过 `GetMailClient()` 获取

## 方法

[`GetMailInfo`](#KMailClient_GetMailInfo)
[`GetMailList`](#KMailClient_GetMailList)
[`DeleteMail`](#KMailClient_DeleteMail)
[`CountMail`](#KMailClient_CountMail)

---

* <h4 id="KMailClient_GetMailInfo">GetMailInfo</h4>

根据邮件 ID 获取邮件信息。

 > ([`KMailInfo`](./KMailInfo.zh-CN.md) mailInfo) KMailClient:GetMailInfo(`number` dwMailID)

* <h4 id="KMailClient_GetMailList">GetMailList</h4>

获取所有邮件列表。

 > (`table` tMailList) KMailClient:GetMailList()

* <h4 id="KMailClient_DeleteMail">DeleteMail</h4>

根据 ID 删除邮件。

 > (`void`) KMailClient:DeleteMail(`number` dwMailID)

* <h4 id="KMailClient_CountMail">CountMail</h4>

统计邮件总数。

 > (`number` nCount) KMailClient:CountMail()

---

## 被屏蔽的方法

以下方法在 addon 环境中被屏蔽，无法使用：

| 方法 | 说明 |
|------|------|
| `SendMail` | ⚠️ 被屏蔽 - 发送邮件 |
| `ApplyMailList` | ⚠️ 被屏蔽 - 申请邮件列表 |
| `GetPlayerMessage` | ⚠️ 被屏蔽 - 获取玩家消息 |
| `GetGmMessage` | ⚠️ 被屏蔽 - 获取 GM 消息 |
| `ReturnMail` | ⚠️ 被屏蔽 - 退回邮件 |
