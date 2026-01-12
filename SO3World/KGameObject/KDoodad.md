English | [中文](./KDoodad.zh-CN.md)

# KDoodad

Doodad object representing interactive objects in the game world (loot, quest objects, etc.).

Notes:

- Obtained via `GetDoodad()`

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `dwID` | `number` | Doodad unique ID |
| `nX` | `number` | X coordinate |
| `nY` | `number` | Y coordinate |
| `nZ` | `number` | Z coordinate |
| `szName` | `string` | Doodad name |
| `dwTemplateID` | `number` | Doodad template ID |
| `nKind` | `number` | Doodad kind (see `DOODAD_KIND`) |

## Methods

[`GetScene`](#KDoodad_GetScene)
[`CanLoot`](#KDoodad_CanLoot)
[`HaveQuest`](#KDoodad_HaveQuest)
[`CanSit`](#KDoodad_CanSit)
[`GetLooterList`](#KDoodad_GetLooterList)
[`DistributeItem`](#KDoodad_DistributeItem)
[`IsSelectable`](#KDoodad_IsSelectable)
[`GetRecipeID`](#KDoodad_GetRecipeID)
[`GetAbsoluteCoordinate`](#KDoodad_GetAbsoluteCoordinate)
[`CanDialog`](#KDoodad_CanDialog)
[`GetLootItem`](#KDoodad_GetLootItem)
[`GetLootMoney`](#KDoodad_GetLootMoney)

---

* <h4 id="KDoodad_GetScene">GetScene</h4>

Gets the scene where the doodad is located.

 > ([`KScene`](./KScene.md) scene) KDoodad:GetScene()

* <h4 id="KDoodad_CanLoot">CanLoot</h4>

Checks if the doodad can be looted.

 > (`boolean` bCanLoot) KDoodad:CanLoot()

* <h4 id="KDoodad_HaveQuest">HaveQuest</h4>

Checks if the doodad is related to a quest.

 > (`boolean` bHaveQuest) KDoodad:HaveQuest()

* <h4 id="KDoodad_CanSit">CanSit</h4>

Checks if the player can sit on this doodad.

 > (`boolean` bCanSit) KDoodad:CanSit()

* <h4 id="KDoodad_GetLooterList">GetLooterList</h4>

Gets the list of players who can loot.

 > (`table` tLooterList) KDoodad:GetLooterList()

* <h4 id="KDoodad_DistributeItem">DistributeItem</h4>

Distributes an item from loot.

 > (`void`) KDoodad:DistributeItem(`number` nIndex, `number` dwPlayerID)

* <h4 id="KDoodad_IsSelectable">IsSelectable</h4>

Checks if the doodad is selectable.

 > (`boolean` bSelectable) KDoodad:IsSelectable()

* <h4 id="KDoodad_GetRecipeID">GetRecipeID</h4>

Gets the recipe ID associated with this doodad (for gathering).

 > (`number` dwRecipeID) KDoodad:GetRecipeID()

* <h4 id="KDoodad_GetAbsoluteCoordinate">GetAbsoluteCoordinate</h4>

Gets the doodad's absolute world coordinates.

 > (`number` nX, `number` nY, `number` nZ) KDoodad:GetAbsoluteCoordinate()

* <h4 id="KDoodad_CanDialog">CanDialog</h4>

Checks if the player can interact/dialog with this doodad.

 > (`boolean` bCanDialog) KDoodad:CanDialog()

* <h4 id="KDoodad_GetLootItem">GetLootItem</h4>

Gets a loot item by index.

 > ([`KGItem`](./KGItem.md) item) KDoodad:GetLootItem(`number` nIndex)

* <h4 id="KDoodad_GetLootMoney">GetLootMoney</h4>

Gets the amount of money in the loot.

 > (`number` nMoney) KDoodad:GetLootMoney()
