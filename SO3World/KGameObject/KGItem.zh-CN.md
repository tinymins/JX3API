[English](./KGItem.md) | 中文

# KGItem（物品实例）

物品实例对象，代表背包或装备中的实际物品。

说明：

- 通过 `GetItem()`、`GetPlayerItem()`、`KPlayer:GetItem()`、`KPlayer:GetTalkLinkItem()`、`KDoodad:GetLootItem()`、`KMailInfo:GetItem()` 获取

## 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `dwID` | `number` | 物品唯一 ID |
| `szName` | `string` | 物品名称 |
| `nLevel` | `number` | 物品等级 |
| `nGenre` | `number` | 物品大类（参见 `ITEM_GENRE`） |
| `nSub` | `number` | 物品子类型 |
| `nDetail` | `number` | 物品详细类型 |
| `nBindType` | `number` | 绑定类型（参见 `ITEM_BIND`） |
| `bCanTrade` | `boolean` | 是否可交易 |
| `bCanDestroy` | `boolean` | 是否可销毁 |
| `nVersion` | `number` | 物品版本 |
| `dwTabType` | `number` | Tab 类型 |
| `dwIndex` | `number` | Tab 索引 |
| `nQuality` | `number` | 物品品质（0-5） |
| `nCurrentDurability` | `number` | 当前耐久度 |
| `nStackNum` | `number` | 当前堆叠数量 |
| `nMaxStackNum` | `number` | 最大堆叠数量 |
| `nMaxDurability` | `number` | 最大耐久度 |
| `nBaseScore` | `number` | 基础装备分数 |
| `nBookID` | `number` | 书籍 ID（书籍类物品） |
| `bBind` | `boolean` | 是否已绑定 |
| `bCanStack` | `boolean` | 是否可堆叠 |
| `bCanConsume` | `boolean` | 是否为消耗品 |
| `dwSetID` | `number` | 套装 ID |
| `nMaxExistAmount` | `number` | 最大存在数量 |
| `nMaxExistTime` | `number` | 最大存在时间 |
| `nUiId` | `number` | UI 图标 ID |
| `nStrengthLevel` | `number` | 精炼等级 |
| `nStrengthScore` | `number` | 精炼分数 |
| `nMountsScore` | `number` | 镶嵌（宝石）分数 |
| `dwPermanentEnchantID` | `number` | 永久附魔 ID |
| `dwTemporaryEnchantID` | `number` | 临时附魔 ID |

## 方法

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

获取物品的魔法属性。

 > (`table` tAttribs) KGItem:GetMagicAttrib()

* <h4 id="KGItem_IsRepairable">IsRepairable</h4>

检查物品是否可修理。

 > (`boolean` bRepairable) KGItem:IsRepairable()

* <h4 id="KGItem_GetRequireAttrib">GetRequireAttrib</h4>

获取装备此物品所需的属性要求。

 > (`table` tRequire) KGItem:GetRequireAttrib()

* <h4 id="KGItem_GetMountIndex">GetMountIndex</h4>

获取宝石镶嵌槽位索引。

 > (`number` nIndex) KGItem:GetMountIndex()

* <h4 id="KGItem_GetBaseAttrib">GetBaseAttrib</h4>

获取物品的基础属性。

 > (`table` tAttribs) KGItem:GetBaseAttrib()

* <h4 id="KGItem_GetSlotCount">GetSlotCount</h4>

获取宝石孔数量。

 > (`number` nCount) KGItem:GetSlotCount()

* <h4 id="KGItem_GetSlotAttrib">GetSlotAttrib</h4>

获取指定孔位镶嵌宝石的属性。

 > (`table` tAttrib) KGItem:GetSlotAttrib(`number` nSlotIndex)

* <h4 id="KGItem_CanMountColorDiamond">CanMountColorDiamond</h4>

检查是否可以镶嵌五彩石。

 > (`boolean` bCan) KGItem:CanMountColorDiamond()

* <h4 id="KGItem_GetMountFEAEnchantID">GetMountFEAEnchantID</h4>

获取五行石附魔 ID。

 > (`number` dwEnchantID) KGItem:GetMountFEAEnchantID()

* <h4 id="KGItem_GetTemporaryEnchantLeftSeconds">GetTemporaryEnchantLeftSeconds</h4>

获取临时附魔剩余秒数。

 > (`number` nSeconds) KGItem:GetTemporaryEnchantLeftSeconds()

* <h4 id="KGItem_GetChangeCof">GetChangeCof</h4>

获取重铸物品的变化系数。

 > (`number` fCof) KGItem:GetChangeCof()

* <h4 id="KGItem_GetChangeAttrib">GetChangeAttrib</h4>

获取重铸后的变化属性。

 > (`table` tAttribs) KGItem:GetChangeAttrib()

* <h4 id="KGItem_GetChangeInfo">GetChangeInfo</h4>

获取详细的变化信息。

 > (`table` tInfo) KGItem:GetChangeInfo()

* <h4 id="KGItem_GetChangeAttribByStrengthLevel">GetChangeAttribByStrengthLevel</h4>

获取指定精炼等级下的变化属性。

 > (`table` tAttribs) KGItem:GetChangeAttribByStrengthLevel(`number` nLevel)

* <h4 id="KGItem_GetLeftExistTime">GetLeftExistTime</h4>

获取限时物品的剩余存在时间。

 > (`number` nTime) KGItem:GetLeftExistTime()

* <h4 id="KGItem_GetMagicAttribByStrengthLevel">GetMagicAttribByStrengthLevel</h4>

获取指定精炼等级下的魔法属性。

 > (`table` tAttribs) KGItem:GetMagicAttribByStrengthLevel(`number` nLevel)

* <h4 id="KGItem_GetMountDiamondEnchantID">GetMountDiamondEnchantID</h4>

获取镶嵌宝石的附魔 ID。

 > (`number` dwEnchantID) KGItem:GetMountDiamondEnchantID(`number` nSlotIndex)

* <h4 id="KGItem_CheckIgnoreBindMask">CheckIgnoreBindMask</h4>

检查忽略绑定掩码。

 > (`boolean` bIgnore) KGItem:CheckIgnoreBindMask(`number` nMask)
