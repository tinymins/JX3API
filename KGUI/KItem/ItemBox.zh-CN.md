[English](./ItemBox.md) | 中文

# ItemBox

说明：

- 部分使用 offset 的 API（例如 `SetOverTextPosition`）在 Lua 侧使用**未缩放的 UI 坐标**；内部会把输入乘以 `Station.GetUIScale()`。

[`SetBoxIndex`](#LuaItemBox_SetIndex)
[`GetBoxIndex`](#LuaItemBox_GetIndex)
[`SetObject`](#LuaItemBox_SetObject)
[`GetObject`](#LuaItemBox_GetObject)
[`GetObjectType`](#LuaItemBox_GetObjectType)
[`SetObjectData`](#LuaItemBox_SetObjectData)
[`GetObjectData`](#LuaItemBox_GetObjectData)
[`ClearObject`](#LuaItemBox_ClearObject)
[`Clear`](#LuaItemBox_Clear)
[`IsEmpty`](#LuaItemBox_IsEmpty)
[`EnableObject`](#LuaItemBox_EnableObject)
[`IsObjectEnable`](#LuaItemBox_IsObjectEnable)
[`EnableObjectEquip`](#LuaItemBox_EnableObjectEquip)
[`IsObjectEquipable`](#LuaItemBox_IsObjectEquipable)
[`SetObjectCoolDown`](#LuaItemBox_SetObjectCoolDown)
[`IsObjectCoolDown`](#LuaItemBox_IsObjectCoolDown)
[`SetObjectSparking`](#LuaItemBox_SetObjectSparking)
[`SetObjectInUse`](#LuaItemBox_SetObjectInUse)
[`SetObjectStaring`](#LuaItemBox_SetObjectStaring)
[`SetObjectSelected`](#LuaItemBox_SetObjectSelected)
[`IsObjectSelected`](#LuaItemBox_IsObjectSelected)
[`SetObjectMouseOver`](#LuaItemBox_SetObjectMouseOver)
[`IsObjectMouseOver`](#LuaItemBox_IsObjectMouseOver)
[`SetObjectPressed`](#LuaItemBox_SetObjectPressed)
[`IsObjectPressed`](#LuaItemBox_IsObjectPressed)
[`SetCoolDownPercentage`](#LuaItemBox_SetCoolDownPercentage)
[`GetCoolDownPercentage`](#LuaItemBox_GetCoolDownPercentage)
[`SetObjectCoolDownType`](#LuaItemBox_SetObjectCoolDownType)
[`SetObjectIcon`](#LuaItemBox_SetObjectIcon)
[`GetObjectIcon`](#LuaItemBox_GetObjectIcon)
[`GetObjectIconPath`](#LuaItemBox_GetObjectIconPath)
[`ClearObjectIcon`](#LuaItemBox_ClearObjectIcon)
[`SetOverText`](#LuaItemBox_SetOverText)
[`GetOverText`](#LuaItemBox_GetOverText)
[`SetOverTextFontScheme`](#LuaItemBox_SetOverTextFontScheme)
[`GetOverTextFontScheme`](#LuaItemBox_GetOverTextFontScheme)
[`SetOverTextPosition`](#LuaItemBox_SetOverTextPosition)
[`GetOverTextPosition`](#LuaItemBox_GetOverTextPosition)
[`SetExtentImage`](#LuaItemBox_SetExtentImage)
[`ClearExtentImage`](#LuaItemBox_ClearExtentImage)
[`SetExtentAnimate`](#LuaItemBox_SetExtentAnimate)
[`ClearExtentAnimate`](#LuaItemBox_ClearExtentAnimate)
[`IsPlayingExAnimate`](#LuaItemBox_IsPlayingExAnimate)
[`SetExtentLayer`](#LuaItemBox_SetExtentLayer)
[`GetExtentLayer`](#LuaItemBox_GetExtentLayer)
[`ClearExtentLayer`](#LuaItemBox_ClearExtentLayer)
[`IsExtentAnimatePlaying`](#LuaItemBox_IsExtentAnimatePlaying)
[`SetExtentImageType`](#LuaItemBox_SetExtentImageType)
[`SetExtentAnimateType`](#LuaItemBox_SetExtentAnimateType)
[`GetExtentPercent`](#LuaItemBox_GetExtentPercent)
[`SetExtentPercent`](#LuaItemBox_SetExtentPercent)
[`GetExtentVisible`](#LuaItemBox_GetExtentVisible)
[`SetExtentVisible`](#LuaItemBox_SetExtentVisible)
[`SetExtentTimeStartAngle`](#LuaItemBox_SetExtentTimeStartAngle)
[`IconToGray`](#LuaItemBox_IconToGray)
[`IconToNormal`](#LuaItemBox_IconToNormal)
[`IsIconGray`](#LuaItemBox_IsIconGray)
[`SetStateResID`](#LuaItemBox_SetStateResID)
[`ExchangeDrawOrder`](#LuaItemBox_ExchangeDrawOrder)

* <h4 id="LuaItemBox_SetIndex">SetBoxIndex</h4>
设置格子索引。

 > (`void`) ItemBox:SetBoxIndex(`number` nIndex)

 ````lua
 ItemBox:SetBoxIndex(0)
 ````

* <h4 id="LuaItemBox_GetIndex">GetBoxIndex</h4>
获取格子索引。

 > (`number` nIndex) ItemBox:GetBoxIndex()

 ````lua
 local nIndex = ItemBox:GetBoxIndex()
 ````

* <h4 id="LuaItemBox_SetObject">SetObject</h4>
设置对象类型与对象数据。

对象数据在引擎内部是固定长度的数组（长度为 `MAX_BOX_OBJECT_DATA_COUNT = 6`）；Lua 侧可以从 `data1` 开始按需传入若干个数字值。

- 需要至少传入 `nObjectType`。
- 只会读取到引擎支持的固定数量（`MAX_BOX_OBJECT_DATA_COUNT`），超出的参数会被忽略。
- 如果希望所有槽位的数据都确定，建议把所有值都显式传齐。

 > (`void`) ItemBox:SetObject(`number` nObjectType[, `number` data1[, `number` data2[, `number` data3[, `number` data4[, `number` data5[, `number` data6]]]]]])

 ````lua
 ItemBox:SetObject(0)
 ItemBox:SetObject(0, 1, 2, 3)
 ````

* <h4 id="LuaItemBox_GetObject">GetObject</h4>
获取对象类型与对象数据。

返回 `nObjectType`，以及 `MAX_BOX_OBJECT_DATA_COUNT` 个数字数据值（`data1`..`data6`）。

 > (`number` nObjectType, `number` data1, `number` data2, `number` data3, `number` data4, `number` data5, `number` data6) ItemBox:GetObject()

 ````lua
 local nObjectType, d1, d2 = ItemBox:GetObject()
 ````

* <h4 id="LuaItemBox_GetObjectType">GetObjectType</h4>
获取对象类型。

 > (`number` nObjectType) ItemBox:GetObjectType()

 ````lua
 local nObjectType = ItemBox:GetObjectType()
 ````

* <h4 id="LuaItemBox_SetObjectData">SetObjectData</h4>
按索引设置单个对象数据值。

索引从 1 开始。
注意：

- 实现中会先取当前的 `ObjectType`，再把修改后的数据整体回写，因此该 API 不会改变对象类型。
- `nValue` 在绑定层会先转换为整数再写入。
- 如果 `nIndex` 越界，绑定层会报错并且不返回值。

 > (`void`) ItemBox:SetObjectData(`number` nIndex, `number` nValue)

 ````lua
 ItemBox:SetObjectData(1, 123)
 ````

* <h4 id="LuaItemBox_GetObjectData">GetObjectData</h4>
获取对象数据。

- 不传索引：返回所有数据值。
- 传入 `nIndex`：返回单个数据值（索引从 1 开始）。

不传索引时固定返回 `MAX_BOX_OBJECT_DATA_COUNT` 个值。

如果 `nIndex` 越界，绑定层会报错并且不返回值。

 > (`number` data1, `number` data2, `number` data3, `number` data4, `number` data5, `number` data6) ItemBox:GetObjectData()

 > (`number` nValue) ItemBox:GetObjectData(`number` nIndex)

 ````lua
 local d1, d2 = ItemBox:GetObjectData()
 local v = ItemBox:GetObjectData(1)
 ````

* <h4 id="LuaItemBox_ClearObject">ClearObject</h4>
清除对象。

 > (`void`) ItemBox:ClearObject()

 ````lua
 ItemBox:ClearObject()
 ````

* <h4 id="LuaItemBox_Clear">Clear</h4>
清空该 box。

 > (`void`) ItemBox:Clear()

 ````lua
 ItemBox:Clear()
 ````

* <h4 id="LuaItemBox_IsEmpty">IsEmpty</h4>
检查该 box 是否为空。

 > (`bool` bEmpty) ItemBox:IsEmpty()

 ````lua
 local bEmpty = ItemBox:IsEmpty()
 ````

* <h4 id="LuaItemBox_EnableObject">EnableObject</h4>
启用/禁用对象。

 > (`void`) ItemBox:EnableObject(`bool|number` bEnable)

 ````lua
 ItemBox:EnableObject(true)
 ````

* <h4 id="LuaItemBox_IsObjectEnable">IsObjectEnable</h4>
检查对象是否启用。

 > (`bool` bEnable) ItemBox:IsObjectEnable()

 ````lua
 local bEnable = ItemBox:IsObjectEnable()
 ````

* <h4 id="LuaItemBox_EnableObjectEquip">EnableObjectEquip</h4>
启用/禁用对象装备（equip）。

 > (`void`) ItemBox:EnableObjectEquip(`bool|number` bEnable)

 ````lua
 ItemBox:EnableObjectEquip(true)
 ````

* <h4 id="LuaItemBox_IsObjectEquipable">IsObjectEquipable</h4>
检查对象是否可装备（equipable）。

 > (`bool` bEquipable) ItemBox:IsObjectEquipable()

 ````lua
 local bEquipable = ItemBox:IsObjectEquipable()
 ````

* <h4 id="LuaItemBox_SetObjectCoolDown">SetObjectCoolDown</h4>
设置对象冷却状态。

 > (`void`) ItemBox:SetObjectCoolDown(`bool|number` bCoolDown)

 ````lua
 ItemBox:SetObjectCoolDown(true)
 ````

* <h4 id="LuaItemBox_IsObjectCoolDown">IsObjectCoolDown</h4>
检查对象冷却状态。

 > (`bool` bCoolDown) ItemBox:IsObjectCoolDown()

 ````lua
 local bCoolDown = ItemBox:IsObjectCoolDown()
 ````

* <h4 id="LuaItemBox_SetObjectSparking">SetObjectSparking</h4>
设置对象闪烁状态。

 > (`void`) ItemBox:SetObjectSparking(`bool|number` bSparking)

 ````lua
 ItemBox:SetObjectSparking(true)
 ````

* <h4 id="LuaItemBox_SetObjectInUse">SetObjectInUse</h4>
设置对象使用中状态。

 > (`void`) ItemBox:SetObjectInUse(`bool|number` bInUse)

 ````lua
 ItemBox:SetObjectInUse(true)
 ````

* <h4 id="LuaItemBox_SetObjectStaring">SetObjectStaring</h4>
设置对象“凝视/高亮关注”状态。

 > (`void`) ItemBox:SetObjectStaring(`bool|number` bStaring)

 ````lua
 ItemBox:SetObjectStaring(true)
 ````

* <h4 id="LuaItemBox_SetObjectSelected">SetObjectSelected</h4>
设置对象选中状态。

 > (`void`) ItemBox:SetObjectSelected(`bool|number` bSelected)

 ````lua
 ItemBox:SetObjectSelected(true)
 ````

* <h4 id="LuaItemBox_IsObjectSelected">IsObjectSelected</h4>
检查对象选中状态。

 > (`bool` bSelected) ItemBox:IsObjectSelected()

 ````lua
 local bSelected = ItemBox:IsObjectSelected()
 ````

* <h4 id="LuaItemBox_SetObjectMouseOver">SetObjectMouseOver</h4>
设置对象鼠标悬停（mouse over）状态。

 > (`void`) ItemBox:SetObjectMouseOver(`bool|number` bMouseOver)

 ````lua
 ItemBox:SetObjectMouseOver(true)
 ````

* <h4 id="LuaItemBox_IsObjectMouseOver">IsObjectMouseOver</h4>
检查对象鼠标悬停（mouse over）状态。

 > (`bool` bMouseOver) ItemBox:IsObjectMouseOver()

 ````lua
 local bMouseOver = ItemBox:IsObjectMouseOver()
 ````

* <h4 id="LuaItemBox_SetObjectPressed">SetObjectPressed</h4>
设置对象按下（pressed）状态。

 > (`void`) ItemBox:SetObjectPressed(`bool|number` bPressed)

 ````lua
 ItemBox:SetObjectPressed(true)
 ````

* <h4 id="LuaItemBox_IsObjectPressed">IsObjectPressed</h4>
检查对象按下（pressed）状态。

 > (`bool` bPressed) ItemBox:IsObjectPressed()

 ````lua
 local bPressed = ItemBox:IsObjectPressed()
 ````

* <h4 id="LuaItemBox_SetCoolDownPercentage">SetCoolDownPercentage</h4>
设置冷却百分比。

 > (`void`) ItemBox:SetCoolDownPercentage(`number` fPercent)

 ````lua
 ItemBox:SetCoolDownPercentage(0.5)
 ````

* <h4 id="LuaItemBox_GetCoolDownPercentage">GetCoolDownPercentage</h4>
获取冷却百分比。

 > (`number` fPercent) ItemBox:GetCoolDownPercentage()

 ````lua
 local fPercent = ItemBox:GetCoolDownPercentage()
 ````

* <h4 id="LuaItemBox_SetObjectCoolDownType">SetObjectCoolDownType</h4>
设置冷却类型。

 > (`void`) ItemBox:SetObjectCoolDownType(`number` dwType)

 ````lua
 ItemBox:SetObjectCoolDownType(0)
 ````

* <h4 id="LuaItemBox_SetObjectIcon">SetObjectIcon</h4>
设置对象图标 id。

 > (`void`) ItemBox:SetObjectIcon(`number` nIconID)

 ````lua
 ItemBox:SetObjectIcon(123)
 ````

* <h4 id="LuaItemBox_GetObjectIcon">GetObjectIcon</h4>
获取对象图标 id。

 > (`number` nIconID) ItemBox:GetObjectIcon()

 ````lua
 local nIconID = ItemBox:GetObjectIcon()
 ````

* <h4 id="LuaItemBox_GetObjectIconPath">GetObjectIconPath</h4>
获取对象图标文件路径。

实现会用当前的 `IconID` 查询图标资源并拼接完整路径；如果 `IconID` 无效（找不到资源），绑定层会报错并且不返回值。

 > (`string` szPath) ItemBox:GetObjectIconPath()

 ````lua
 local szPath = ItemBox:GetObjectIconPath()
 ````

* <h4 id="LuaItemBox_ClearObjectIcon">ClearObjectIcon</h4>
清除对象图标。

 > (`void`) ItemBox:ClearObjectIcon()

 ````lua
 ItemBox:ClearObjectIcon()
 ````

* <h4 id="LuaItemBox_SetOverText">SetOverText</h4>
按索引设置叠加文本（over text）。

`szText` 会按当前代码页从 Lua 字符串转换后再传入引擎。

 > (`void`) ItemBox:SetOverText(`number` nOverTextIndex, `string` szText)

 ````lua
 ItemBox:SetOverText(0, "text")
 ````

* <h4 id="LuaItemBox_GetOverText">GetOverText</h4>
按索引获取叠加文本（over text）。

 > (`string` szText) ItemBox:GetOverText(`number` nOverTextIndex)

 ````lua
 local szText = ItemBox:GetOverText(0)
 ````

* <h4 id="LuaItemBox_SetOverTextFontScheme">SetOverTextFontScheme</h4>
设置叠加文本的字体方案。

 > (`void`) ItemBox:SetOverTextFontScheme(`number` nOverTextIndex, `number` nFontScheme)

 ````lua
 ItemBox:SetOverTextFontScheme(0, 0)
 ````

* <h4 id="LuaItemBox_GetOverTextFontScheme">GetOverTextFontScheme</h4>
获取叠加文本的字体方案。

 > (`number` nFontScheme) ItemBox:GetOverTextFontScheme(`number` nOverTextIndex)

 ````lua
 local nFontScheme = ItemBox:GetOverTextFontScheme(0)
 ````

* <h4 id="LuaItemBox_SetOverTextPosition">SetOverTextPosition</h4>
设置叠加文本的位置。

`fOffsetX`/`fOffsetY` 在 Lua 侧是未缩放值；内部会乘以 UIScale。

 > (`void`) ItemBox:SetOverTextPosition(`number` nOverTextIndex, `number` nPos[, `number` fOffsetX[, `number` fOffsetY]])

 ````lua
 ItemBox:SetOverTextPosition(0, 0)
 ItemBox:SetOverTextPosition(0, 0, 10)
 ItemBox:SetOverTextPosition(0, 0, 10, 10)
 ````

* <h4 id="LuaItemBox_GetOverTextPosition">GetOverTextPosition</h4>
获取叠加文本的位置。

 > (`number` nPos) ItemBox:GetOverTextPosition(`number` nOverTextIndex)

 ````lua
 local nPos = ItemBox:GetOverTextPosition(0)
 ````

* <h4 id="LuaItemBox_SetExtentImage">SetExtentImage</h4>
将 extent 第 0 层设置为图片。

`szImage` 会经过 `FormatFilePath` 规范化后再使用。

 > (`void`) ItemBox:SetExtentImage(`string` szImage, `number` nFrame)

 ````lua
 ItemBox:SetExtentImage("interface/ui/image/tex.tga", 0)
 ````

* <h4 id="LuaItemBox_ClearExtentImage">ClearExtentImage</h4>
清除 extent 第 0 层。

 > (`void`) ItemBox:ClearExtentImage()

 ````lua
 ItemBox:ClearExtentImage()
 ````

* <h4 id="LuaItemBox_SetExtentAnimate">SetExtentAnimate</h4>
将 extent 第 1 层设置为动画。

`szImage` 会经过 `FormatFilePath` 规范化后再使用。

 > (`void`) ItemBox:SetExtentAnimate(`string` szImage, `number` nGroup[, `number` nLoopCount = -1])

 ````lua
 ItemBox:SetExtentAnimate("interface/ui/ani/ani.tga", 0)
 ItemBox:SetExtentAnimate("interface/ui/ani/ani.tga", 0, -1)
 ````

* <h4 id="LuaItemBox_ClearExtentAnimate">ClearExtentAnimate</h4>
清除 extent 第 1 层。

 > (`void`) ItemBox:ClearExtentAnimate()

 ````lua
 ItemBox:ClearExtentAnimate()
 ````

* <h4 id="LuaItemBox_IsPlayingExAnimate">IsPlayingExAnimate</h4>
检查 extent 第 1 层动画是否正在播放。

 > (`bool` bPlaying) ItemBox:IsPlayingExAnimate()

 ````lua
 local bPlaying = ItemBox:IsPlayingExAnimate()
 ````

* <h4 id="LuaItemBox_SetExtentLayer">SetExtentLayer</h4>
设置 extent 层（通用形式）。

实现要求参数个数为 4 或 5；当不传 `nLoopCount` 时，会把 `-2` 作为默认值传入引擎。

 > (`void`) ItemBox:SetExtentLayer(`number` uLayer, `string` szImage, `number` nFrame[, `number` nLoopCount])

 ````lua
 ItemBox:SetExtentLayer(2, "interface/ui/image/tex.tga", 0)
 ItemBox:SetExtentLayer(2, "interface/ui/image/tex.tga", 0, -1)
 ````

* <h4 id="LuaItemBox_GetExtentLayer">GetExtentLayer</h4>
获取 extent 层信息。

 > (`string` szImage, `number` nFrame, `number` nLoopCount) ItemBox:GetExtentLayer(`number` uLayer)

 ````lua
 local szImage, nFrame, nLoopCount = ItemBox:GetExtentLayer(2)
 ````

* <h4 id="LuaItemBox_ClearExtentLayer">ClearExtentLayer</h4>
清除 extent 层。

- 传入 `uLayer`：清除指定层。
- 不传 `uLayer`：清除所有层。

 > (`void`) ItemBox:ClearExtentLayer([`number` uLayer])

 ````lua
 ItemBox:ClearExtentLayer(2)
 ItemBox:ClearExtentLayer()
 ````

* <h4 id="LuaItemBox_IsExtentAnimatePlaying">IsExtentAnimatePlaying</h4>
检查某个 extent 动画层是否正在播放。

 > (`bool` bPlaying) ItemBox:IsExtentAnimatePlaying(`number` uLayer)

 ````lua
 local bPlaying = ItemBox:IsExtentAnimatePlaying(1)
 ````

* <h4 id="LuaItemBox_SetExtentImageType">SetExtentImageType</h4>
设置 extent 层图片类型。

如果当前层不是图片类型，绑定层会报错（错误信息：`Current box layer type is not image!`）。

 > (`void`) ItemBox:SetExtentImageType(`number` uLayer, `number` dwType)

 ````lua
 ItemBox:SetExtentImageType(0, 0)
 ````

* <h4 id="LuaItemBox_SetExtentAnimateType">SetExtentAnimateType</h4>
设置 extent 层动画类型。

如果当前层不是动画类型，绑定层会报错（错误信息：`Current box layer type is not animate!`）。

 > (`void`) ItemBox:SetExtentAnimateType(`number` uLayer, `number` dwType)

 ````lua
 ItemBox:SetExtentAnimateType(1, 0)
 ````

* <h4 id="LuaItemBox_GetExtentPercent">GetExtentPercent</h4>
获取 extent 百分比。

 > (`number` fPercent) ItemBox:GetExtentPercent(`number` uLayer)

 ````lua
 local fPercent = ItemBox:GetExtentPercent(0)
 ````

* <h4 id="LuaItemBox_SetExtentPercent">SetExtentPercent</h4>
设置 extent 百分比。

 > (`void`) ItemBox:SetExtentPercent(`number` uLayer, `number` fPercent)

 ````lua
 ItemBox:SetExtentPercent(0, 1.0)
 ````

* <h4 id="LuaItemBox_GetExtentVisible">GetExtentVisible</h4>
获取 extent 可见性。

 > (`bool` bVisible) ItemBox:GetExtentVisible(`number` uLayer)

 ````lua
 local bVisible = ItemBox:GetExtentVisible(0)
 ````

* <h4 id="LuaItemBox_SetExtentVisible">SetExtentVisible</h4>
设置 extent 可见性。

 > (`void`) ItemBox:SetExtentVisible(`number` uLayer, `bool` bVisible)

 ````lua
 ItemBox:SetExtentVisible(0, true)
 ````

* <h4 id="LuaItemBox_SetExtentTimeStartAngle">SetExtentTimeStartAngle</h4>
设置 extent 时间起始角度。

 > (`void`) ItemBox:SetExtentTimeStartAngle(`number` uLayer, `number` fAngle)

 ````lua
 ItemBox:SetExtentTimeStartAngle(0, 0)
 ````

* <h4 id="LuaItemBox_IconToGray">IconToGray</h4>
将对象图标灰化。

 > (`void`) ItemBox:IconToGray()

 ````lua
 ItemBox:IconToGray()
 ````

* <h4 id="LuaItemBox_IconToNormal">IconToNormal</h4>
恢复对象图标为正常状态。

 > (`void`) ItemBox:IconToNormal()

 ````lua
 ItemBox:IconToNormal()
 ````

* <h4 id="LuaItemBox_IsIconGray">IsIconGray</h4>
检查图标是否已灰化。

 > (`bool` bGray) ItemBox:IsIconGray()

 ````lua
 local bGray = ItemBox:IsIconGray()
 ````

* <h4 id="LuaItemBox_SetStateResID">SetStateResID</h4>
设置状态资源 id。

 > (`void`) ItemBox:SetStateResID(`number` eType, `number` nResID)

 ````lua
 ItemBox:SetStateResID(0, 0)
 ````

* <h4 id="LuaItemBox_ExchangeDrawOrder">ExchangeDrawOrder</h4>
交换层与层之间的绘制顺序。

 > (`void`) ItemBox:ExchangeDrawOrder(`number` uSrc, `number` uDst)

 ````lua
 ItemBox:ExchangeDrawOrder(0, 1)
 ````
