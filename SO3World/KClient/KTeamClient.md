English | [中文](./KTeamClient.zh-CN.md)

# KTeamClient

Team/Party client object for managing party operations.

Notes:

- Obtained via `GetClientTeam()`

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `dwTeamID` | `number` | Team ID |
| `bSystem` | `boolean` | Whether is system team |
| `bTeamLeader` | `boolean` | Whether current player is team leader |
| `nLootMode` | `number` | Loot mode (see `PARTY_LOOT_MODE`) |
| `nRollQuality` | `number` | Roll quality threshold |
| `nCamp` | `number` | Team camp |
| `dwDistributeMan` | `number` | Item distributor player ID |
| `dwFormationLeader` | `number` | Formation leader ID |
| `nGroupNum` | `number` | Number of groups in team |
| `nInComeMoney` | `number` | Income money (for gold distribution) |

## Methods

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

Gets group information by group index.

 > (`table` tGroupInfo) KTeamClient:GetGroupInfo(`number` nGroupIndex)

Returns:
```lua
{
    MemberList = {dwMemberID1, dwMemberID2, ...}
}
```

* <h4 id="KTeamClient_GetMemberInfo">GetMemberInfo</h4>

Gets member information by player ID.

 > (`table` tMemberInfo) KTeamClient:GetMemberInfo(`number` dwMemberID)

Returns:
```lua
{
    szName = "PlayerName",
    dwID = 12345,
    nLevel = 120,
    dwSchoolID = 1,
    -- ... other member data
}
```

* <h4 id="KTeamClient_GetAuthorityInfo">GetAuthorityInfo</h4>

Gets authority information (leader, distributor, etc.).

 > (`number` dwPlayerID) KTeamClient:GetAuthorityInfo(`number` nAuthorityType)

* <h4 id="KTeamClient_GetTeamMark">GetTeamMark</h4>

Gets team mark information.

 > (`table` tMark) KTeamClient:GetTeamMark(`number` nMarkIndex)

* <h4 id="KTeamClient_GetMarkIndex">GetMarkIndex</h4>

Gets mark index by target.

 > (`number` nMarkIndex) KTeamClient:GetMarkIndex(`number` dwTargetID)

* <h4 id="KTeamClient_IsPlayerInTeam">IsPlayerInTeam</h4>

Checks if a player is in the team.

 > (`boolean` bInTeam) KTeamClient:IsPlayerInTeam(`number` dwPlayerID)

* <h4 id="KTeamClient_GetMemberGroupIndex">GetMemberGroupIndex</h4>

Gets the group index of a team member.

 > (`number` nGroupIndex) KTeamClient:GetMemberGroupIndex(`number` dwMemberID)

* <h4 id="KTeamClient_SetTeamLootMode">SetTeamLootMode</h4>

Sets the team loot mode.

 > (`void`) KTeamClient:SetTeamLootMode(`number` nLootMode)

* <h4 id="KTeamClient_SetTeamRollQuality">SetTeamRollQuality</h4>

Sets the roll quality threshold.

 > (`void`) KTeamClient:SetTeamRollQuality(`number` nQuality)

* <h4 id="KTeamClient_ChangeMemberGroup">ChangeMemberGroup</h4>

Changes a member to a different group.

 > (`void`) KTeamClient:ChangeMemberGroup(`number` dwMemberID, `number` nGroupIndex)

* <h4 id="KTeamClient_SetTeamMark">SetTeamMark</h4>

Sets a team mark on a target.

 > (`void`) KTeamClient:SetTeamMark(`number` nMarkIndex, `number` dwTargetID)

* <h4 id="KTeamClient_GetTeamMemberList">GetTeamMemberList</h4>

Gets the list of all team members.

 > (`table` tMemberList) KTeamClient:GetTeamMemberList()

* <h4 id="KTeamClient_GetTeamSize">GetTeamSize</h4>

Gets the current team size.

 > (`number` nSize) KTeamClient:GetTeamSize()

* <h4 id="KTeamClient_SetTeamFormationLeader">SetTeamFormationLeader</h4>

Sets the formation leader.

 > (`void`) KTeamClient:SetTeamFormationLeader(`number` dwPlayerID)

* <h4 id="KTeamClient_GetClientTeamMemberName">GetClientTeamMemberName</h4>

Gets team member name by ID.

 > (`string` szName) KTeamClient:GetClientTeamMemberName(`number` dwMemberID)

* <h4 id="KTeamClient_SetAuthorityInfo">SetAuthorityInfo</h4>

Sets authority information.

 > (`void`) KTeamClient:SetAuthorityInfo(`number` nAuthorityType, `number` dwPlayerID)

* <h4 id="KTeamClient_TeamNotifySignpost">TeamNotifySignpost</h4>

Sends a signpost notification to team.

 > (`void`) KTeamClient:TeamNotifySignpost(`number` nX, `number` nY, `number` nZ)

---

## Shielded Methods

The following methods are blocked in addon environment and cannot be used:

| Method | Description |
|--------|-------------|
| `InviteJoinTeam` | ⚠️ Blocked - Invite player to join team |
