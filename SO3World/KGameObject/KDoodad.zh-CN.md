[English](./KDoodad.md) | 中文

# KDoodad（交互物件）

交互物件对象，代表游戏世界中的可交互物体（战利品、任务物件等）。

说明：

- 通过 `GetDoodad()` 获取

## 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `dwID` | `number` | 物件唯一 ID |
| `nX` | `number` | X 坐标 |
| `nY` | `number` | Y 坐标 |
| `nZ` | `number` | Z 坐标 |
| `szName` | `string` | 物件名称 |
| `dwTemplateID` | `number` | 物件模板 ID |
| `nKind` | `number` | 物件类型（参见 `DOODAD_KIND`） |

## 方法

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

获取物件所在的场景。

 > ([`KScene`](./KScene.zh-CN.md) scene) KDoodad:GetScene()

* <h4 id="KDoodad_CanLoot">CanLoot</h4>

检查物件是否可被拾取。

 > (`boolean` bCanLoot) KDoodad:CanLoot()

* <h4 id="KDoodad_HaveQuest">HaveQuest</h4>

检查物件是否与任务相关。

 > (`boolean` bHaveQuest) KDoodad:HaveQuest()

* <h4 id="KDoodad_CanSit">CanSit</h4>

检查玩家是否可以坐在此物件上。

 > (`boolean` bCanSit) KDoodad:CanSit()

* <h4 id="KDoodad_GetLooterList">GetLooterList</h4>

获取可拾取的玩家列表。

 > (`table` tLooterList) KDoodad:GetLooterList()

* <h4 id="KDoodad_DistributeItem">DistributeItem</h4>

分配战利品中的物品。

 > (`void`) KDoodad:DistributeItem(`number` nIndex, `number` dwPlayerID)

* <h4 id="KDoodad_IsSelectable">IsSelectable</h4>

检查物件是否可被选中。

 > (`boolean` bSelectable) KDoodad:IsSelectable()

* <h4 id="KDoodad_GetRecipeID">GetRecipeID</h4>

获取与此物件关联的配方 ID（用于采集）。

 > (`number` dwRecipeID) KDoodad:GetRecipeID()

* <h4 id="KDoodad_GetAbsoluteCoordinate">GetAbsoluteCoordinate</h4>

获取物件的绝对世界坐标。

 > (`number` nX, `number` nY, `number` nZ) KDoodad:GetAbsoluteCoordinate()

* <h4 id="KDoodad_CanDialog">CanDialog</h4>

检查玩家是否可以与此物件交互/对话。

 > (`boolean` bCanDialog) KDoodad:CanDialog()

* <h4 id="KDoodad_GetLootItem">GetLootItem</h4>

根据索引获取战利品物品。

 > ([`KGItem`](./KGItem.zh-CN.md) item) KDoodad:GetLootItem(`number` nIndex)

* <h4 id="KDoodad_GetLootMoney">GetLootMoney</h4>

获取战利品中的金钱数量。

 > (`number` nMoney) KDoodad:GetLootMoney()
