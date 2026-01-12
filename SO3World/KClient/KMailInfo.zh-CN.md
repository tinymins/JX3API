[English](./KMailInfo.md) | 中文

# KMailInfo（邮件信息）

邮件信息对象，代表单封邮件。

说明：

- 通过 `KMailClient:GetMailInfo()` 获取

## 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `dwMailID` | `number` | 邮件唯一 ID |
| `szSenderName` | `string` | 发件人名称 |
| `szTitle` | `string` | 邮件标题 |
| `bReadFlag` | `boolean` | 邮件是否已读 |
| `bMoneyFlag` | `boolean` | 邮件是否包含金钱 |
| `bItemFlag` | `boolean` | 邮件是否包含物品 |
| `bPayFlag` | `boolean` | 邮件是否需要付款（到付） |
| `bGotContentFlag` | `boolean` | 是否已获取邮件内容 |
| `nMoney` | `number` | 金钱数量 |
| `nAllItemPrice` | `number` | 物品总价 |

## 方法

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

从邮件获取附件物品。

 > ([`KGItem`](../KGameObject/KGItem.zh-CN.md) item) KMailInfo:GetItem(`number` nIndex)

* <h4 id="KMailInfo_RequestContent">RequestContent</h4>

从服务器请求邮件内容。

 > (`void`) KMailInfo:RequestContent()

* <h4 id="KMailInfo_GetText">GetText</h4>

获取邮件文本内容。

 > (`string` szText) KMailInfo:GetText()

* <h4 id="KMailInfo_GetLeftTime">GetLeftTime</h4>

获取邮件过期前的剩余时间。

 > (`number` nLeftTime) KMailInfo:GetLeftTime()

* <h4 id="KMailInfo_GetType">GetType</h4>

获取邮件类型。

 > (`number` nType) KMailInfo:GetType()

* <h4 id="KMailInfo_Read">Read</h4>

将邮件标记为已读。

 > (`void`) KMailInfo:Read()

* <h4 id="KMailInfo_TakeItem">TakeItem</h4>

从邮件中取走附件物品。

 > (`void`) KMailInfo:TakeItem(`number` nIndex)

* <h4 id="KMailInfo_TakeMoney">TakeMoney</h4>

从邮件中取走金钱。

 > (`void`) KMailInfo:TakeMoney()
