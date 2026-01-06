# ItemHandle

Notes:

- For position/size related APIs, Lua side uses **unscaled UI coordinates**. Internally values are multiplied by `Station.GetUIScale()`. Corresponding getters divide by UIScale before returning.

[`AppendItemFromString`](#LuaItemHandle_AppendItemFromString)
[`AppendItemFromIni`](#LuaItemHandle_AppendItemFromIni)
[`AdjustItemShowInfo`](#LuaItemHandle_AdjustItemShowInfo)
[`InsertItemFromString`](#LuaItemHandle_InsertItemFromString)
[`InsertItemFromIni`](#LuaItemHandle_InsertItemFromIni)
[`FormatAllItemPos`](#LuaItemHandle_FormatAllItemPos)
[`SetHandleStyle`](#LuaItemHandle_SetHandleStyle)
[`SetMinRowHeight`](#LuaItemHandle_SetMinRowHeight)
[`SetMaxRowHeight`](#LuaItemHandle_SetMaxRowHeight)
[`SetRowHeight`](#LuaItemHandle_SetRowHeight)
[`SetRowSpacing`](#LuaItemHandle_SetRowSpacing)
[`GetRowSpacing`](#LuaItemHandle_GetRowSpacing)
[`RemoveItem`](#LuaItemHandle_RemoveItem)
[`Clear`](#LuaItemHandle_Clear)
[`GetItemStartRelPos`](#LuaItemHandle_GetItemStartRelPos)
[`SetItemStartRelPos`](#LuaItemHandle_SetItemStartRelPos)
[`SetSizeByAllItemSize`](#LuaItemHandle_SetSizeByAllItemSize)
[`GetAllItemSize`](#LuaItemHandle_GetAllItemSize)
[`GetItemCount`](#LuaItemHandle_GetItemCount)
[`GetVisibleItemCount`](#LuaItemHandle_GetVisibleItemCount)
[`Lookup`](#LuaItemHandle_Lookup)
[`EnableFormatWhenAppend`](#LuaItemHandle_EnableFormatWhenAppend)
[`RemoveItemUntilNewLine`](#LuaItemHandle_RemoveItemUntilNewLine)
[`ExchangeItemIndex`](#LuaItemHandle_ExchangeItemIndex)
[`Sort`](#LuaItemHandle_Sort)
[`AppendItemFromData`](#LuaItemHandle_AppendItemFromData)
[`IsInStencialArea`](#LuaItemHandle_IsInStencialArea)
[`SetVAlign`](#LuaItemHandle_SetVAlign)
[`GetVAlign`](#LuaItemHandle_GetVAlign)
[`SetHAlign`](#LuaItemHandle_SetHAlign)
[`GetHAlign`](#LuaItemHandle_GetHAlign)
[`IsIgnoreInvisibleChild`](#LuaItemHandle_IsIgnoreInvisibleChild)
[`SetIgnoreInvisibleChild`](#LuaItemHandle_SetIgnoreInvisibleChild)
[`LoadShapTexture`](#LuaItemHandle_LoadShapTexture)
[`UnloadShapTexture`](#LuaItemHandle_UnloadShapTexture)

* <h4 id="LuaItemHandle_AppendItemFromString">AppendItemFromString</h4>
Append item(s) from an encoded string.

 > (`void`) ItemHandle:AppendItemFromString(`string` szString)

 ````lua
 ItemHandle:AppendItemFromString("...")
 ````

* <h4 id="LuaItemHandle_AppendItemFromIni">AppendItemFromIni</h4>
Append item from an ini section.

Returns the created item.

 > (`ItemNull` Item) ItemHandle:AppendItemFromIni(`string` szIniFile, `string` szSectionName[, `string` szNewName[, `bool` bEnableCache]])

 ````lua
 local Item = ItemHandle:AppendItemFromIni("interface/ui/test.ini", "Item", "NewName")
 ````

* <h4 id="LuaItemHandle_AppendItemFromData">AppendItemFromData</h4>
Append item from `ItemData` userdata.

Returns the created item.

 > (`ItemNull` Item) ItemHandle:AppendItemFromData(`userdata` ItemData[, `string` szNewName])

 ````lua
 local Item = ItemHandle:AppendItemFromData(ItemData)
 ````

* <h4 id="LuaItemHandle_AdjustItemShowInfo">AdjustItemShowInfo</h4>
Adjust item show info.

 > (`void`) ItemHandle:AdjustItemShowInfo()

 ````lua
 ItemHandle:AdjustItemShowInfo()
 ````

* <h4 id="LuaItemHandle_InsertItemFromString">InsertItemFromString</h4>
Insert item(s) from an encoded string.

`ref` can be:

- `number`: item index
- `string`: tree path

`bBehindOrBefore` can be boolean or number.

 > (`void`) ItemHandle:InsertItemFromString(`number|string` ref, `bool|number` bBehindOrBefore, `string` szString)

 ````lua
 ItemHandle:InsertItemFromString(0, true, "...")
 ItemHandle:InsertItemFromString("ChildPath", false, "...")
 ````

* <h4 id="LuaItemHandle_InsertItemFromIni">InsertItemFromIni</h4>
Insert item from ini section.

Returns the created item.

`ref` and `bBehindOrBefore` are the same as [`InsertItemFromString`](#LuaItemHandle_InsertItemFromString).

 > (`ItemNull` Item) ItemHandle:InsertItemFromIni(`number|string` ref, `bool|number` bBehindOrBefore, `string` szIniFile, `string` szSectionName[, `string` szNewName])

 ````lua
 local Item = ItemHandle:InsertItemFromIni(0, true, "interface/ui/test.ini", "Item")
 ````

* <h4 id="LuaItemHandle_FormatAllItemPos">FormatAllItemPos</h4>
Format all item positions.

If `bNotifyLua` is `true`, it will call `LuaNotifyUIFormatAllPos`.

 > (`void`) ItemHandle:FormatAllItemPos([`bool` bNotifyLua = false])

 ````lua
 ItemHandle:FormatAllItemPos()
 ItemHandle:FormatAllItemPos(true)
 ````

* <h4 id="LuaItemHandle_SetHandleStyle">SetHandleStyle</h4>
Set handle style.

 > (`void`) ItemHandle:SetHandleStyle(`number` dwHandleStyle)

 ````lua
 ItemHandle:SetHandleStyle(0)
 ````

* <h4 id="LuaItemHandle_SetMinRowHeight">SetMinRowHeight</h4>
Set minimum row height.

 > (`void`) ItemHandle:SetMinRowHeight(`number` fHeight)

 ````lua
 ItemHandle:SetMinRowHeight(20)
 ````

* <h4 id="LuaItemHandle_SetMaxRowHeight">SetMaxRowHeight</h4>
Set maximum row height.

 > (`void`) ItemHandle:SetMaxRowHeight(`number` fHeight)

 ````lua
 ItemHandle:SetMaxRowHeight(60)
 ````

* <h4 id="LuaItemHandle_SetRowHeight">SetRowHeight</h4>
Set row height.

 > (`void`) ItemHandle:SetRowHeight(`number` fHeight)

 ````lua
 ItemHandle:SetRowHeight(30)
 ````

* <h4 id="LuaItemHandle_SetRowSpacing">SetRowSpacing</h4>
Set row spacing.

 > (`void`) ItemHandle:SetRowSpacing(`number` fSpacing)

 ````lua
 ItemHandle:SetRowSpacing(4)
 ````

* <h4 id="LuaItemHandle_GetRowSpacing">GetRowSpacing</h4>
Get row spacing.

 > (`number` fSpacing) ItemHandle:GetRowSpacing()

 ````lua
 local fSpacing = ItemHandle:GetRowSpacing()
 ````

* <h4 id="LuaItemHandle_RemoveItem">RemoveItem</h4>
Remove an item.

Argument can be:

- `number`: item index
- `ItemNull` (table userdata)
- `string`: tree path

 > (`void`) ItemHandle:RemoveItem(`number|ItemNull|string` item)

 ````lua
 ItemHandle:RemoveItem(0)
 ItemHandle:RemoveItem("ChildPath")
 ItemHandle:RemoveItem(ItemNull)
 ````

* <h4 id="LuaItemHandle_Clear">Clear</h4>
Clear all child items.

 > (`void`) ItemHandle:Clear()

 ````lua
 ItemHandle:Clear()
 ````

* <h4 id="LuaItemHandle_GetItemStartRelPos">GetItemStartRelPos</h4>
Get child start relative position.

 > (`number` x, `number` y) ItemHandle:GetItemStartRelPos()

 ````lua
 local x, y = ItemHandle:GetItemStartRelPos()
 ````

* <h4 id="LuaItemHandle_SetItemStartRelPos">SetItemStartRelPos</h4>
Set child start relative position.

 > (`void`) ItemHandle:SetItemStartRelPos(`number` x, `number` y)

 ````lua
 ItemHandle:SetItemStartRelPos(0, 0)
 ````

* <h4 id="LuaItemHandle_SetSizeByAllItemSize">SetSizeByAllItemSize</h4>
Set handle size by all child item size.

 > (`void`) ItemHandle:SetSizeByAllItemSize()

 ````lua
 ItemHandle:SetSizeByAllItemSize()
 ````

* <h4 id="LuaItemHandle_GetAllItemSize">GetAllItemSize</h4>
Get all child item size.

 > (`number` w, `number` h) ItemHandle:GetAllItemSize()

 ````lua
 local w, h = ItemHandle:GetAllItemSize()
 ````

* <h4 id="LuaItemHandle_GetItemCount">GetItemCount</h4>
Get item count.

 > (`number` nCount) ItemHandle:GetItemCount()

 ````lua
 local nCount = ItemHandle:GetItemCount()
 ````

* <h4 id="LuaItemHandle_GetVisibleItemCount">GetVisibleItemCount</h4>
Get visible item count.

 > (`number` nCount) ItemHandle:GetVisibleItemCount()

 ````lua
 local nCount = ItemHandle:GetVisibleItemCount()
 ````

* <h4 id="LuaItemHandle_Lookup">Lookup</h4>
Lookup child item.

Argument can be index or tree path.

 > (`ItemNull` Item) ItemHandle:Lookup(`number|string` ref)

 ````lua
 local Item = ItemHandle:Lookup(0)
 local Item = ItemHandle:Lookup("ChildPath")
 ````

* <h4 id="LuaItemHandle_EnableFormatWhenAppend">EnableFormatWhenAppend</h4>
Enable/disable auto formatting when appending.

 > (`void`) ItemHandle:EnableFormatWhenAppend(`bool|number` bEnable)

 ````lua
 ItemHandle:EnableFormatWhenAppend(true)
 ````

* <h4 id="LuaItemHandle_RemoveItemUntilNewLine">RemoveItemUntilNewLine</h4>
Remove items until new line.

 > (`void`) ItemHandle:RemoveItemUntilNewLine()

 ````lua
 ItemHandle:RemoveItemUntilNewLine()
 ````

* <h4 id="LuaItemHandle_ExchangeItemIndex">ExchangeItemIndex</h4>
Exchange two item indices.

Each argument can be a numeric index or an `ItemNull` (table userdata) under this handle.

 > (`void`) ItemHandle:ExchangeItemIndex(`number|ItemNull` a, `number|ItemNull` b)

 ````lua
 ItemHandle:ExchangeItemIndex(0, 1)
 ItemHandle:ExchangeItemIndex(ItemA, ItemB)
 ````

* <h4 id="LuaItemHandle_Sort">Sort</h4>
Sort items.

 > (`void`) ItemHandle:Sort()

 ````lua
 ItemHandle:Sort()
 ````

* <h4 id="LuaItemHandle_IsInStencialArea">IsInStencialArea</h4>
Test whether a point is in stencil area.

`fAbsX`/`fAbsY` are unscaled values on Lua side; internally they are multiplied by UIScale.

 > (`bool` bInArea) ItemHandle:IsInStencialArea(`number` fAbsX, `number` fAbsY)

 ````lua
 local bInArea = ItemHandle:IsInStencialArea(100, 100)
 ````

* <h4 id="LuaItemHandle_SetVAlign">SetVAlign</h4>
Set vertical align style.

 > (`void`) ItemHandle:SetVAlign(`number` nValign)

 ````lua
 ItemHandle:SetVAlign(0)
 ````

* <h4 id="LuaItemHandle_GetVAlign">GetVAlign</h4>
Get vertical align style.

 > (`number` nValign) ItemHandle:GetVAlign()

 ````lua
 local nValign = ItemHandle:GetVAlign()
 ````

* <h4 id="LuaItemHandle_SetHAlign">SetHAlign</h4>
Set horizontal align style.

 > (`void`) ItemHandle:SetHAlign(`number` nHalign)

 ````lua
 ItemHandle:SetHAlign(0)
 ````

* <h4 id="LuaItemHandle_GetHAlign">GetHAlign</h4>
Get horizontal align style.

 > (`number` nHalign) ItemHandle:GetHAlign()

 ````lua
 local nHalign = ItemHandle:GetHAlign()
 ````

* <h4 id="LuaItemHandle_IsIgnoreInvisibleChild">IsIgnoreInvisibleChild</h4>
Whether to ignore invisible child.

 > (`bool` bIgnore) ItemHandle:IsIgnoreInvisibleChild()

 ````lua
 local bIgnore = ItemHandle:IsIgnoreInvisibleChild()
 ````

* <h4 id="LuaItemHandle_SetIgnoreInvisibleChild">SetIgnoreInvisibleChild</h4>
Set whether to ignore invisible child.

 > (`void`) ItemHandle:SetIgnoreInvisibleChild(`bool` bIgnore)

 ````lua
 ItemHandle:SetIgnoreInvisibleChild(true)
 ````

* <h4 id="LuaItemHandle_LoadShapTexture">LoadShapTexture</h4>
Load shap texture.

 > (`void`) ItemHandle:LoadShapTexture(`string` szFile)

 ````lua
 ItemHandle:LoadShapTexture("interface/ui/image/shape.tga")
 ````

* <h4 id="LuaItemHandle_UnloadShapTexture">UnloadShapTexture</h4>
Unload shap texture.

 > (`void`) ItemHandle:UnloadShapTexture()

 ````lua
 ItemHandle:UnloadShapTexture()
 ````
