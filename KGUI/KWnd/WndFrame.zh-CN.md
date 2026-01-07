[English](./WndFrame.md) | 中文

# WndFrame（框架）

说明：

- `WndFrame` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

[`EnableDrag`](#LuaFrame_EnableDrag)
[`IsDragable`](#LuaFrame_IsDragable)
[`EnableFollowMouse`](#LuaFrame_EnableFollowMouse)
[`IsFollowMouseMove`](#LuaFrame_IsFollowMouseMove)
[`SetDragArea`](#LuaFrame_SetDragArea)
[`RegisterEvent`](#LuaFrame_RegisterEvent)
[`UnRegisterEvent`](#LuaFrame_UnRegisterEvent)
[`FocusPrev`](#LuaFrame_FocusPrev)
[`FocusNext`](#LuaFrame_FocusNext)
[`FocusHome`](#LuaFrame_FocusHome)
[`FocusEnd`](#LuaFrame_FocusEnd)
[`FadeIn`](#LuaFrame_FadeIn)
[`FadeOut`](#LuaFrame_FadeOut)
[`IsAlwaysTop`](#LuaFrame_IsAlwaysTop)
[`SetAlwaysTop`](#LuaFrame_SetAlwaysTop)
[`ShowWhenUIHide`](#LuaFrame_ShowWhenUIHide)
[`HideWhenUIHide`](#LuaFrame_HideWhenUIHide)
[`IsVisibleWhenUIHide`](#LuaFrame_IsVisibleWhenUIHide)
[`IsAddOn`](#LuaFrame_IsAddOn)
[`CreateItemData`](#LuaFrame_CreateItemData)
[`RemoveItemData`](#LuaFrame_RemoveItemData)
[`LookUpItemData`](#LuaFrame_LookUpItemData)
[`GetItemDataKey`](#LuaFrame_GetItemDataKey)
[`SwitchLayer`](#LuaFrame_SwitchLayer)
[`IsVisibleInCurrentShowMode`](#LuaFrame_IsVisibleInCurrentShowMode)
[`IsVisibleInShowMode`](#LuaFrame_IsVisibleInShowMode)
[`AddShowModeByName`](#LuaFrame_AddShowModeByName)
[`RemoveShowModeByName`](#LuaFrame_RemoveShowModeByName)
[`GetViewLevel`](#LuaFrame_GetViewLevel)
[`IsViewMutex`](#LuaFrame_IsViewMutex)
[`GetViewMutexKey`](#LuaFrame_GetViewMutexKey)
[`IsAddBackGround`](#LuaFrame_IsAddBackGround)

* <h4 id="LuaFrame_EnableDrag">EnableDrag</h4>

 > (`void`) WndFrame:EnableDrag(`bool|number` bEnable)

说明：

- 参数个数必须为 2。
- `bEnable` 支持 `bool` 或 `number`（实现中：bool 用 `lua_toboolean`，否则用 `lua_tonumber`）。
- 实际调用底层 `EnableDrag(bEnable)`。

* <h4 id="LuaFrame_IsDragable">IsDragable</h4>

 > (`bool` bEnable) WndFrame:IsDragable()

说明：

- 只接受 `self` 一个参数。
- 返回底层 `IsDragable()` 的结果（Lua boolean）。

* <h4 id="LuaFrame_EnableFollowMouse">EnableFollowMouse</h4>

 > (`void`) WndFrame:EnableFollowMouse(`bool|number` bEnable)

说明：

- 参数个数必须为 2。
- `bEnable` 支持 `bool` 或 `number`（非 0 视为 true）。
- 实际调用底层 `EnableFollowMouseMove(bEnable)`。

* <h4 id="LuaFrame_IsFollowMouseMove">IsFollowMouseMove</h4>

 > (`bool` bEnable) WndFrame:IsFollowMouseMove()

说明：

- 只接受 `self` 一个参数。
- 返回底层 `IsFollowMouseMove()` 的结果（Lua boolean）。

* <h4 id="LuaFrame_SetDragArea">SetDragArea</h4>

 > (`void`) WndFrame:SetDragArea(`number` x, `number` y, `number` w, `number` h)

说明：

- 参数个数必须为 5。
- `x`/`y`/`w`/`h` 在传入底层前会乘以 `Station.GetUIScale()`（Lua 侧按“未缩放坐标/尺寸”传入）。
- 实际调用底层 `SetDragArea(fX, fY, fW, fH)`。

* <h4 id="LuaFrame_RegisterEvent">RegisterEvent</h4>

 > (`void`) WndFrame:RegisterEvent(`string` szEvent[, `function` fnCallback])

说明：

- 参数个数必须为 2 或 3。
- `szEvent` 必须为非空字符串。
- 传入回调函数时，会通过 `luaL_ref(L, LUA_REGISTRYINDEX)` 保存引用，并将该引用交给 `SubscribeEvent(...)`。
- 未传回调函数时会以 `LUA_NOREF` 订阅事件（事件如何分发由脚本系统决定）。

* <h4 id="LuaFrame_UnRegisterEvent">UnRegisterEvent</h4>

 > (`void`) WndFrame:UnRegisterEvent(`string` szEvent[, `function|number` ref])

说明：

- 参数个数必须为 2 或 3。
- `szEvent` 必须为非空字符串。
- 若传 `ref`：
	- 传 `function`：调用 `UnsubscribeEvent(pWnd, szEvent, 3, false)`（按函数对象取消）。
	- 传 `number`：视为之前保存的 `luaL_ref` 引用，调用 `UnsubscribeEvent(pWnd, szEvent, nRef, true)`。
- 未传 `ref`：调用 `UnsubscribeEvent(pWnd, szEvent, LUA_NOREF, true)`。

* <h4 id="LuaFrame_FocusPrev">FocusPrev</h4>

 > (`bool` bOk) WndFrame:FocusPrev()

说明：

- 只接受 `self` 一个参数。
- 以实现为准：底层 `FocusPrev()` 会返回结果，Lua 层会把该结果作为 boolean 返回。

* <h4 id="LuaFrame_FocusNext">FocusNext</h4>

 > (`bool` bOk) WndFrame:FocusNext()

说明：

- 只接受 `self` 一个参数。
- 以实现为准：底层 `FocusNext()` 会返回结果，Lua 层会把该结果作为 boolean 返回。

* <h4 id="LuaFrame_FocusHome">FocusHome</h4>

 > (`bool` bOk) WndFrame:FocusHome()

说明：

- 只接受 `self` 一个参数。
- 以实现为准：底层 `FocusHome()` 会返回结果，Lua 层会把该结果作为 boolean 返回。

* <h4 id="LuaFrame_FocusEnd">FocusEnd</h4>

 > (`bool` bOk) WndFrame:FocusEnd()

说明：

- 只接受 `self` 一个参数。
- 以实现为准：底层 `FocusEnd()` 会返回结果，Lua 层会把该结果作为 boolean 返回。

* <h4 id="LuaFrame_FadeIn">FadeIn</h4>

 > (`void`) WndFrame:FadeIn(`number` dwTime)

说明：

- 参数个数必须为 2。
- `dwTime` 会以整数形式传给底层 `FadeIn(nCount)`。

* <h4 id="LuaFrame_FadeOut">FadeOut</h4>

 > (`void`) WndFrame:FadeOut(`number` dwTime)

说明：

- 参数个数必须为 2。
- `dwTime` 会以整数形式传给底层 `FadeOut(nCount)`。

* <h4 id="LuaFrame_IsAlwaysTop">IsAlwaysTop</h4>

 > (`bool` bTop) WndFrame:IsAlwaysTop()

说明：

- 只接受 `self` 一个参数。
- 等价于检测窗口样式 `WND_S_ALWAYS_TOP`。

* <h4 id="LuaFrame_SetAlwaysTop">SetAlwaysTop</h4>

 > (`void`) WndFrame:SetAlwaysTop(`bool|number` bTop)

说明：

- 参数个数必须为 2。
- `bTop` 支持 `bool` 或 `number`（非 0 视为 true）。
- 若状态发生变化：
	- 设为 true：设置 `WND_S_ALWAYS_TOP` 并 `BringToTop()`。
	- 设为 false：清除 `WND_S_ALWAYS_TOP`，并尝试插回普通 frame 的最上层（通过 `GetFirstAlwaysTopBrother()` / `AddAsElderBrother(...)`）。

* <h4 id="LuaFrame_ShowWhenUIHide">ShowWhenUIHide</h4>

 > (`void`) WndFrame:ShowWhenUIHide()

说明：

- 只接受 `self` 一个参数。
- 调用底层 `ShowWhenUIHide()`，用于在 UI 隐藏时保持显示。

* <h4 id="LuaFrame_HideWhenUIHide">HideWhenUIHide</h4>

 > (`void`) WndFrame:HideWhenUIHide()

说明：

- 只接受 `self` 一个参数。
- 调用底层 `HideWhenUIHide()`，用于在 UI 隐藏时跟随隐藏。

* <h4 id="LuaFrame_IsVisibleWhenUIHide">IsVisibleWhenUIHide</h4>

 > (`bool` bVisible) WndFrame:IsVisibleWhenUIHide()

说明：

- 只接受 `self` 一个参数。
- 返回底层 `IsVisibleWhenUIHide()` 的结果（Lua boolean）。

* <h4 id="LuaFrame_IsAddOn">IsAddOn</h4>

 > (`bool` bAddOn) WndFrame:IsAddOn()

说明：

- 只接受 `self` 一个参数。
- 返回是否为 AddOn frame（底层 `IsAddOnFrame()`）。

* <h4 id="LuaFrame_CreateItemData">CreateItemData</h4>

 > (`userdata` ItemData) WndFrame:CreateItemData(`string` szIniFile, `string` szSectionName)

说明：

- 参数个数必须为 3：`self` + `szIniFile` + `szSectionName`。
- `szIniFile` 会 `FormatFilePath()`，并会尝试 `AdjustFilePath(...)` 后优先读取调整后的路径；否则读取原路径。
- 读取 ini 后会通过 `KUiComponentsDecoder` 选择/申请缓冲区，加载字符串表并创建 `ItemData`（创建时会使用当前 `UIScale`）。
- 成功时返回一个 Lua `ItemData` 引用（`lua_rawgeti` 推入栈顶）。失败时不返回值，并清理 `nRef`/decoder buffer 等资源。

* <h4 id="LuaFrame_RemoveItemData">RemoveItemData</h4>

 > (`bool` bResult) WndFrame:RemoveItemData(`table|string` ref)

说明：

- 参数个数必须为 2。
- `ref` 支持两种形式：
	- `table`：按 `ItemData` table 取 CData（`ItemData_GetCData`）并从 `m_ItemDataMgr` 移除。
	- `string`：按 key（字符串）从 `m_ItemDataMgr` 移除。
- 返回 boolean（成功路径返回 true）。

* <h4 id="LuaFrame_LookUpItemData">LookUpItemData</h4>

 > (`userdata` ItemData) WndFrame:LookUpItemData(`string` szKey)

说明：

- 参数个数必须为 2，`szKey` 必须为非空字符串。
- 从 `m_ItemDataMgr` 取到对应的 Lua ref 后，会 `lua_rawgeti` 把 `ItemData` 推到栈顶并返回 1 个值；找不到则不返回值。

* <h4 id="LuaFrame_GetItemDataKey">GetItemDataKey</h4>

 > (`string` szKey) WndFrame:GetItemDataKey(`userdata` ItemData)

说明：

- 参数个数必须为 2。
- 第 2 个参数要求为 `ItemData` table（实现中用 `lua_istable` 校验，并取出其 CData）。
- 返回底层 `ItemData` 的名字（`pItemData->wszName` 宽字串转多字节）。

* <h4 id="LuaFrame_SwitchLayer">SwitchLayer</h4>

 > (`void`) WndFrame:SwitchLayer(`string` szLayer)

说明：

- 参数个数必须为 2，`szLayer` 必须为非空字符串。
- 通过 `KWndStation::GetLayerIndexByName(szLayer)` 得到层索引后，调用 `Station.AddFrame(pWnd, nLayer)`。

* <h4 id="LuaFrame_IsVisibleInCurrentShowMode">IsVisibleInCurrentShowMode</h4>

 > (`bool` bVisible) WndFrame:IsVisibleInCurrentShowMode()

说明：

- 只接受 `self` 一个参数。
- 用当前 show mode（`Station.GetCurrentShowMode()`）调用 `IsVisibleInShowMode(...)` 并返回结果。

* <h4 id="LuaFrame_IsVisibleInShowMode">IsVisibleInShowMode</h4>

 > (`bool` bVisible) WndFrame:IsVisibleInShowMode(`string` szMode)

说明：

- 参数个数必须为 2。
- `szMode` 必须为非空字符串。
- 返回底层 `IsVisibleInShowMode(szMode)` 的结果（Lua boolean）。

* <h4 id="LuaFrame_AddShowModeByName">AddShowModeByName</h4>

 > (`bool` bOk) WndFrame:AddShowModeByName(`string` szMode)

说明：

- 参数个数必须为 2。
- 返回 boolean（是否成功添加）。

* <h4 id="LuaFrame_RemoveShowModeByName">RemoveShowModeByName</h4>

 > (`bool` bOk) WndFrame:RemoveShowModeByName(`string` szMode)

说明：

- 参数个数必须为 2。
- 返回 boolean（是否成功移除）。

* <h4 id="LuaFrame_GetViewLevel">GetViewLevel</h4>

 > (`number` nLevel) WndFrame:GetViewLevel()

说明：

- 只接受 `self` 一个参数。
- 返回底层 `GetViewLevel()`。

* <h4 id="LuaFrame_IsViewMutex">IsViewMutex</h4>

 > (`bool` bMutex) WndFrame:IsViewMutex()

说明：

- 只接受 `self` 一个参数。
- 返回底层 `IsViewMutex()` 的结果（Lua boolean）。

* <h4 id="LuaFrame_GetViewMutexKey">GetViewMutexKey</h4>

 > (`string` szKey) WndFrame:GetViewMutexKey()

说明：

- 只接受 `self` 一个参数。
- 底层返回 `NULL` 时会在 Lua 层转换为 `""`（空字符串）。

* <h4 id="LuaFrame_IsAddBackGround">IsAddBackGround</h4>

 > (`bool` bBg) WndFrame:IsAddBackGround()

说明：

- 只接受 `self` 一个参数。
- 返回底层 `IsBackGround()` 的结果（Lua boolean）。
