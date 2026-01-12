[English](./KTeamClient.md) | 中文

# KTeamClient（队伍客户端）

队伍客户端对象，用于管理队伍操作。

说明：

- 通过 `GetClientTeam()` 获取

## 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `dwTeamID` | `number` | 队伍 ID |
| `bSystem` | `boolean` | 是否为系统队伍 |
| `bTeamLeader` | `boolean` | 当前玩家是否为队长 |
| `nLootMode` | `number` | 分配模式（参见 `PARTY_LOOT_MODE`） |
| `nRollQuality` | `number` | Roll 品质阈值 |
| `nCamp` | `number` | 队伍阵营 |
| `dwDistributeMan` | `number` | 物品分配者玩家 ID |
| `dwFormationLeader` | `number` | 阵型领袖 ID |
| `nGroupNum` | `number` | 队伍中的小队数量 |
| `nInComeMoney` | `number` | 收入金钱（金团分配用） |

## 方法

[`GetGroupInfo`](#KTeamClient_GetGroupInfo)
[`GetMemberInfo`](#KTeamClient_GetMemberInfo)
[`GetAuthorityInfo`](#KTeamClient_GetAuthorityInfo)
[`GetTeamMark`](#KTeamClient_GetTeamMark)
[`GetMarkIndex`](#KTeamClient_GetMarkIndex)
[`IsPlayerInTeam`](#KTeamClient_IsPlayerInTeam)
[`GetMemberGroupIndex`](#KTeamClient_GetMemberGroupIndex)
[`SetTeamLootMode`](#KTeamClient_SetTeamLootMode)
[`SetTeamRollQuality`](#KTeamClient_SetTeamRollQuality)
[`ChangeMemberGroup`](#KTeamClient_ChangeMemberGroup)
[`SetTeamMark`](#KTeamClient_SetTeamMark)
[`GetTeamMemberList`](#KTeamClient_GetTeamMemberList)
[`GetTeamSize`](#KTeamClient_GetTeamSize)
[`SetTeamFormationLeader`](#KTeamClient_SetTeamFormationLeader)
[`GetClientTeamMemberName`](#KTeamClient_GetClientTeamMemberName)
[`SetAuthorityInfo`](#KTeamClient_SetAuthorityInfo)
[`TeamNotifySignpost`](#KTeamClient_TeamNotifySignpost)

---

* <h4 id="KTeamClient_GetGroupInfo">GetGroupInfo</h4>

根据小队索引获取小队信息。

 > (`table` tGroupInfo) KTeamClient:GetGroupInfo(`number` nGroupIndex)

返回值：
```lua
{
    MemberList = {dwMemberID1, dwMemberID2, ...}
}
```

* <h4 id="KTeamClient_GetMemberInfo">GetMemberInfo</h4>

根据玩家 ID 获取队员信息。

 > (`table` tMemberInfo) KTeamClient:GetMemberInfo(`number` dwMemberID)

返回值：
```lua
{
    szName = "玩家名称",
    dwID = 12345,
    nLevel = 120,
    dwSchoolID = 1,
    -- ... 其他队员数据
}
```

* <h4 id="KTeamClient_GetAuthorityInfo">GetAuthorityInfo</h4>

获取权限信息（队长、分配者等）。

 > (`number` dwPlayerID) KTeamClient:GetAuthorityInfo(`number` nAuthorityType)

* <h4 id="KTeamClient_GetTeamMark">GetTeamMark</h4>

获取团队标记信息。

 > (`table` tMark) KTeamClient:GetTeamMark(`number` nMarkIndex)

* <h4 id="KTeamClient_GetMarkIndex">GetMarkIndex</h4>

根据目标获取标记索引。

 > (`number` nMarkIndex) KTeamClient:GetMarkIndex(`number` dwTargetID)

* <h4 id="KTeamClient_IsPlayerInTeam">IsPlayerInTeam</h4>

检查玩家是否在队伍中。

 > (`boolean` bInTeam) KTeamClient:IsPlayerInTeam(`number` dwPlayerID)

* <h4 id="KTeamClient_GetMemberGroupIndex">GetMemberGroupIndex</h4>

获取队员所在的小队索引。

 > (`number` nGroupIndex) KTeamClient:GetMemberGroupIndex(`number` dwMemberID)

* <h4 id="KTeamClient_SetTeamLootMode">SetTeamLootMode</h4>

设置队伍分配模式。

 > (`void`) KTeamClient:SetTeamLootMode(`number` nLootMode)

* <h4 id="KTeamClient_SetTeamRollQuality">SetTeamRollQuality</h4>

设置 Roll 品质阈值。

 > (`void`) KTeamClient:SetTeamRollQuality(`number` nQuality)

* <h4 id="KTeamClient_ChangeMemberGroup">ChangeMemberGroup</h4>

将队员移动到其他小队。

 > (`void`) KTeamClient:ChangeMemberGroup(`number` dwMemberID, `number` nGroupIndex)

* <h4 id="KTeamClient_SetTeamMark">SetTeamMark</h4>

在目标上设置团队标记。

 > (`void`) KTeamClient:SetTeamMark(`number` nMarkIndex, `number` dwTargetID)

* <h4 id="KTeamClient_GetTeamMemberList">GetTeamMemberList</h4>

获取所有队员列表。

 > (`table` tMemberList) KTeamClient:GetTeamMemberList()

* <h4 id="KTeamClient_GetTeamSize">GetTeamSize</h4>

获取当前队伍人数。

 > (`number` nSize) KTeamClient:GetTeamSize()

* <h4 id="KTeamClient_SetTeamFormationLeader">SetTeamFormationLeader</h4>

设置阵型领袖。

 > (`void`) KTeamClient:SetTeamFormationLeader(`number` dwPlayerID)

* <h4 id="KTeamClient_GetClientTeamMemberName">GetClientTeamMemberName</h4>

根据 ID 获取队员名称。

 > (`string` szName) KTeamClient:GetClientTeamMemberName(`number` dwMemberID)

* <h4 id="KTeamClient_SetAuthorityInfo">SetAuthorityInfo</h4>

设置权限信息。

 > (`void`) KTeamClient:SetAuthorityInfo(`number` nAuthorityType, `number` dwPlayerID)

* <h4 id="KTeamClient_TeamNotifySignpost">TeamNotifySignpost</h4>

向队伍发送指示标记通知。

 > (`void`) KTeamClient:TeamNotifySignpost(`number` nX, `number` nY, `number` nZ)

---

## 被屏蔽的方法

以下方法在 addon 环境中被屏蔽，无法使用：

| 方法 | 说明 |
|------|------|
| `InviteJoinTeam` | ⚠️ 被屏蔽 - 邀请玩家加入队伍 |
