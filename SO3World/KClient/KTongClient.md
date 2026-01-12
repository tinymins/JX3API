English | [中文](./KTongClient.zh-CN.md)

# KTongClient

Guild client object for managing guild operations.

Notes:

- Obtained via `GetTongClient()`

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `dwMaster` | `number` | Guild master player ID |
| `nTotalWageRate` | `number` | Total wage rate |
| `nLevel` | `number` | Guild level |
| `nDevelopmentPoint` | `number` | Development points |
| `nMaxMemberCount` | `number` | Maximum member count |
| `bCanModifyGroupWage` | `boolean` | Whether group wage can be modified |
| `nCamp` | `number` | Guild camp |
| `szTongName` | `string` | Guild name |
| `szAnnouncement` | `string` | Guild announcement |
| `szOnlineMessage` | `string` | Online message |
| `szIntroduction` | `string` | Guild introduction |
| `szRules` | `string` | Guild rules |
| `nState` | `number` | Guild state |

## Methods

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

Requests the guild name.

 > (`void`) KTongClient:ApplyGetTongName()

* <h4 id="KTongClient_ApplyTongInfo">ApplyTongInfo</h4>

Requests guild information.

 > (`void`) KTongClient:ApplyTongInfo()

* <h4 id="KTongClient_ApplyTongRoster">ApplyTongRoster</h4>

Requests guild roster.

 > (`void`) KTongClient:ApplyTongRoster()

* <h4 id="KTongClient_GetMemberList">GetMemberList</h4>

Gets the list of guild members.

 > (`table` tMemberList) KTongClient:GetMemberList()

* <h4 id="KTongClient_CheckBaseOperationGroup">CheckBaseOperationGroup</h4>

Checks if base operation is allowed for a group.

 > (`boolean` bAllowed) KTongClient:CheckBaseOperationGroup(`number` nOperation, `number` nGroupIndex)

* <h4 id="KTongClient_ApplyRepertoryPage">ApplyRepertoryPage</h4>

Requests a repertory (guild bank) page.

 > (`void`) KTongClient:ApplyRepertoryPage(`number` nPage)

* <h4 id="KTongClient_ApplyOpenRepertory">ApplyOpenRepertory</h4>

Requests to open the repertory.

 > (`void`) KTongClient:ApplyOpenRepertory()

* <h4 id="KTongClient_ChangeMemberGroup">ChangeMemberGroup</h4>

Changes a member's group (rank).

 > (`void`) KTongClient:ChangeMemberGroup(`number` dwMemberID, `number` nGroupIndex)

* <h4 id="KTongClient_GetMemberCount">GetMemberCount</h4>

Gets the total member count.

 > (`number` nCount) KTongClient:GetMemberCount()

* <h4 id="KTongClient_GetMemberInfo">GetMemberInfo</h4>

Gets member information by ID.

 > (`table` tMemberInfo) KTongClient:GetMemberInfo(`number` dwMemberID)

* <h4 id="KTongClient_GetGroupInfo">GetGroupInfo</h4>

Gets group (rank) information.

 > (`table` tGroupInfo) KTongClient:GetGroupInfo(`number` nGroupIndex)

* <h4 id="KTongClient_GetRepertoryItem">GetRepertoryItem</h4>

Gets an item from the repertory (guild bank).

 > (`table` tItem) KTongClient:GetRepertoryItem(`number` nPage, `number` nIndex)
