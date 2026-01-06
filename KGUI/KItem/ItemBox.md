# ItemBox

Notes:

- Some APIs using offsets (like `SetOverTextPosition`) use **unscaled UI coordinates** on Lua side; internally they are multiplied by `Station.GetUIScale()`.

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
Set box index.

 > (`void`) ItemBox:SetBoxIndex(`number` nIndex)

 ````lua
 ItemBox:SetBoxIndex(0)
 ````

* <h4 id="LuaItemBox_GetIndex">GetBoxIndex</h4>
Get box index.

 > (`number` nIndex) ItemBox:GetBoxIndex()

 ````lua
 local nIndex = ItemBox:GetBoxIndex()
 ````

* <h4 id="LuaItemBox_SetObject">SetObject</h4>
Set object type and its data.

The object data is a fixed-size array in engine; pass as many numeric values as needed.

 > (`void`) ItemBox:SetObject(`number` nObjectType[, `number` data1[, `number` data2[, ...]]])

 ````lua
 ItemBox:SetObject(0)
 ItemBox:SetObject(0, 1, 2, 3)
 ````

* <h4 id="LuaItemBox_GetObject">GetObject</h4>
Get object type and its data.

Returns `nObjectType` plus a fixed number of numeric data values.

 > (`number` nObjectType, `number` data1, `number` data2, ...) ItemBox:GetObject()

 ````lua
 local nObjectType, d1, d2 = ItemBox:GetObject()
 ````

* <h4 id="LuaItemBox_GetObjectType">GetObjectType</h4>
Get object type.

 > (`number` nObjectType) ItemBox:GetObjectType()

 ````lua
 local nObjectType = ItemBox:GetObjectType()
 ````

* <h4 id="LuaItemBox_SetObjectData">SetObjectData</h4>
Set a single object data value by index.

Index is **1-based**.

 > (`void`) ItemBox:SetObjectData(`number` nIndex, `number` nValue)

 ````lua
 ItemBox:SetObjectData(1, 123)
 ````

* <h4 id="LuaItemBox_GetObjectData">GetObjectData</h4>
Get object data.

- With no index: returns all data values.
- With `nIndex`: returns a single data value (index is **1-based**).

 > (`number` data1, `number` data2, ...) ItemBox:GetObjectData()

 > (`number` nValue) ItemBox:GetObjectData(`number` nIndex)

 ````lua
 local d1, d2 = ItemBox:GetObjectData()
 local v = ItemBox:GetObjectData(1)
 ````

* <h4 id="LuaItemBox_ClearObject">ClearObject</h4>
Clear object.

 > (`void`) ItemBox:ClearObject()

 ````lua
 ItemBox:ClearObject()
 ````

* <h4 id="LuaItemBox_Clear">Clear</h4>
Clear box.

 > (`void`) ItemBox:Clear()

 ````lua
 ItemBox:Clear()
 ````

* <h4 id="LuaItemBox_IsEmpty">IsEmpty</h4>
Check whether box is empty.

 > (`bool` bEmpty) ItemBox:IsEmpty()

 ````lua
 local bEmpty = ItemBox:IsEmpty()
 ````

* <h4 id="LuaItemBox_EnableObject">EnableObject</h4>
Enable/disable object.

 > (`void`) ItemBox:EnableObject(`bool|number` bEnable)

 ````lua
 ItemBox:EnableObject(true)
 ````

* <h4 id="LuaItemBox_IsObjectEnable">IsObjectEnable</h4>
Check whether object is enabled.

 > (`bool` bEnable) ItemBox:IsObjectEnable()

 ````lua
 local bEnable = ItemBox:IsObjectEnable()
 ````

* <h4 id="LuaItemBox_EnableObjectEquip">EnableObjectEquip</h4>
Enable/disable object equip.

 > (`void`) ItemBox:EnableObjectEquip(`bool|number` bEnable)

 ````lua
 ItemBox:EnableObjectEquip(true)
 ````

* <h4 id="LuaItemBox_IsObjectEquipable">IsObjectEquipable</h4>
Check whether object is equipable.

 > (`bool` bEquipable) ItemBox:IsObjectEquipable()

 ````lua
 local bEquipable = ItemBox:IsObjectEquipable()
 ````

* <h4 id="LuaItemBox_SetObjectCoolDown">SetObjectCoolDown</h4>
Set object cooldown state.

 > (`void`) ItemBox:SetObjectCoolDown(`bool|number` bCoolDown)

 ````lua
 ItemBox:SetObjectCoolDown(true)
 ````

* <h4 id="LuaItemBox_IsObjectCoolDown">IsObjectCoolDown</h4>
Check object cooldown state.

 > (`bool` bCoolDown) ItemBox:IsObjectCoolDown()

 ````lua
 local bCoolDown = ItemBox:IsObjectCoolDown()
 ````

* <h4 id="LuaItemBox_SetObjectSparking">SetObjectSparking</h4>
Set object sparking state.

 > (`void`) ItemBox:SetObjectSparking(`bool|number` bSparking)

 ````lua
 ItemBox:SetObjectSparking(true)
 ````

* <h4 id="LuaItemBox_SetObjectInUse">SetObjectInUse</h4>
Set object in-use state.

 > (`void`) ItemBox:SetObjectInUse(`bool|number` bInUse)

 ````lua
 ItemBox:SetObjectInUse(true)
 ````

* <h4 id="LuaItemBox_SetObjectStaring">SetObjectStaring</h4>
Set object staring state.

 > (`void`) ItemBox:SetObjectStaring(`bool|number` bStaring)

 ````lua
 ItemBox:SetObjectStaring(true)
 ````

* <h4 id="LuaItemBox_SetObjectSelected">SetObjectSelected</h4>
Set object selected state.

 > (`void`) ItemBox:SetObjectSelected(`bool|number` bSelected)

 ````lua
 ItemBox:SetObjectSelected(true)
 ````

* <h4 id="LuaItemBox_IsObjectSelected">IsObjectSelected</h4>
Check object selected state.

 > (`bool` bSelected) ItemBox:IsObjectSelected()

 ````lua
 local bSelected = ItemBox:IsObjectSelected()
 ````

* <h4 id="LuaItemBox_SetObjectMouseOver">SetObjectMouseOver</h4>
Set object mouse over state.

 > (`void`) ItemBox:SetObjectMouseOver(`bool|number` bMouseOver)

 ````lua
 ItemBox:SetObjectMouseOver(true)
 ````

* <h4 id="LuaItemBox_IsObjectMouseOver">IsObjectMouseOver</h4>
Check object mouse over state.

 > (`bool` bMouseOver) ItemBox:IsObjectMouseOver()

 ````lua
 local bMouseOver = ItemBox:IsObjectMouseOver()
 ````

* <h4 id="LuaItemBox_SetObjectPressed">SetObjectPressed</h4>
Set object pressed state.

 > (`void`) ItemBox:SetObjectPressed(`bool|number` bPressed)

 ````lua
 ItemBox:SetObjectPressed(true)
 ````

* <h4 id="LuaItemBox_IsObjectPressed">IsObjectPressed</h4>
Check object pressed state.

 > (`bool` bPressed) ItemBox:IsObjectPressed()

 ````lua
 local bPressed = ItemBox:IsObjectPressed()
 ````

* <h4 id="LuaItemBox_SetCoolDownPercentage">SetCoolDownPercentage</h4>
Set cooldown percentage.

 > (`void`) ItemBox:SetCoolDownPercentage(`number` fPercent)

 ````lua
 ItemBox:SetCoolDownPercentage(0.5)
 ````

* <h4 id="LuaItemBox_GetCoolDownPercentage">GetCoolDownPercentage</h4>
Get cooldown percentage.

 > (`number` fPercent) ItemBox:GetCoolDownPercentage()

 ````lua
 local fPercent = ItemBox:GetCoolDownPercentage()
 ````

* <h4 id="LuaItemBox_SetObjectCoolDownType">SetObjectCoolDownType</h4>
Set cooldown type.

 > (`void`) ItemBox:SetObjectCoolDownType(`number` dwType)

 ````lua
 ItemBox:SetObjectCoolDownType(0)
 ````

* <h4 id="LuaItemBox_SetObjectIcon">SetObjectIcon</h4>
Set object icon id.

 > (`void`) ItemBox:SetObjectIcon(`number` nIconID)

 ````lua
 ItemBox:SetObjectIcon(123)
 ````

* <h4 id="LuaItemBox_GetObjectIcon">GetObjectIcon</h4>
Get object icon id.

 > (`number` nIconID) ItemBox:GetObjectIcon()

 ````lua
 local nIconID = ItemBox:GetObjectIcon()
 ````

* <h4 id="LuaItemBox_GetObjectIconPath">GetObjectIconPath</h4>
Get object icon file path.

 > (`string` szPath) ItemBox:GetObjectIconPath()

 ````lua
 local szPath = ItemBox:GetObjectIconPath()
 ````

* <h4 id="LuaItemBox_ClearObjectIcon">ClearObjectIcon</h4>
Clear object icon.

 > (`void`) ItemBox:ClearObjectIcon()

 ````lua
 ItemBox:ClearObjectIcon()
 ````

* <h4 id="LuaItemBox_SetOverText">SetOverText</h4>
Set over text by index.

 > (`void`) ItemBox:SetOverText(`number` nOverTextIndex, `string` szText)

 ````lua
 ItemBox:SetOverText(0, "text")
 ````

* <h4 id="LuaItemBox_GetOverText">GetOverText</h4>
Get over text by index.

 > (`string` szText) ItemBox:GetOverText(`number` nOverTextIndex)

 ````lua
 local szText = ItemBox:GetOverText(0)
 ````

* <h4 id="LuaItemBox_SetOverTextFontScheme">SetOverTextFontScheme</h4>
Set font scheme for over text.

 > (`void`) ItemBox:SetOverTextFontScheme(`number` nOverTextIndex, `number` nFontScheme)

 ````lua
 ItemBox:SetOverTextFontScheme(0, 0)
 ````

* <h4 id="LuaItemBox_GetOverTextFontScheme">GetOverTextFontScheme</h4>
Get font scheme for over text.

 > (`number` nFontScheme) ItemBox:GetOverTextFontScheme(`number` nOverTextIndex)

 ````lua
 local nFontScheme = ItemBox:GetOverTextFontScheme(0)
 ````

* <h4 id="LuaItemBox_SetOverTextPosition">SetOverTextPosition</h4>
Set over text position.

`fOffsetX`/`fOffsetY` are unscaled values on Lua side; internally they are multiplied by UIScale.

 > (`void`) ItemBox:SetOverTextPosition(`number` nOverTextIndex, `number` nPos[, `number` fOffsetX[, `number` fOffsetY]])

 ````lua
 ItemBox:SetOverTextPosition(0, 0)
 ItemBox:SetOverTextPosition(0, 0, 10)
 ItemBox:SetOverTextPosition(0, 0, 10, 10)
 ````

* <h4 id="LuaItemBox_GetOverTextPosition">GetOverTextPosition</h4>
Get over text position.

 > (`number` nPos) ItemBox:GetOverTextPosition(`number` nOverTextIndex)

 ````lua
 local nPos = ItemBox:GetOverTextPosition(0)
 ````

* <h4 id="LuaItemBox_SetExtentImage">SetExtentImage</h4>
Set extent layer 0 as an image.

 > (`void`) ItemBox:SetExtentImage(`string` szImage, `number` nFrame)

 ````lua
 ItemBox:SetExtentImage("interface/ui/image/tex.tga", 0)
 ````

* <h4 id="LuaItemBox_ClearExtentImage">ClearExtentImage</h4>
Clear extent layer 0.

 > (`void`) ItemBox:ClearExtentImage()

 ````lua
 ItemBox:ClearExtentImage()
 ````

* <h4 id="LuaItemBox_SetExtentAnimate">SetExtentAnimate</h4>
Set extent layer 1 as an animate.

 > (`void`) ItemBox:SetExtentAnimate(`string` szImage, `number` nGroup[, `number` nLoopCount = -1])

 ````lua
 ItemBox:SetExtentAnimate("interface/ui/ani/ani.tga", 0)
 ItemBox:SetExtentAnimate("interface/ui/ani/ani.tga", 0, -1)
 ````

* <h4 id="LuaItemBox_ClearExtentAnimate">ClearExtentAnimate</h4>
Clear extent layer 1.

 > (`void`) ItemBox:ClearExtentAnimate()

 ````lua
 ItemBox:ClearExtentAnimate()
 ````

* <h4 id="LuaItemBox_IsPlayingExAnimate">IsPlayingExAnimate</h4>
Whether extent layer 1 animate is playing.

 > (`bool` bPlaying) ItemBox:IsPlayingExAnimate()

 ````lua
 local bPlaying = ItemBox:IsPlayingExAnimate()
 ````

* <h4 id="LuaItemBox_SetExtentLayer">SetExtentLayer</h4>
Set extent layer (generic).

 > (`void`) ItemBox:SetExtentLayer(`number` uLayer, `string` szImage, `number` nFrame[, `number` nLoopCount])

 ````lua
 ItemBox:SetExtentLayer(2, "interface/ui/image/tex.tga", 0)
 ItemBox:SetExtentLayer(2, "interface/ui/image/tex.tga", 0, -1)
 ````

* <h4 id="LuaItemBox_GetExtentLayer">GetExtentLayer</h4>
Get extent layer info.

 > (`string` szImage, `number` nFrame, `number` nLoopCount) ItemBox:GetExtentLayer(`number` uLayer)

 ````lua
 local szImage, nFrame, nLoopCount = ItemBox:GetExtentLayer(2)
 ````

* <h4 id="LuaItemBox_ClearExtentLayer">ClearExtentLayer</h4>
Clear extent layer.

- If `uLayer` is provided: clears that layer.
- If `uLayer` is not provided: clears all layers.

 > (`void`) ItemBox:ClearExtentLayer([`number` uLayer])

 ````lua
 ItemBox:ClearExtentLayer(2)
 ItemBox:ClearExtentLayer()
 ````

* <h4 id="LuaItemBox_IsExtentAnimatePlaying">IsExtentAnimatePlaying</h4>
Whether an extent animate layer is playing.

 > (`bool` bPlaying) ItemBox:IsExtentAnimatePlaying(`number` uLayer)

 ````lua
 local bPlaying = ItemBox:IsExtentAnimatePlaying(1)
 ````

* <h4 id="LuaItemBox_SetExtentImageType">SetExtentImageType</h4>
Set extent layer image type.

 > (`void`) ItemBox:SetExtentImageType(`number` uLayer, `number` dwType)

 ````lua
 ItemBox:SetExtentImageType(0, 0)
 ````

* <h4 id="LuaItemBox_SetExtentAnimateType">SetExtentAnimateType</h4>
Set extent layer animate type.

 > (`void`) ItemBox:SetExtentAnimateType(`number` uLayer, `number` dwType)

 ````lua
 ItemBox:SetExtentAnimateType(1, 0)
 ````

* <h4 id="LuaItemBox_GetExtentPercent">GetExtentPercent</h4>
Get extent percent.

 > (`number` fPercent) ItemBox:GetExtentPercent(`number` uLayer)

 ````lua
 local fPercent = ItemBox:GetExtentPercent(0)
 ````

* <h4 id="LuaItemBox_SetExtentPercent">SetExtentPercent</h4>
Set extent percent.

 > (`void`) ItemBox:SetExtentPercent(`number` uLayer, `number` fPercent)

 ````lua
 ItemBox:SetExtentPercent(0, 1.0)
 ````

* <h4 id="LuaItemBox_GetExtentVisible">GetExtentVisible</h4>
Get extent visibility.

 > (`bool` bVisible) ItemBox:GetExtentVisible(`number` uLayer)

 ````lua
 local bVisible = ItemBox:GetExtentVisible(0)
 ````

* <h4 id="LuaItemBox_SetExtentVisible">SetExtentVisible</h4>
Set extent visibility.

 > (`void`) ItemBox:SetExtentVisible(`number` uLayer, `bool` bVisible)

 ````lua
 ItemBox:SetExtentVisible(0, true)
 ````

* <h4 id="LuaItemBox_SetExtentTimeStartAngle">SetExtentTimeStartAngle</h4>
Set extent time start angle.

 > (`void`) ItemBox:SetExtentTimeStartAngle(`number` uLayer, `number` fAngle)

 ````lua
 ItemBox:SetExtentTimeStartAngle(0, 0)
 ````

* <h4 id="LuaItemBox_IconToGray">IconToGray</h4>
Gray object icon.

 > (`void`) ItemBox:IconToGray()

 ````lua
 ItemBox:IconToGray()
 ````

* <h4 id="LuaItemBox_IconToNormal">IconToNormal</h4>
Restore object icon.

 > (`void`) ItemBox:IconToNormal()

 ````lua
 ItemBox:IconToNormal()
 ````

* <h4 id="LuaItemBox_IsIconGray">IsIconGray</h4>
Check whether icon is gray.

 > (`bool` bGray) ItemBox:IsIconGray()

 ````lua
 local bGray = ItemBox:IsIconGray()
 ````

* <h4 id="LuaItemBox_SetStateResID">SetStateResID</h4>
Set state resource id.

 > (`void`) ItemBox:SetStateResID(`number` eType, `number` nResID)

 ````lua
 ItemBox:SetStateResID(0, 0)
 ````

* <h4 id="LuaItemBox_ExchangeDrawOrder">ExchangeDrawOrder</h4>
Exchange draw order between layers.

 > (`void`) ItemBox:ExchangeDrawOrder(`number` uSrc, `number` uDst)

 ````lua
 ItemBox:ExchangeDrawOrder(0, 1)
 ````
