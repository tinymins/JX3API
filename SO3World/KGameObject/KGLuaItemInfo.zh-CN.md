[English](./KGLuaItemInfo.md) | 中文

# KGLuaItemInfo（物品信息模板）

物品信息模板对象，包含物品的静态数据。

说明：

- 通过 `GetItemInfo()`、`GetItemAdvanceBoxKeyInfo()` 获取
- 这是物品模板数据，不是实际的物品实例

## 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `dwID` | `number` | 物品模板 ID |
| `szName` | `string` | 物品名称 |
| `nLevel` | `number` | 物品等级 |
| `nGenre` | `number` | 物品大类（参见 `ITEM_GENRE`） |
| `nSub` | `number` | 物品子类型 |
| `nDetail` | `number` | 物品详细类型 |
| `nExistType` | `number` | 存在类型（参见 `ITEM_EXIST_TYPE`） |
| `nBindType` | `number` | 绑定类型（参见 `ITEM_BIND`） |
| `nQuality` | `number` | 物品品质（0-5） |
| `dwSetID` | `number` | 套装 ID |
| `nMaxExistAmount` | `number` | 最大存在数量 |
| `nMaxExistTime` | `number` | 最大存在时间 |
| `dwCoolDownID` | `number` | 冷却 ID |
| `nUiId` | `number` | UI 图标 ID |
| `nMaxStrengthLevel` | `number` | 最大精炼等级 |

## 方法

[`GetBaseAttrib`](#KGLuaItemInfo_GetBaseAttrib)
[`GetRequireAttrib`](#KGLuaItemInfo_GetRequireAttrib)
[`GetMagicAttribIndexList`](#KGLuaItemInfo_GetMagicAttribIndexList)
[`GetCoolDown`](#KGLuaItemInfo_GetCoolDown)

---

* <h4 id="KGLuaItemInfo_GetBaseAttrib">GetBaseAttrib</h4>

获取物品模板的基础属性。

 > (`table` tAttribs) KGLuaItemInfo:GetBaseAttrib()

* <h4 id="KGLuaItemInfo_GetRequireAttrib">GetRequireAttrib</h4>

获取装备此物品所需的属性要求。

 > (`table` tRequire) KGLuaItemInfo:GetRequireAttrib()

* <h4 id="KGLuaItemInfo_GetMagicAttribIndexList">GetMagicAttribIndexList</h4>

获取魔法属性索引列表。

 > (`table` tIndices) KGLuaItemInfo:GetMagicAttribIndexList()

* <h4 id="KGLuaItemInfo_GetCoolDown">GetCoolDown</h4>

获取物品的冷却信息。

 > (`number` nCoolDown) KGLuaItemInfo:GetCoolDown()
