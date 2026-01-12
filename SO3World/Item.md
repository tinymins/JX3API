English | [中文](./Item.zh-CN.md)

# Item Functions

Functions for item operations.

## Functions

[`GetItem`](#GetItem)
[`GetItemInfo`](#GetItemInfo)
[`GetItemTip`](#GetItemTip)
[`GetItemEnchantAttrib`](#GetItemEnchantAttrib)
[`GetItemRepairPrice`](#GetItemRepairPrice)

---

* <h4 id="GetItem">GetItem</h4>

Gets an item object by package and index.

 > ([`KGItem`](./KGameObject/KGItem.md) item) GetItem(`number` nPackage, `number` nIndex)

* <h4 id="GetItemInfo">GetItemInfo</h4>

Gets item information by item table type and ID.

 > ([`KGLuaItemInfo`](./KGameObject/KGLuaItemInfo.md) itemInfo) GetItemInfo(`number` nItemTableType, `number` nItemID)

* <h4 id="GetItemTip">GetItemTip</h4>

Gets the tooltip text for an item.

 > (`string` szTip) GetItemTip([`KGItem`](./KGameObject/KGItem.md) item)

* <h4 id="GetItemEnchantAttrib">GetItemEnchantAttrib</h4>

Gets enchant attributes for an item.

 > (`table` tAttrib) GetItemEnchantAttrib(`number` nEnchantID)

* <h4 id="GetItemRepairPrice">GetItemRepairPrice</h4>

Gets the repair price for an item.

 > (`number` nPrice) GetItemRepairPrice([`KGItem`](./KGameObject/KGItem.md) item)
