[English](./WndContainer.md) | 中文

# WndContainer（容器）

说明：

- `WndContainer` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

[`SetContainerType`](#LuaContainer_SetContainerType)
[`FormatAllContentPos`](#LuaContainer_FormatAllContentPos)
[`GetAllContentSize`](#LuaContainer_GetAllContentSize)
[`AppendContentFromIni`](#LuaContainer_AppendContentFromIni)
[`Clear`](#LuaContainer_Clear)
[`GetAllContentCount`](#LuaContainer_GetAllContentCount)
[`SetColumn`](#LuaContainer_SetColumn)
[`SetDrawStyle`](#LuaContainer_SetDrawStyle)
[`LookupContent`](#LuaContainer_LookupContent)
[`SetStartRelPos`](#LuaContainer_SetStartRelPos)
[`GetStartRelPos`](#LuaContainer_GetStartRelPos)
[`SetVAlign`](#LuaContainer_SetVAlign)
[`GetVAlign`](#LuaContainer_GetVAlign)
[`SetHAlign`](#LuaContainer_SetHAlign)
[`GetHAlign`](#LuaContainer_GetHAlign)
[`LoadShapTexture`](#LuaContainer_LoadShapTexture)
[`UnloadShapTexture`](#LuaContainer_UnloadShapTexture)

* <h4 id="LuaContainer_SetContainerType">SetContainerType</h4>

 > (`void`) WndContainer:SetContainerType(`number` nType)

说明：

- 参数个数必须为 2，且实现中要求第 2 个参数必须为 `number`。
- 直接调用底层 `SetContainerType(nContainerType)`。

* <h4 id="LuaContainer_FormatAllContentPos">FormatAllContentPos</h4>

 > (`void`) WndContainer:FormatAllContentPos([`bool|number` bNotifyLua = false])

说明：

- 参数个数允许为 1 或 2。
- 先调用底层 `FormatAllContentPos()`。
- 若传入 `bNotifyLua` 且 `lua_toboolean` 为 true，则会额外调用 `LuaNotifyUIFormatAllPos(L, pWnd)` 通知 Lua（用于同步布局信息）。

* <h4 id="LuaContainer_GetAllContentSize">GetAllContentSize</h4>

 > (`number` w, `number` h) WndContainer:GetAllContentSize()

说明：

- 只接受 `self` 一个参数。
- 返回值会在 Lua 层按 `UIScale` 还原（内部值 / `Station.GetUIScale()`）。

* <h4 id="LuaContainer_AppendContentFromIni">AppendContentFromIni</h4>

 > (`WndWindow` Content) WndContainer:AppendContentFromIni(`string` szIniFile, `string` szSectionName[, `string` szNewName[, `bool|number` bEnableCache]])

说明：

- 参数个数允许为 3、4 或 5。
- `szIniFile` 会先 `FormatFilePath()`，再尝试 `AdjustFilePath(...)`，若调整后的路径存在则优先使用。
- 读取 ini 的方式与缓存开关有关：
	- 若启用缓存（`m_bEnableCache`）：通过 `FrameFileCache` 获取/创建 `IIniFile`（并根据路径前缀判断是否 addon）。
	- 否则：通过 `Config.OpenConfigFileMaxMatching(...)` 打开。
- 创建内容窗口时会包裹在 `KFrameCreateData::Begin/End` 中，并会加载字符串表。
- 若传 `szNewName` 且参数总数为 4，会对新创建的窗口执行 `SetName(szNewName)`。
- 以实现为准：当参数总数为 5 时，第 5 个参数会读取为 `bEnableCache`，但当前实现不会在该分支里应用 `szNewName`（第 4 个参数仍会被传入但不会用于 `SetName`）。
- 成功时返回新创建的内容窗口（通过 `HostStation_Lookup` 推入 Lua）。

* <h4 id="LuaContainer_Clear">Clear</h4>

 > (`void`) WndContainer:Clear()

说明：

- 只接受 `self` 一个参数。
- 清空容器内的所有内容（底层 `Clear()`）。

* <h4 id="LuaContainer_GetAllContentCount">GetAllContentCount</h4>

 > (`number` nCount) WndContainer:GetAllContentCount()

说明：

- 只接受 `self` 一个参数。
- 返回容器内内容数量。

* <h4 id="LuaContainer_SetColumn">SetColumn</h4>

 > (`void`) WndContainer:SetColumn(`bool|number` bColumn)

说明：

- 参数个数必须为 2。
- `bColumn` 会用 `lua_toboolean` 读取（因此实际是开关语义），并调用 `SetColumn(bColumn)`。

* <h4 id="LuaContainer_SetDrawStyle">SetDrawStyle</h4>

 > (`void`) WndContainer:SetDrawStyle(`number` dwStyle)

说明：

- 参数个数必须为 2。
- `dwStyle` 以 `DWORD` 形式传给底层 `SetDrawStyle(dwDrawStyle)`。

* <h4 id="LuaContainer_LookupContent">LookupContent</h4>

 > (`WndWindow` Content) WndContainer:LookupContent(`number` nIndex)

说明：

- 参数个数必须为 2。
- `nIndex` 会按 `number` 读取为索引（`nIndex = (int)lua_tonumber(L, 2)`），并要求 `nIndex >= 0`。
- 找到内容窗口后会通过 `HostStation_Lookup` 返回（找不到则不返回值）。

* <h4 id="LuaContainer_SetStartRelPos">SetStartRelPos</h4>

 > (`void`) WndContainer:SetStartRelPos(`number` x, `number` y)

说明：

- 参数个数必须为 3。
- `x`/`y` 在传入底层前会乘以 `Station.GetUIScale()`。
- 调用底层 `SetContentStartRelPos(fX, fY)`。

* <h4 id="LuaContainer_GetStartRelPos">GetStartRelPos</h4>

 > (`number` x, `number` y) WndContainer:GetStartRelPos()

说明：

- 只接受 `self` 一个参数。
- 返回底层 `GetContentStartRelPos(fX, fY)` 的结果。
- 以实现为准：返回值未在 Lua 层做 `UIScale` 还原（直接把 `fX`/`fY` 推给 Lua）。

* <h4 id="LuaContainer_SetVAlign">SetVAlign</h4>

 > (`void`) WndContainer:SetVAlign(`number` nValign, `number` nReserved)

说明：

- 参数个数必须为 3（实现只读取第 2 个参数作为 `nValign`）。
- `nReserved` 当前实现未读取，但仍需要占位以满足参数个数校验。
- `nValign` 会转换为 `ELEM_V_ALIGN_STYLE` 并调用 `SetVAlign(...)`。

* <h4 id="LuaContainer_GetVAlign">GetVAlign</h4>

 > (`number` nValign) WndContainer:GetVAlign()

说明：

- 只接受 `self` 一个参数。
- 返回当前的 `ELEM_V_ALIGN_STYLE`（数值）。

* <h4 id="LuaContainer_SetHAlign">SetHAlign</h4>

 > (`void`) WndContainer:SetHAlign(`number` nHalign, `number` nReserved)

说明：

- 参数个数必须为 3（实现只读取第 2 个参数作为 `nHalign`）。
- `nReserved` 当前实现未读取，但仍需要占位以满足参数个数校验。
- `nHalign` 会转换为 `ELEM_H_ALIGN_STYLE` 并调用 `SetHAlign(...)`。

* <h4 id="LuaContainer_GetHAlign">GetHAlign</h4>

 > (`number` nHalign) WndContainer:GetHAlign()

说明：

- 只接受 `self` 一个参数。
- 返回当前的 `ELEM_H_ALIGN_STYLE`（数值）。

* <h4 id="LuaContainer_LoadShapTexture">LoadShapTexture</h4>

 > (`void`) WndContainer:LoadShapTexture(`string` szFile)

说明：

- 参数个数必须为 2。
- `szFile` 必须为非空字符串；实现中未对路径做 `FormatFilePath()`。
- 失败时会调用 `LuaMsgError` 输出错误信息，并返回 0 个值。

* <h4 id="LuaContainer_UnloadShapTexture">UnloadShapTexture</h4>

 > (`void`) WndContainer:UnloadShapTexture()

说明：

- 只接受 `self` 一个参数。
- 调用底层 `UnloadShapTexture()`；失败时会 `LuaMsgError`。
