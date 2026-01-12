English | [中文](./Craft.zh-CN.md)

# Craft Functions

Functions for crafting (life skills) operations.

## Functions

[`GetCraftRecipe`](#GetCraftRecipe)
[`GetCraftInfo`](#GetCraftInfo)
[`GetProfessionInfo`](#GetProfessionInfo)
[`CanCraft`](#CanCraft)
[`DoCraft`](#DoCraft)
[`GetCraftSkillLevel`](#GetCraftSkillLevel)

---

* <h4 id="GetCraftRecipe">GetCraftRecipe</h4>

Gets craft recipe information.

 > (`table` tRecipe) GetCraftRecipe(`number` nCraftID, `number` nRecipeID)

* <h4 id="GetCraftInfo">GetCraftInfo</h4>

Gets craft information.

 > (`table` tCraftInfo) GetCraftInfo(`number` nCraftID)

* <h4 id="GetProfessionInfo">GetProfessionInfo</h4>

Gets profession information.

 > (`table` tProfessionInfo) GetProfessionInfo(`number` nProfessionID)

* <h4 id="CanCraft">CanCraft</h4>

Checks if a craft recipe can be performed.

 > (`boolean` bCan, `string` szReason) CanCraft(`number` nCraftID, `number` nRecipeID)

* <h4 id="DoCraft">DoCraft</h4>

Performs a craft recipe.

 > (`void`) DoCraft(`number` nCraftID, `number` nRecipeID)

* <h4 id="GetCraftSkillLevel">GetCraftSkillLevel</h4>

Gets the player's craft skill level.

 > (`number` nLevel, `number` nMaxLevel) GetCraftSkillLevel(`number` nCraftID)
