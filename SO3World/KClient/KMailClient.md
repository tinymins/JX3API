English | [中文](./KMailClient.zh-CN.md)

# KMailClient

Mail client object for managing mail operations.

Notes:

- Obtained via `GetMailClient()`

## Methods

[`GetMailInfo`](#KMailClient_GetMailInfo)
[`GetMailList`](#KMailClient_GetMailList)
[`DeleteMail`](#KMailClient_DeleteMail)
[`CountMail`](#KMailClient_CountMail)

---

* <h4 id="KMailClient_GetMailInfo">GetMailInfo</h4>

Gets mail information by mail ID.

 > ([`KMailInfo`](./KMailInfo.md) mailInfo) KMailClient:GetMailInfo(`number` dwMailID)

* <h4 id="KMailClient_GetMailList">GetMailList</h4>

Gets the list of all mails.

 > (`table` tMailList) KMailClient:GetMailList()

* <h4 id="KMailClient_DeleteMail">DeleteMail</h4>

Deletes a mail by ID.

 > (`void`) KMailClient:DeleteMail(`number` dwMailID)

* <h4 id="KMailClient_CountMail">CountMail</h4>

Counts the total number of mails.

 > (`number` nCount) KMailClient:CountMail()

---

## Shielded Methods

The following methods are blocked in addon environment and cannot be used:

| Method | Description |
|--------|-------------|
| `SendMail` | ⚠️ Blocked - Send mail |
| `ApplyMailList` | ⚠️ Blocked - Apply for mail list |
| `GetPlayerMessage` | ⚠️ Blocked - Get player message |
| `GetGmMessage` | ⚠️ Blocked - Get GM message |
| `ReturnMail` | ⚠️ Blocked - Return mail |
