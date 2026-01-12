[English](./KTongClient.md) | 中文

# KTongClient（帮会客户端）

帮会客户端对象，用于管理帮会操作。

说明：

- 通过 `GetTongClient()` 获取

## 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `dwMaster` | `number` | 帮主玩家 ID |
| `nTotalWageRate` | `number` | 总工资比率 |
| `nLevel` | `number` | 帮会等级 |
| `nDevelopmentPoint` | `number` | 发展点数 |
| `nMaxMemberCount` | `number` | 最大成员数量 |
| `bCanModifyGroupWage` | `boolean` | 是否可修改职位工资 |
| `nCamp` | `number` | 帮会阵营 |
| `szTongName` | `string` | 帮会名称 |
| `szAnnouncement` | `string` | 帮会公告 |
| `szOnlineMessage` | `string` | 上线消息 |
| `szIntroduction` | `string` | 帮会简介 |
| `szRules` | `string` | 帮会规则 |
| `nState` | `number` | 帮会状态 |

## 方法

[`ApplyGetTongName`](#KTongClient_ApplyGetTongName)
[`ApplyTongInfo`](#KTongClient_ApplyTongInfo)
[`ApplyTongRoster`](#KTongClient_ApplyTongRoster)
[`GetMemberList`](#KTongClient_GetMemberList)
[`CheckBaseOperationGroup`](#KTongClient_CheckBaseOperationGroup)
[`ApplyRepertoryPage`](#KTongClient_ApplyRepertoryPage)
[`ApplyOpenRepertory`](#KTongClient_ApplyOpenRepertory)
[`ChangeMemberGroup`](#KTongClient_ChangeMemberGroup)
[`GetMemberCount`](#KTongClient_GetMemberCount)
[`GetMemberInfo`](#KTongClient_GetMemberInfo)
[`GetGroupInfo`](#KTongClient_GetGroupInfo)
[`GetRepertoryItem`](#KTongClient_GetRepertoryItem)

---

* <h4 id="KTongClient_ApplyGetTongName">ApplyGetTongName</h4>

请求获取帮会名称。

 > (`void`) KTongClient:ApplyGetTongName()

* <h4 id="KTongClient_ApplyTongInfo">ApplyTongInfo</h4>

请求获取帮会信息。

 > (`void`) KTongClient:ApplyTongInfo()

* <h4 id="KTongClient_ApplyTongRoster">ApplyTongRoster</h4>

请求获取帮会成员名册。

 > (`void`) KTongClient:ApplyTongRoster()

* <h4 id="KTongClient_GetMemberList">GetMemberList</h4>

获取帮会成员列表。

 > (`table` tMemberList) KTongClient:GetMemberList()

* <h4 id="KTongClient_CheckBaseOperationGroup">CheckBaseOperationGroup</h4>

检查某职位是否允许执行指定操作。

 > (`boolean` bAllowed) KTongClient:CheckBaseOperationGroup(`number` nOperation, `number` nGroupIndex)

* <h4 id="KTongClient_ApplyRepertoryPage">ApplyRepertoryPage</h4>

请求获取帮会仓库页面。

 > (`void`) KTongClient:ApplyRepertoryPage(`number` nPage)

* <h4 id="KTongClient_ApplyOpenRepertory">ApplyOpenRepertory</h4>

请求打开帮会仓库。

 > (`void`) KTongClient:ApplyOpenRepertory()

* <h4 id="KTongClient_ChangeMemberGroup">ChangeMemberGroup</h4>

更改成员职位。

 > (`void`) KTongClient:ChangeMemberGroup(`number` dwMemberID, `number` nGroupIndex)

* <h4 id="KTongClient_GetMemberCount">GetMemberCount</h4>

获取成员总数。

 > (`number` nCount) KTongClient:GetMemberCount()

* <h4 id="KTongClient_GetMemberInfo">GetMemberInfo</h4>

根据 ID 获取成员信息。

 > (`table` tMemberInfo) KTongClient:GetMemberInfo(`number` dwMemberID)

* <h4 id="KTongClient_GetGroupInfo">GetGroupInfo</h4>

获取职位信息。

 > (`table` tGroupInfo) KTongClient:GetGroupInfo(`number` nGroupIndex)

* <h4 id="KTongClient_GetRepertoryItem">GetRepertoryItem</h4>

从帮会仓库获取物品。

 > (`table` tItem) KTongClient:GetRepertoryItem(`number` nPage, `number` nIndex)
