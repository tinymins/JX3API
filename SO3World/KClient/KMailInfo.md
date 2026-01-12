English | [中文](./KMailInfo.zh-CN.md)

# KMailInfo

Mail information object representing a single mail.

Notes:

- Obtained via `KMailClient:GetMailInfo()`

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `dwMailID` | `number` | Mail unique ID |
| `szSenderName` | `string` | Sender name |
| `szTitle` | `string` | Mail title |
| `bReadFlag` | `boolean` | Whether mail has been read |
| `bMoneyFlag` | `boolean` | Whether mail contains money |
| `bItemFlag` | `boolean` | Whether mail contains items |
| `bPayFlag` | `boolean` | Whether mail requires payment (COD) |
| `bGotContentFlag` | `boolean` | Whether content has been retrieved |
| `nMoney` | `number` | Money amount |
| `nAllItemPrice` | `number` | Total item price |

## Methods

[`GetItem`](#KMailInfo_GetItem)
[`RequestContent`](#KMailInfo_RequestContent)
[`GetText`](#KMailInfo_GetText)
[`GetLeftTime`](#KMailInfo_GetLeftTime)
[`GetType`](#KMailInfo_GetType)
[`Read`](#KMailInfo_Read)
[`TakeItem`](#KMailInfo_TakeItem)
[`TakeMoney`](#KMailInfo_TakeMoney)

---

* <h4 id="KMailInfo_GetItem">GetItem</h4>

Gets an item attachment from the mail.

 > ([`KGItem`](../KGameObject/KGItem.md) item) KMailInfo:GetItem(`number` nIndex)

* <h4 id="KMailInfo_RequestContent">RequestContent</h4>

Requests the mail content from server.

 > (`void`) KMailInfo:RequestContent()

* <h4 id="KMailInfo_GetText">GetText</h4>

Gets the mail text content.

 > (`string` szText) KMailInfo:GetText()

* <h4 id="KMailInfo_GetLeftTime">GetLeftTime</h4>

Gets the remaining time before mail expires.

 > (`number` nLeftTime) KMailInfo:GetLeftTime()

* <h4 id="KMailInfo_GetType">GetType</h4>

Gets the mail type.

 > (`number` nType) KMailInfo:GetType()

* <h4 id="KMailInfo_Read">Read</h4>

Marks the mail as read.

 > (`void`) KMailInfo:Read()

* <h4 id="KMailInfo_TakeItem">TakeItem</h4>

Takes an item attachment from the mail.

 > (`void`) KMailInfo:TakeItem(`number` nIndex)

* <h4 id="KMailInfo_TakeMoney">TakeMoney</h4>

Takes money from the mail.

 > (`void`) KMailInfo:TakeMoney()
