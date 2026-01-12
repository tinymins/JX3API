[English](./Logic.md) | 中文

# 逻辑函数

玩家、场景和目标操作的游戏逻辑函数。

## 玩家函数

[`GetClientPlayer`](#GetClientPlayer)
[`GetPlayer`](#GetPlayer)
[`GetPlayerID`](#GetPlayerID)
[`IsPlayer`](#IsPlayer)
[`GetClientTeam`](#GetClientTeam)
[`GetTeamClient`](#GetTeamClient)
[`GetTongClient`](#GetTongClient)
[`GetFellowshipCardClient`](#GetFellowshipCardClient)

## 场景函数

[`GetClientScene`](#GetClientScene)
[`GetScene`](#GetScene)
[`GetNpc`](#GetNpc)
[`IsNpc`](#IsNpc)
[`GetDoodad`](#GetDoodad)
[`IsDoodad`](#IsDoodad)

## 目标函数

[`GetTargetHandle`](#GetTargetHandle)
[`SetTarget`](#SetTarget)
[`GetControlPlayerID`](#GetControlPlayerID)

---

* <h4 id="GetClientPlayer">GetClientPlayer</h4>

获取客户端玩家对象（当前角色）。

 > ([`KPlayer`](./KGameObject/KPlayer.zh-CN.md) player) GetClientPlayer()

* <h4 id="GetPlayer">GetPlayer</h4>

根据 ID 获取玩家对象。

 > ([`KPlayer`](./KGameObject/KPlayer.zh-CN.md) player) GetPlayer(`number` dwPlayerID)

* <h4 id="GetPlayerID">GetPlayerID</h4>

从角色对象获取玩家 ID。

 > (`number` dwPlayerID) GetPlayerID(`KCharacter` character)

* <h4 id="IsPlayer">IsPlayer</h4>

检查 ID 是否属于玩家。

 > (`boolean` bIsPlayer) IsPlayer(`number` dwID)

* <h4 id="GetClientTeam">GetClientTeam</h4>

获取客户端队伍对象。

 > (`KTeam` team) GetClientTeam()

* <h4 id="GetTeamClient">GetTeamClient</h4>

获取队伍客户端对象。

 > ([`KTeamClient`](./KClient/KTeamClient.zh-CN.md) teamClient) GetTeamClient()

* <h4 id="GetTongClient">GetTongClient</h4>

获取帮会客户端对象。

 > ([`KTongClient`](./KClient/KTongClient.zh-CN.md) tongClient) GetTongClient()

* <h4 id="GetFellowshipCardClient">GetFellowshipCardClient</h4>

获取好友名片客户端对象。

 > ([`KFellowshipCardClient`](./KClient/KFellowshipCardClient.zh-CN.md) cardClient) GetFellowshipCardClient()

* <h4 id="GetClientScene">GetClientScene</h4>

获取客户端场景对象（当前地图）。

 > ([`KScene`](./KGameObject/KScene.zh-CN.md) scene) GetClientScene()

* <h4 id="GetScene">GetScene</h4>

获取场景对象。

 > ([`KScene`](./KGameObject/KScene.zh-CN.md) scene) GetScene()

* <h4 id="GetNpc">GetNpc</h4>

根据 ID 获取 NPC 对象。

 > ([`KNpc`](./KGameObject/KNpc.zh-CN.md) npc) GetNpc(`number` dwNpcID)

* <h4 id="IsNpc">IsNpc</h4>

检查 ID 是否属于 NPC。

 > (`boolean` bIsNpc) IsNpc(`number` dwID)

* <h4 id="GetDoodad">GetDoodad</h4>

根据 ID 获取 Doodad 对象。

 > ([`KDoodad`](./KGameObject/KDoodad.zh-CN.md) doodad) GetDoodad(`number` dwDoodadID)

* <h4 id="IsDoodad">IsDoodad</h4>

检查 ID 是否属于 Doodad。

 > (`boolean` bIsDoodad) IsDoodad(`number` dwID)

* <h4 id="GetTargetHandle">GetTargetHandle</h4>

获取当前目标句柄。

 > (`number` dwHandle) GetTargetHandle()

* <h4 id="SetTarget">SetTarget</h4>

设置当前目标。

 > (`void`) SetTarget(`number` nTargetType, `number` dwTargetID)

* <h4 id="GetControlPlayerID">GetControlPlayerID</h4>

获取被控制玩家的 ID。

 > (`number` dwPlayerID) GetControlPlayerID()

---

## 已禁用的函数

以下函数在源码中存在但已被注释，无法使用：

* <h4 id="GetNearbyDoodadList">~~GetNearbyDoodadList~~</h4>

⚠️ **已禁用** - 此函数已被注释。

```lua
-- 已注释
-- local tList = GetNearbyDoodadList()
```

* <h4 id="GetNearbyNpcList">~~GetNearbyNpcList~~</h4>

⚠️ **已禁用** - 此函数已被注释。

```lua
-- 已注释
-- local tList = GetNearbyNpcList()
```

* <h4 id="GetNearbyPlayerList">~~GetNearbyPlayerList~~</h4>

⚠️ **已禁用** - 此函数已被注释。

```lua
-- 已注释
-- local tList = GetNearbyPlayerList()
```
