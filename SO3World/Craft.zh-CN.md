[English](./Craft.md) | 中文

# 生活技能函数

生活技能操作相关函数。

## 函数

[`GetCraftRecipe`](#GetCraftRecipe)
[`GetCraftInfo`](#GetCraftInfo)
[`GetProfessionInfo`](#GetProfessionInfo)
[`CanCraft`](#CanCraft)
[`DoCraft`](#DoCraft)
[`GetCraftSkillLevel`](#GetCraftSkillLevel)

---

* <h4 id="GetCraftRecipe">GetCraftRecipe</h4>

获取制作配方信息。

 > (`table` tRecipe) GetCraftRecipe(`number` nCraftID, `number` nRecipeID)

* <h4 id="GetCraftInfo">GetCraftInfo</h4>

获取制作信息。

 > (`table` tCraftInfo) GetCraftInfo(`number` nCraftID)

* <h4 id="GetProfessionInfo">GetProfessionInfo</h4>

获取职业信息。

 > (`table` tProfessionInfo) GetProfessionInfo(`number` nProfessionID)

* <h4 id="CanCraft">CanCraft</h4>

检查是否可以执行制作配方。

 > (`boolean` bCan, `string` szReason) CanCraft(`number` nCraftID, `number` nRecipeID)

* <h4 id="DoCraft">DoCraft</h4>

执行制作配方。

 > (`void`) DoCraft(`number` nCraftID, `number` nRecipeID)

* <h4 id="GetCraftSkillLevel">GetCraftSkillLevel</h4>

获取玩家的制作技能等级。

 > (`number` nLevel, `number` nMaxLevel) GetCraftSkillLevel(`number` nCraftID)
