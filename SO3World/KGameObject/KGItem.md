English | [中文](./KGItem.zh-CN.md)

# KGItem

Item instance object representing an actual item in inventory or equipment.

Notes:

- Obtained via `GetItem()`, `GetPlayerItem()`, `KPlayer:GetItem()`, `KPlayer:GetTalkLinkItem()`, `KDoodad:GetLootItem()`, `KMailInfo:GetItem()`

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `dwID` | `number` | Item unique ID |
| `szName` | `string` | Item name |
| `nLevel` | `number` | Item level |
| `nGenre` | `number` | Item genre (see `ITEM_GENRE`) |
| `nSub` | `number` | Item sub-type |
| `nDetail` | `number` | Item detail type |
| `nBindType` | `number` | Bind type (see `ITEM_BIND`) |
| `bCanTrade` | `boolean` | Whether item can be traded |
| `bCanDestroy` | `boolean` | Whether item can be destroyed |
| `nVersion` | `number` | Item version |
| `dwTabType` | `number` | Tab type |
| `dwIndex` | `number` | Tab index |
| `nQuality` | `number` | Item quality (0-5) |
| `nCurrentDurability` | `number` | Current durability |
| `nStackNum` | `number` | Current stack count |
| `nMaxStackNum` | `number` | Maximum stack count |
| `nMaxDurability` | `number` | Maximum durability |
| `nBaseScore` | `number` | Base equipment score |
| `nBookID` | `number` | Book ID (for book items) |
| `bBind` | `boolean` | Whether item is bound |
| `bCanStack` | `boolean` | Whether item can stack |
| `bCanConsume` | `boolean` | Whether item is consumable |
| `dwSetID` | `number` | Equipment set ID |
| `nMaxExistAmount` | `number` | Maximum exist amount |
| `nMaxExistTime` | `number` | Maximum exist time |
| `nUiId` | `number` | UI ID for icon |
| `nStrengthLevel` | `number` | Strengthen level |
| `nStrengthScore` | `number` | Strengthen score |
| `nMountsScore` | `number` | Mounts (gems) score |
| `dwPermanentEnchantID` | `number` | Permanent enchant ID |
| `dwTemporaryEnchantID` | `number` | Temporary enchant ID |

## Methods

[`GetMagicAttrib`](#KGItem_GetMagicAttrib)
[`IsRepairable`](#KGItem_IsRepairable)
[`GetRequireAttrib`](#KGItem_GetRequireAttrib)
[`GetMountIndex`](#KGItem_GetMountIndex)
[`GetBaseAttrib`](#KGItem_GetBaseAttrib)
[`GetSlotCount`](#KGItem_GetSlotCount)
[`GetSlotAttrib`](#KGItem_GetSlotAttrib)
[`CanMountColorDiamond`](#KGItem_CanMountColorDiamond)
[`GetMountFEAEnchantID`](#KGItem_GetMountFEAEnchantID)
[`GetTemporaryEnchantLeftSeconds`](#KGItem_GetTemporaryEnchantLeftSeconds)
[`GetChangeCof`](#KGItem_GetChangeCof)
[`GetChangeAttrib`](#KGItem_GetChangeAttrib)
[`GetChangeInfo`](#KGItem_GetChangeInfo)
[`GetChangeAttribByStrengthLevel`](#KGItem_GetChangeAttribByStrengthLevel)
[`GetLeftExistTime`](#KGItem_GetLeftExistTime)
[`GetMagicAttribByStrengthLevel`](#KGItem_GetMagicAttribByStrengthLevel)
[`GetMountDiamondEnchantID`](#KGItem_GetMountDiamondEnchantID)
[`CheckIgnoreBindMask`](#KGItem_CheckIgnoreBindMask)

---

* <h4 id="KGItem_GetMagicAttrib">GetMagicAttrib</h4>

Gets the magic attributes of the item.

 > (`table` tAttribs) KGItem:GetMagicAttrib()

* <h4 id="KGItem_IsRepairable">IsRepairable</h4>

Checks if the item can be repaired.

 > (`boolean` bRepairable) KGItem:IsRepairable()

* <h4 id="KGItem_GetRequireAttrib">GetRequireAttrib</h4>

Gets the required attributes to equip this item.

 > (`table` tRequire) KGItem:GetRequireAttrib()

* <h4 id="KGItem_GetMountIndex">GetMountIndex</h4>

Gets the mount slot index for gems.

 > (`number` nIndex) KGItem:GetMountIndex()

* <h4 id="KGItem_GetBaseAttrib">GetBaseAttrib</h4>

Gets the base attributes of the item.

 > (`table` tAttribs) KGItem:GetBaseAttrib()

* <h4 id="KGItem_GetSlotCount">GetSlotCount</h4>

Gets the number of gem slots.

 > (`number` nCount) KGItem:GetSlotCount()

* <h4 id="KGItem_GetSlotAttrib">GetSlotAttrib</h4>

Gets attributes from mounted gems in specified slot.

 > (`table` tAttrib) KGItem:GetSlotAttrib(`number` nSlotIndex)

* <h4 id="KGItem_CanMountColorDiamond">CanMountColorDiamond</h4>

Checks if a colored diamond can be mounted.

 > (`boolean` bCan) KGItem:CanMountColorDiamond()

* <h4 id="KGItem_GetMountFEAEnchantID">GetMountFEAEnchantID</h4>

Gets the FEA (Five Elements Attribute) enchant ID from mount.

 > (`number` dwEnchantID) KGItem:GetMountFEAEnchantID()

* <h4 id="KGItem_GetTemporaryEnchantLeftSeconds">GetTemporaryEnchantLeftSeconds</h4>

Gets remaining seconds for temporary enchant.

 > (`number` nSeconds) KGItem:GetTemporaryEnchantLeftSeconds()

* <h4 id="KGItem_GetChangeCof">GetChangeCof</h4>

Gets the change coefficient for refined items.

 > (`number` fCof) KGItem:GetChangeCof()

* <h4 id="KGItem_GetChangeAttrib">GetChangeAttrib</h4>

Gets the changed attributes after refining.

 > (`table` tAttribs) KGItem:GetChangeAttrib()

* <h4 id="KGItem_GetChangeInfo">GetChangeInfo</h4>

Gets detailed change information.

 > (`table` tInfo) KGItem:GetChangeInfo()

* <h4 id="KGItem_GetChangeAttribByStrengthLevel">GetChangeAttribByStrengthLevel</h4>

Gets changed attributes at specific strengthen level.

 > (`table` tAttribs) KGItem:GetChangeAttribByStrengthLevel(`number` nLevel)

* <h4 id="KGItem_GetLeftExistTime">GetLeftExistTime</h4>

Gets remaining exist time for timed items.

 > (`number` nTime) KGItem:GetLeftExistTime()

* <h4 id="KGItem_GetMagicAttribByStrengthLevel">GetMagicAttribByStrengthLevel</h4>

Gets magic attributes at specific strengthen level.

 > (`table` tAttribs) KGItem:GetMagicAttribByStrengthLevel(`number` nLevel)

* <h4 id="KGItem_GetMountDiamondEnchantID">GetMountDiamondEnchantID</h4>

Gets the enchant ID of mounted diamond.

 > (`number` dwEnchantID) KGItem:GetMountDiamondEnchantID(`number` nSlotIndex)

* <h4 id="KGItem_CheckIgnoreBindMask">CheckIgnoreBindMask</h4>

Checks the ignore bind mask.

 > (`boolean` bIgnore) KGItem:CheckIgnoreBindMask(`number` nMask)
