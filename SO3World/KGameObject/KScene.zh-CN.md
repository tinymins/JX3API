[English](./KScene.md) | 中文

# KScene（场景对象）

场景/地图对象，代表当前游戏场景。

说明：

- 通过 `GetScene()`、`KPlayer:GetScene()`、`KNpc:GetScene()`、`KDoodad:GetScene()` 获取

## 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `dwID` | `number` | 场景 ID |
| `nType` | `number` | 场景类型（参见 `MAP_TYPE`） |
| `szName` | `string` | 场景名称 |
| `bCanTongWar` | `boolean` | 是否允许帮会战 |
| `bCanPK` | `boolean` | 是否允许 PK |
| `bCanDuel` | `boolean` | 是否允许切磋 |
| `szDisplayName` | `string` | 显示名称 |
| `dwMapID` | `number` | 地图 ID |
| `nCopyIndex` | `number` | 副本索引 |
| `bReviveInSitu` | `boolean` | 是否可原地复活 |
| `nInFightPlayerCount` | `number` | 战斗中的玩家数量 |
| `bCampType` | `number` | 阵营类型（参见 `MAP_CAMP_TYPE`） |
| `bIsArenaMap` | `boolean` | 是否为竞技场地图 |

## 方法

[`TimeLimitationBindItemGetLeftTime`](#KScene_TimeLimitationBindItemGetLeftTime)
[`GetArenaPlayerCount`](#KScene_GetArenaPlayerCount)
[`GetArenaPlayer`](#KScene_GetArenaPlayer)

---

* <h4 id="KScene_TimeLimitationBindItemGetLeftTime">TimeLimitationBindItemGetLeftTime</h4>

获取限时绑定物品的剩余时间。

 > (`number` nLeftTime) KScene:TimeLimitationBindItemGetLeftTime()

* <h4 id="KScene_GetArenaPlayerCount">GetArenaPlayerCount</h4>

获取竞技场中的玩家数量。

 > (`number` nCount) KScene:GetArenaPlayerCount()

* <h4 id="KScene_GetArenaPlayer">GetArenaPlayer</h4>

根据索引获取竞技场玩家信息。

 > (`table` tPlayerInfo) KScene:GetArenaPlayer(`number` nIndex)
