English | [中文](./KSkill.zh-CN.md)

# KSkill

Skill object containing skill information and attributes.

Notes:

- Obtained via `GetSkill()`, `GetPlayerSkill()`, `KPlayer:GetKungfuMount()`

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `szSkillName` | `string` | Skill name |
| `dwSkillID` | `number` | Skill ID |
| `dwMaxLevel` | `number` | Maximum skill level |
| `nUIType` | `number` | UI type |
| `dwBelongKungfu` | `number` | Belong kungfu ID |
| `dwBelongSchool` | `number` | Belong school ID |
| `nCastMode` | `number` | Cast mode |
| `dwWeaponRequest` | `number` | Required weapon type |
| `nCostItemType` | `number` | Cost item type |
| `nCostItemIndex` | `number` | Cost item index |
| `dwMountRequestType` | `number` | Mount request type |
| `dwMountRequestDetail` | `number` | Mount request detail |
| `dwMountRequestDetailLevel` | `number` | Mount request detail level |
| `dwMountType` | `number` | Mount type |
| `bIsMountAble` | `boolean` | Whether can be mounted (as kungfu) |
| `bIsPassiveSkill` | `boolean` | Whether is passive skill |
| `bIsChannelSkill` | `boolean` | Whether is channel skill |
| `bIsExpSkill` | `boolean` | Whether is exp skill |
| `bIsExactHit` | `boolean` | Whether is exact hit |
| `nEffectType` | `number` | Effect type (see `SKILL_EFFECT_TYPE`) |
| `dwLevel` | `number` | Current skill level |
| `dwLevelUpExp` | `number` | Experience needed to level up |
| `nPlayerLevelLimit` | `number` | Player level limit |
| `nCostLife` | `number` | Life cost |
| `nCostMana` | `number` | Mana cost |
| `nCostManaBasePercent` | `number` | Mana cost base percent |
| `nCostRage` | `number` | Rage cost |
| `nCostEnergy` | `number` | Energy cost |
| `nCostStamina` | `number` | Stamina cost |
| `nCostTrain` | `number` | Train cost |

## Commented Properties

The following properties are commented out in the API:

| Property | Type | Description |
|----------|------|-------------|
| ~~`nPrepareFrames`~~ | `number` | Prepare frames (disabled) |
| ~~`UITestCast`~~ | `function` | UI test cast (disabled) |
