[English](./KSkill.md) | 中文

# KSkill（技能对象）

技能对象，包含技能信息和属性。

说明：

- 通过 `GetSkill()`、`GetPlayerSkill()`、`KPlayer:GetKungfuMount()` 获取

## 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `szSkillName` | `string` | 技能名称 |
| `dwSkillID` | `number` | 技能 ID |
| `dwMaxLevel` | `number` | 技能最大等级 |
| `nUIType` | `number` | UI 类型 |
| `dwBelongKungfu` | `number` | 所属心法 ID |
| `dwBelongSchool` | `number` | 所属门派 ID |
| `nCastMode` | `number` | 施放模式 |
| `dwWeaponRequest` | `number` | 需求武器类型 |
| `nCostItemType` | `number` | 消耗物品类型 |
| `nCostItemIndex` | `number` | 消耗物品索引 |
| `dwMountRequestType` | `number` | 挂载需求类型 |
| `dwMountRequestDetail` | `number` | 挂载需求详情 |
| `dwMountRequestDetailLevel` | `number` | 挂载需求详情等级 |
| `dwMountType` | `number` | 挂载类型 |
| `bIsMountAble` | `boolean` | 是否可作为心法挂载 |
| `bIsPassiveSkill` | `boolean` | 是否为被动技能 |
| `bIsChannelSkill` | `boolean` | 是否为引导技能 |
| `bIsExpSkill` | `boolean` | 是否为经验技能 |
| `bIsExactHit` | `boolean` | 是否必中 |
| `nEffectType` | `number` | 效果类型（参见 `SKILL_EFFECT_TYPE`） |
| `dwLevel` | `number` | 当前技能等级 |
| `dwLevelUpExp` | `number` | 升级所需经验 |
| `nPlayerLevelLimit` | `number` | 玩家等级限制 |
| `nCostLife` | `number` | 生命消耗 |
| `nCostMana` | `number` | 内力消耗 |
| `nCostManaBasePercent` | `number` | 内力消耗基础百分比 |
| `nCostRage` | `number` | 怒气消耗 |
| `nCostEnergy` | `number` | 能量消耗 |
| `nCostStamina` | `number` | 体力消耗 |
| `nCostTrain` | `number` | 修为消耗 |

## 已注释属性

以下属性在 API 中已被注释：

| 属性 | 类型 | 说明 |
|------|------|------|
| ~~`nPrepareFrames`~~ | `number` | 准备帧数（已禁用） |
| ~~`UITestCast`~~ | `function` | UI 测试施放（已禁用） |
