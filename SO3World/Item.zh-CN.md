[English](./Item.md) | 中文

# 物品函数

物品操作相关函数。

## 函数

[`GetItem`](#GetItem)
[`GetItemInfo`](#GetItemInfo)
[`GetItemTip`](#GetItemTip)
[`GetItemEnchantAttrib`](#GetItemEnchantAttrib)
[`GetItemRepairPrice`](#GetItemRepairPrice)

---

* <h4 id="GetItem">GetItem</h4>

根据背包和索引获取物品对象。

 > ([`KGItem`](./KGameObject/KGItem.zh-CN.md) item) GetItem(`number` nPackage, `number` nIndex)

* <h4 id="GetItemInfo">GetItemInfo</h4>

根据物品表类型和 ID 获取物品信息。

 > ([`KGLuaItemInfo`](./KGameObject/KGLuaItemInfo.zh-CN.md) itemInfo) GetItemInfo(`number` nItemTableType, `number` nItemID)

* <h4 id="GetItemTip">GetItemTip</h4>

获取物品的提示文本。

 > (`string` szTip) GetItemTip([`KGItem`](./KGameObject/KGItem.zh-CN.md) item)

* <h4 id="GetItemEnchantAttrib">GetItemEnchantAttrib</h4>

获取物品的附魔属性。

 > (`table` tAttrib) GetItemEnchantAttrib(`number` nEnchantID)

* <h4 id="GetItemRepairPrice">GetItemRepairPrice</h4>

获取物品的修理价格。

 > (`number` nPrice) GetItemRepairPrice([`KGItem`](./KGameObject/KGItem.zh-CN.md) item)
