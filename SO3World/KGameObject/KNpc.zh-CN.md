[English](./KNpc.md) | 中文

# KNpc（NPC 对象）

NPC 对象，代表游戏中的非玩家角色。

说明：

- 通过 `GetNpc()`、`KPlayer:GetPet()` 获取
- NPC 名称可见性取决于 `CanSeeName()` 的结果

## 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `dwID` | `number` | NPC 唯一 ID |
| `nX` | `number` | X 坐标 |
| `nY` | `number` | Y 坐标 |
| `nZ` | `number` | Z 坐标 |
| `nFaceDirection` | `number` | 面向方向 |
| `szName` | `string` | NPC 名称（若 `CanSeeName()` 为 false 则返回空字符串） |
| `szTitle` | `string` | NPC 称号 |
| `dwForceID` | `number` | 势力 ID |
| `nLevel` | `number` | NPC 等级 |
| `dwTemplateID` | `number` | NPC 模板 ID |
| `dwModelID` | `number` | 模型 ID |
| `nTouchRange` | `number` | 交互范围 |
| `bDialogFlag` | `boolean` | 是否有对话 |
| `nGender` | `number` | 性别 |
| `nMoveState` | `number` | 移动状态（参见 `MOVE_STATE`） |
| `bFightState` | `boolean` | 是否处于战斗状态 |
| `dwEmployer` | `number` | 雇主玩家 ID（对于宠物） |
| `nCurrentLife` | `number` | 当前生命值 |
| `nMaxLife` | `number` | 最大生命值 |
| `nCurrentMana` | `number` | 当前内力值 |
| `nMaxMana` | `number` | 最大内力值 |
| `nCurrentRage` | `number` | 当前怒气值 |
| `nMaxRage` | `number` | 最大怒气值 |
| `nCurrentEnergy` | `number` | 当前能量值 |
| `nMaxEnergy` | `number` | 最大能量值 |
| `dwDropTargetPlayerID` | `number` | 掉落目标玩家 ID |

## 方法

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

## 已注释方法

| 方法 | 说明 |
|------|------|
| ~~`CastSkill`~~ | 施放技能（已禁用） |

---

* <h4 id="KNpc_GetScene">GetScene</h4>

获取 NPC 所在的场景。

 > ([`KScene`](./KScene.zh-CN.md) scene) KNpc:GetScene()

* <h4 id="KNpc_GetTarget">GetTarget</h4>

获取 NPC 当前的目标。

 > (`number` dwTargetType, `number` dwTargetID) KNpc:GetTarget()

* <h4 id="KNpc_GetMapID">GetMapID</h4>

获取 NPC 所在的地图 ID。

 > (`number` dwMapID) KNpc:GetMapID()

* <h4 id="KNpc_CanSeeName">CanSeeName</h4>

检查 NPC 名称是否对玩家可见。

 > (`boolean` bCanSee) KNpc:CanSeeName()

* <h4 id="KNpc_CanSeeLifeBar">CanSeeLifeBar</h4>

检查 NPC 血条是否可见。

 > (`boolean` bCanSee) KNpc:CanSeeLifeBar()

* <h4 id="KNpc_GetSkillOTActionState">GetSkillOTActionState</h4>

获取 NPC 当前的技能 OT 动作状态。

说明：
- 如果 NPC 是敌人且地图不是副本，则返回 nil

 > (`table` tState) KNpc:GetSkillOTActionState()

* <h4 id="KNpc_GetSkillPrepareState">GetSkillPrepareState</h4>

获取 NPC 的技能准备状态（旧接口，将被移除）。

 > (`table` tState) KNpc:GetSkillPrepareState()

* <h4 id="KNpc_GetAbsoluteCoordinate">GetAbsoluteCoordinate</h4>

获取 NPC 的绝对世界坐标。

 > (`number` nX, `number` nY, `number` nZ) KNpc:GetAbsoluteCoordinate()

* <h4 id="KNpc_GetNpcQuest">GetNpcQuest</h4>

获取与此 NPC 相关的任务信息。

 > (`table` tQuestInfo) KNpc:GetNpcQuest()

* <h4 id="KNpc_GetBuffCount">GetBuffCount</h4>

获取 NPC 身上的 Buff 数量。

 > (`number` nCount) KNpc:GetBuffCount()

* <h4 id="KNpc_GetBuff">GetBuff</h4>

根据索引获取 Buff 信息。

 > (`table` tBuff) KNpc:GetBuff(`number` nIndex)

* <h4 id="KNpc_CanDialog">CanDialog</h4>

检查玩家是否可以与此 NPC 对话。

 > (`boolean` bCanDialog) KNpc:CanDialog()

* <h4 id="KNpc_IsSelectable">IsSelectable</h4>

检查 NPC 是否可被选中。

 > (`boolean` bSelectable) KNpc:IsSelectable()

* <h4 id="KNpc_SetTarget">SetTarget</h4>

设置 NPC 的目标。

 > (`void`) KNpc:SetTarget(`number` dwTargetType, `number` dwTargetID)
