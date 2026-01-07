[English](./ItemHandle.md) | 中文

# ItemHandle（句柄）

说明：

- 对于位置/尺寸相关 API：Lua 侧使用**未缩放的 UI 坐标**。内部会把输入乘以 `Station.GetUIScale()`；对应的 Get* 会再除以 UIScale 后返回。

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
从编码字符串追加组件。

内部会将 `szString` 按当前代码页转换为宽字符串，并使用 `Station.GetUIScale()` 参与解码参数。

 > (`void`) ItemHandle:AppendItemFromString(`string` szString)

 ````lua
 ItemHandle:AppendItemFromString("...")
 ````

* <h4 id="LuaItemHandle_AppendItemFromIni">AppendItemFromIni</h4>
从 ini 文件的某个 section 追加组件。

`szIniFile` 会经过 `FormatFilePath()` 与路径调整后再尝试打开。

返回创建的组件；若传入 `szNewName`，会在创建后设置组件名称。

 > (`ItemNull` Item) ItemHandle:AppendItemFromIni(`string` szIniFile, `string` szSectionName[, `string` szNewName[, `bool` bEnableCache]])

 ````lua
 local Item = ItemHandle:AppendItemFromIni("interface/ui/test.ini", "Item", "NewName")
 ````

* <h4 id="LuaItemHandle_AppendItemFromData">AppendItemFromData</h4>
从 `ItemData` userdata 追加组件。

返回创建的组件；若传入 `szNewName`，其不能为空字符串。

 > (`ItemNull` Item) ItemHandle:AppendItemFromData(`userdata` ItemData[, `string` szNewName])

 ````lua
 local Item = ItemHandle:AppendItemFromData(ItemData)
 ````

* <h4 id="LuaItemHandle_AdjustItemShowInfo">AdjustItemShowInfo</h4>
更新/调整子组件的显示信息。

 > (`void`) ItemHandle:AdjustItemShowInfo()

 ````lua
 ItemHandle:AdjustItemShowInfo()
 ````

* <h4 id="LuaItemHandle_InsertItemFromString">InsertItemFromString</h4>
从编码字符串插入组件。

插入位置由 `ref` 与 `bBehindOrBefore` 决定；当 Handle 为空或 `ref` 越界时会退化为追加。

`ref` 可以是：

- `number`：子组件索引
- `string`：树路径

`bBehindOrBefore` 可以是布尔值或数字。

 > (`void`) ItemHandle:InsertItemFromString(`number|string` ref, `bool|number` bBehindOrBefore, `string` szString)

 ````lua
 ItemHandle:InsertItemFromString(0, true, "...")
 ItemHandle:InsertItemFromString("ChildPath", false, "...")
 ````

* <h4 id="LuaItemHandle_InsertItemFromIni">InsertItemFromIni</h4>
从 ini 节加载并插入组件。

返回创建的组件。

`ref` 与 `bBehindOrBefore` 的含义与 [`InsertItemFromString`](#LuaItemHandle_InsertItemFromString) 相同。

 > (`ItemNull` Item) ItemHandle:InsertItemFromIni(`number|string` ref, `bool|number` bBehindOrBefore, `string` szIniFile, `string` szSectionName[, `string` szNewName])

 ````lua
 local Item = ItemHandle:InsertItemFromIni(0, true, "interface/ui/test.ini", "Item")
 ````

* <h4 id="LuaItemHandle_FormatAllItemPos">FormatAllItemPos</h4>
格式化所有组件位置。

如果 `bNotifyLua` 为 `true`，则会调用 `LuaNotifyUIFormatAllPos`。

 > (`void`) ItemHandle:FormatAllItemPos([`bool` bNotifyLua = false])

 ````lua
 ItemHandle:FormatAllItemPos()
 ItemHandle:FormatAllItemPos(true)
 ````

* <h4 id="LuaItemHandle_SetHandleStyle">SetHandleStyle</h4>
设置 handle 样式。

 > (`void`) ItemHandle:SetHandleStyle(`number` dwHandleStyle)

 ````lua
 ItemHandle:SetHandleStyle(0)
 ````

* <h4 id="LuaItemHandle_SetMinRowHeight">SetMinRowHeight</h4>
设置minimum row 高度。

 > (`void`) ItemHandle:SetMinRowHeight(`number` fHeight)

 ````lua
 ItemHandle:SetMinRowHeight(20)
 ````

* <h4 id="LuaItemHandle_SetMaxRowHeight">SetMaxRowHeight</h4>
设置maximum row 高度。

 > (`void`) ItemHandle:SetMaxRowHeight(`number` fHeight)

 ````lua
 ItemHandle:SetMaxRowHeight(60)
 ````

* <h4 id="LuaItemHandle_SetRowHeight">SetRowHeight</h4>
设置row 高度。

 > (`void`) ItemHandle:SetRowHeight(`number` fHeight)

 ````lua
 ItemHandle:SetRowHeight(30)
 ````

* <h4 id="LuaItemHandle_SetRowSpacing">SetRowSpacing</h4>
设置row 间距。

 > (`void`) ItemHandle:SetRowSpacing(`number` fSpacing)

 ````lua
 ItemHandle:SetRowSpacing(4)
 ````

* <h4 id="LuaItemHandle_GetRowSpacing">GetRowSpacing</h4>
获取row 间距。

 > (`number` fSpacing) ItemHandle:GetRowSpacing()

 ````lua
 local fSpacing = ItemHandle:GetRowSpacing()
 ````

* <h4 id="LuaItemHandle_RemoveItem">RemoveItem</h4>
移除一个子组件。

参数可以是：

- `number`：子组件索引
- `ItemNull`（table userdata）
- `string`：树路径

 > (`void`) ItemHandle:RemoveItem(`number|ItemNull|string` item)

 ````lua
 ItemHandle:RemoveItem(0)
 ItemHandle:RemoveItem("ChildPath")
 ItemHandle:RemoveItem(ItemNull)
 ````

* <h4 id="LuaItemHandle_Clear">Clear</h4>
清空所有子组件。

 > (`void`) ItemHandle:Clear()

 ````lua
 ItemHandle:Clear()
 ````

* <h4 id="LuaItemHandle_GetItemStartRelPos">GetItemStartRelPos</h4>
获取子组件的起始相对位置。

返回值已从内部坐标除以 UIScale。

发生错误时会报错，并返回 `(0, 0)`。

 > (`number` x, `number` y) ItemHandle:GetItemStartRelPos()

 ````lua
 local x, y = ItemHandle:GetItemStartRelPos()
 ````

* <h4 id="LuaItemHandle_SetItemStartRelPos">SetItemStartRelPos</h4>
设置子组件的起始相对位置。

`x`/`y` 在 Lua 侧为未缩放值；内部会乘以 UIScale。

 > (`void`) ItemHandle:SetItemStartRelPos(`number` x, `number` y)

 ````lua
 ItemHandle:SetItemStartRelPos(0, 0)
 ````

* <h4 id="LuaItemHandle_SetSizeByAllItemSize">SetSizeByAllItemSize</h4>
根据所有子组件的总尺寸设置 Handle 自身尺寸。

 > (`void`) ItemHandle:SetSizeByAllItemSize()

 ````lua
 ItemHandle:SetSizeByAllItemSize()
 ````

* <h4 id="LuaItemHandle_GetAllItemSize">GetAllItemSize</h4>
获取所有子组件的总尺寸。

返回值已从内部坐标除以 UIScale。

发生错误时会报错，并返回 `(0, 0)`。

 > (`number` w, `number` h) ItemHandle:GetAllItemSize()

 ````lua
 local w, h = ItemHandle:GetAllItemSize()
 ````

* <h4 id="LuaItemHandle_GetItemCount">GetItemCount</h4>
获取组件 count。

 > (`number` nCount) ItemHandle:GetItemCount()

 ````lua
 local nCount = ItemHandle:GetItemCount()
 ````

* <h4 id="LuaItemHandle_GetVisibleItemCount">GetVisibleItemCount</h4>
获取visible 组件 count。

 > (`number` nCount) ItemHandle:GetVisibleItemCount()

 ````lua
 local nCount = ItemHandle:GetVisibleItemCount()
 ````

* <h4 id="LuaItemHandle_Lookup">Lookup</h4>
查找子组件。

参数可以是索引或树路径。

如果找不到对应组件，则不返回任何值。

 > (`ItemNull` Item) ItemHandle:Lookup(`number|string` ref)

 ````lua
 local Item = ItemHandle:Lookup(0)
 local Item = ItemHandle:Lookup("ChildPath")
 ````

* <h4 id="LuaItemHandle_EnableFormatWhenAppend">EnableFormatWhenAppend</h4>
启用/禁用追加组件时的自动排版。

 > (`void`) ItemHandle:EnableFormatWhenAppend(`bool|number` bEnable)

 ````lua
 ItemHandle:EnableFormatWhenAppend(true)
 ````

* <h4 id="LuaItemHandle_RemoveItemUntilNewLine">RemoveItemUntilNewLine</h4>
移除组件直到新行。

 > (`void`) ItemHandle:RemoveItemUntilNewLine()

 ````lua
 ItemHandle:RemoveItemUntilNewLine()
 ````

* <h4 id="LuaItemHandle_ExchangeItemIndex">ExchangeItemIndex</h4>
交换两个组件的索引。

每个参数都可以是数字索引，或该 Handle 下的 `ItemNull`（table userdata）。

 > (`void`) ItemHandle:ExchangeItemIndex(`number|ItemNull` a, `number|ItemNull` b)

 ````lua
 ItemHandle:ExchangeItemIndex(0, 1)
 ItemHandle:ExchangeItemIndex(ItemA, ItemB)
 ````

* <h4 id="LuaItemHandle_Sort">Sort</h4>
对组件进行排序。

 > (`void`) ItemHandle:Sort()

 ````lua
 ItemHandle:Sort()
 ````

* <h4 id="LuaItemHandle_IsInStencialArea">IsInStencialArea</h4>
测试点是否位于 stencil 区域内。

`fAbsX`/`fAbsY` 在 Lua 侧为未缩放值；内部会乘以 UIScale。

 > (`bool` bInArea) ItemHandle:IsInStencialArea(`number` fAbsX, `number` fAbsY)

 ````lua
 local bInArea = ItemHandle:IsInStencialArea(100, 100)
 ````

* <h4 id="LuaItemHandle_SetVAlign">SetVAlign</h4>
设置垂直对齐方式。

 > (`void`) ItemHandle:SetVAlign(`number` nValign)

 ````lua
 ItemHandle:SetVAlign(0)
 ````

* <h4 id="LuaItemHandle_GetVAlign">GetVAlign</h4>
获取垂直对齐方式。

 > (`number` nValign) ItemHandle:GetVAlign()

 ````lua
 local nValign = ItemHandle:GetVAlign()
 ````

* <h4 id="LuaItemHandle_SetHAlign">SetHAlign</h4>
设置水平对齐方式。

 > (`void`) ItemHandle:SetHAlign(`number` nHalign)

 ````lua
 ItemHandle:SetHAlign(0)
 ````

* <h4 id="LuaItemHandle_GetHAlign">GetHAlign</h4>
获取水平对齐方式。

 > (`number` nHalign) ItemHandle:GetHAlign()

 ````lua
 local nHalign = ItemHandle:GetHAlign()
 ````

* <h4 id="LuaItemHandle_IsIgnoreInvisibleChild">IsIgnoreInvisibleChild</h4>
获取是否忽略不可见子组件。

 > (`bool` bIgnore) ItemHandle:IsIgnoreInvisibleChild()

 ````lua
 local bIgnore = ItemHandle:IsIgnoreInvisibleChild()
 ````

* <h4 id="LuaItemHandle_SetIgnoreInvisibleChild">SetIgnoreInvisibleChild</h4>
设置是否忽略不可见子组件。

 > (`void`) ItemHandle:SetIgnoreInvisibleChild(`bool` bIgnore)

 ````lua
 ItemHandle:SetIgnoreInvisibleChild(true)
 ````

* <h4 id="LuaItemHandle_LoadShapTexture">LoadShapTexture</h4>
加载 shap 纹理。

 > (`void`) ItemHandle:LoadShapTexture(`string` szFile)

 ````lua
 ItemHandle:LoadShapTexture("interface/ui/image/shape.tga")
 ````

* <h4 id="LuaItemHandle_UnloadShapTexture">UnloadShapTexture</h4>
卸载 shap 纹理。

 > (`void`) ItemHandle:UnloadShapTexture()

 ````lua
 ItemHandle:UnloadShapTexture()
 ````
