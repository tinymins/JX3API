English | [中文](./KScene.zh-CN.md)

# KScene

Scene/Map object representing the current game scene.

Notes:

- Obtained via `GetScene()`, `KPlayer:GetScene()`, `KNpc:GetScene()`, `KDoodad:GetScene()`

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `dwID` | `number` | Scene ID |
| `nType` | `number` | Scene type (see `MAP_TYPE`) |
| `szName` | `string` | Scene name |
| `bCanTongWar` | `boolean` | Whether guild war is allowed |
| `bCanPK` | `boolean` | Whether PK is allowed |
| `bCanDuel` | `boolean` | Whether duel is allowed |
| `szDisplayName` | `string` | Display name |
| `dwMapID` | `number` | Map ID |
| `nCopyIndex` | `number` | Copy index (for instances) |
| `bReviveInSitu` | `boolean` | Whether can revive in place |
| `nInFightPlayerCount` | `number` | Number of players in combat |
| `bCampType` | `number` | Camp type (see `MAP_CAMP_TYPE`) |
| `bIsArenaMap` | `boolean` | Whether is arena map |

## Methods

[`TimeLimitationBindItemGetLeftTime`](#KScene_TimeLimitationBindItemGetLeftTime)
[`GetArenaPlayerCount`](#KScene_GetArenaPlayerCount)
[`GetArenaPlayer`](#KScene_GetArenaPlayer)

---

* <h4 id="KScene_TimeLimitationBindItemGetLeftTime">TimeLimitationBindItemGetLeftTime</h4>

Gets the remaining time for time-limited bind items.

 > (`number` nLeftTime) KScene:TimeLimitationBindItemGetLeftTime()

* <h4 id="KScene_GetArenaPlayerCount">GetArenaPlayerCount</h4>

Gets the number of players in arena.

 > (`number` nCount) KScene:GetArenaPlayerCount()

* <h4 id="KScene_GetArenaPlayer">GetArenaPlayer</h4>

Gets arena player information by index.

 > (`table` tPlayerInfo) KScene:GetArenaPlayer(`number` nIndex)
