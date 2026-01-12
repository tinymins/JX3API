English | [中文](./KNpc.zh-CN.md)

# KNpc

NPC object representing non-player characters in the game.

Notes:

- Obtained via `GetNpc()`, `KPlayer:GetPet()`
- NPC name visibility depends on `CanSeeName()` result

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `dwID` | `number` | NPC unique ID |
| `nX` | `number` | X coordinate |
| `nY` | `number` | Y coordinate |
| `nZ` | `number` | Z coordinate |
| `nFaceDirection` | `number` | Face direction |
| `szName` | `string` | NPC name (returns empty string if `CanSeeName()` is false) |
| `szTitle` | `string` | NPC title |
| `dwForceID` | `number` | Force ID |
| `nLevel` | `number` | NPC level |
| `dwTemplateID` | `number` | NPC template ID |
| `dwModelID` | `number` | Model ID |
| `nTouchRange` | `number` | Touch/interact range |
| `bDialogFlag` | `boolean` | Whether has dialog |
| `nGender` | `number` | Gender |
| `nMoveState` | `number` | Move state (see `MOVE_STATE`) |
| `bFightState` | `boolean` | Whether in combat |
| `dwEmployer` | `number` | Employer player ID (for pets) |
| `nCurrentLife` | `number` | Current life |
| `nMaxLife` | `number` | Maximum life |
| `nCurrentMana` | `number` | Current mana |
| `nMaxMana` | `number` | Maximum mana |
| `nCurrentRage` | `number` | Current rage |
| `nMaxRage` | `number` | Maximum rage |
| `nCurrentEnergy` | `number` | Current energy |
| `nMaxEnergy` | `number` | Maximum energy |
| `dwDropTargetPlayerID` | `number` | Drop target player ID |

## Methods

[`GetScene`](#KNpc_GetScene)
[`GetTarget`](#KNpc_GetTarget)
[`GetMapID`](#KNpc_GetMapID)
[`CanSeeName`](#KNpc_CanSeeName)
[`CanSeeLifeBar`](#KNpc_CanSeeLifeBar)
[`GetSkillOTActionState`](#KNpc_GetSkillOTActionState)
[`GetSkillPrepareState`](#KNpc_GetSkillPrepareState)
[`GetAbsoluteCoordinate`](#KNpc_GetAbsoluteCoordinate)
[`GetNpcQuest`](#KNpc_GetNpcQuest)
[`GetBuffCount`](#KNpc_GetBuffCount)
[`GetBuff`](#KNpc_GetBuff)
[`CanDialog`](#KNpc_CanDialog)
[`IsSelectable`](#KNpc_IsSelectable)
[`SetTarget`](#KNpc_SetTarget)

## Commented Methods

| Method | Description |
|--------|-------------|
| ~~`CastSkill`~~ | Cast skill (disabled) |

---

* <h4 id="KNpc_GetScene">GetScene</h4>

Gets the scene where the NPC is located.

 > ([`KScene`](./KScene.md) scene) KNpc:GetScene()

* <h4 id="KNpc_GetTarget">GetTarget</h4>

Gets the NPC's current target.

 > (`number` dwTargetType, `number` dwTargetID) KNpc:GetTarget()

* <h4 id="KNpc_GetMapID">GetMapID</h4>

Gets the map ID where the NPC is located.

 > (`number` dwMapID) KNpc:GetMapID()

* <h4 id="KNpc_CanSeeName">CanSeeName</h4>

Checks if the NPC name is visible to the player.

 > (`boolean` bCanSee) KNpc:CanSeeName()

* <h4 id="KNpc_CanSeeLifeBar">CanSeeLifeBar</h4>

Checks if the NPC life bar is visible.

 > (`boolean` bCanSee) KNpc:CanSeeLifeBar()

* <h4 id="KNpc_GetSkillOTActionState">GetSkillOTActionState</h4>

Gets the NPC's current skill OT action state.

Notes:
- Returns nil if the NPC is an enemy and the map is not a dungeon

 > (`table` tState) KNpc:GetSkillOTActionState()

* <h4 id="KNpc_GetSkillPrepareState">GetSkillPrepareState</h4>

Gets the NPC's skill prepare state (legacy, will be removed).

 > (`table` tState) KNpc:GetSkillPrepareState()

* <h4 id="KNpc_GetAbsoluteCoordinate">GetAbsoluteCoordinate</h4>

Gets the NPC's absolute world coordinates.

 > (`number` nX, `number` nY, `number` nZ) KNpc:GetAbsoluteCoordinate()

* <h4 id="KNpc_GetNpcQuest">GetNpcQuest</h4>

Gets quest information related to this NPC.

 > (`table` tQuestInfo) KNpc:GetNpcQuest()

* <h4 id="KNpc_GetBuffCount">GetBuffCount</h4>

Gets the number of buffs on the NPC.

 > (`number` nCount) KNpc:GetBuffCount()

* <h4 id="KNpc_GetBuff">GetBuff</h4>

Gets buff information by index.

 > (`table` tBuff) KNpc:GetBuff(`number` nIndex)

* <h4 id="KNpc_CanDialog">CanDialog</h4>

Checks if the player can dialog with this NPC.

 > (`boolean` bCanDialog) KNpc:CanDialog()

* <h4 id="KNpc_IsSelectable">IsSelectable</h4>

Checks if the NPC is selectable.

 > (`boolean` bSelectable) KNpc:IsSelectable()

* <h4 id="KNpc_SetTarget">SetTarget</h4>

Sets the NPC's target.

 > (`void`) KNpc:SetTarget(`number` dwTargetType, `number` dwTargetID)
