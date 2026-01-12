English | [中文](./KGLuaItemInfo.zh-CN.md)

# KGLuaItemInfo

Item information template object containing static item data.

Notes:

- Obtained via `GetItemInfo()`, `GetItemAdvanceBoxKeyInfo()`
- This is the item template data, not an actual item instance

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `dwID` | `number` | Item template ID |
| `szName` | `string` | Item name |
| `nLevel` | `number` | Item level |
| `nGenre` | `number` | Item genre (see `ITEM_GENRE`) |
| `nSub` | `number` | Item sub-type |
| `nDetail` | `number` | Item detail type |
| `nExistType` | `number` | Exist type (see `ITEM_EXIST_TYPE`) |
| `nBindType` | `number` | Bind type (see `ITEM_BIND`) |
| `nQuality` | `number` | Item quality (0-5) |
| `dwSetID` | `number` | Equipment set ID |
| `nMaxExistAmount` | `number` | Maximum exist amount |
| `nMaxExistTime` | `number` | Maximum exist time |
| `dwCoolDownID` | `number` | Cooldown ID |
| `nUiId` | `number` | UI icon ID |
| `nMaxStrengthLevel` | `number` | Maximum strengthen level |

## Methods

[`GetBaseAttrib`](#KGLuaItemInfo_GetBaseAttrib)
[`GetRequireAttrib`](#KGLuaItemInfo_GetRequireAttrib)
[`GetMagicAttribIndexList`](#KGLuaItemInfo_GetMagicAttribIndexList)
[`GetCoolDown`](#KGLuaItemInfo_GetCoolDown)

---

* <h4 id="KGLuaItemInfo_GetBaseAttrib">GetBaseAttrib</h4>

Gets the base attributes of the item template.

 > (`table` tAttribs) KGLuaItemInfo:GetBaseAttrib()

* <h4 id="KGLuaItemInfo_GetRequireAttrib">GetRequireAttrib</h4>

Gets the required attributes to equip this item.

 > (`table` tRequire) KGLuaItemInfo:GetRequireAttrib()

* <h4 id="KGLuaItemInfo_GetMagicAttribIndexList">GetMagicAttribIndexList</h4>

Gets the list of magic attribute indices.

 > (`table` tIndices) KGLuaItemInfo:GetMagicAttribIndexList()

* <h4 id="KGLuaItemInfo_GetCoolDown">GetCoolDown</h4>

Gets the cooldown information for the item.

 > (`number` nCoolDown) KGLuaItemInfo:GetCoolDown()
