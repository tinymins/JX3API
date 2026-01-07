[English](./WndWindow.md) | 中文

# WndWindow

说明：

- 位置/尺寸相关 API 会受到 `UIScale` 影响：
  - `Set*` 通常会先将 Lua 输入乘以 `Station.GetUIScale()` 再应用。
  - `Get*` 通常会在返回前将内部值除以 `UIScale`。
- `SetPoint` 的锚点解析会对 `x/y` 与 `offsetX/offsetY` 应用 `UIScale` 缩放。

[`SetRelX`](#LuaWindow_SetRelX)
[`SetRelY`](#LuaWindow_SetRelY)
[`GetRelX`](#LuaWindow_GetRelX)
[`GetRelY`](#LuaWindow_GetRelY)
[`SetAbsX`](#LuaWindow_SetAbsX)
[`SetAbsY`](#LuaWindow_SetAbsY)
[`GetAbsX`](#LuaWindow_GetAbsX)
[`GetAbsY`](#LuaWindow_GetAbsY)
[`SetW`](#LuaWindow_SetW)
[`SetH`](#LuaWindow_SetH)
[`GetW`](#LuaWindow_GetW)
[`GetH`](#LuaWindow_GetH)
[`GetRelPos`](#LuaWindow_GetRelPos)
[`GetAbsPos`](#LuaWindow_GetAbsPos)
[`GetSize`](#LuaWindow_GetSize)
[`SetSize`](#LuaWindow_SetSize)
[`IsVisible`](#LuaWindow_IsVisible)
[`IsDisable`](#LuaWindow_IsDisable)
[`SetRelPos`](#LuaWindow_SetRelPos)
[`SetAbsPos`](#LuaWindow_SetAbsPos)
[`SetCursorAbove`](#LuaWindow_SetCursorAbove)
[`Enable`](#LuaWindow_Enable)
[`SetVisible`](#LuaWindow_SetVisible)
[`Show`](#LuaWindow_Show)
[`Hide`](#LuaWindow_Hide)
[`ToggleVisible`](#LuaWindow_ToggleVisible)
[`BringToTop`](#LuaWindow_BringToTop)
[`Scale`](#LuaWindow_Scale)
[`CreateItemHandle`](#LuaWindow_CreateItemHandle)
[`ReleaseItemHandle`](#LuaWindow_ReleaseItemHandle)
[`Lookup`](#LuaWindow_Lookup)
[`GetName`](#LuaWindow_GetName)
[`SetName`](#LuaWindow_SetName)
[`GetPrev`](#LuaWindow_GetPrev)
[`GetNext`](#LuaWindow_GetNext)
[`GetParent`](#LuaWindow_GetParent)
[`GetRoot`](#LuaWindow_GetRoot)
[`GetFirstChild`](#LuaWindow_GetFirstChild)
[`CorrectPos`](#LuaWindow_CorrectPos)
[`IsDummyWnd`](#LuaWindow_IsDummyWnd)
[`SetDummyWnd`](#LuaWindow_SetDummyWnd)
[`IsMoveable`](#LuaWindow_IsMoveable)
[`SetMoveable`](#LuaWindow_SetMoveable)
[`IsMousePenetrable`](#LuaWindow_IsMousePenetrable)
[`SetMousePenetrable`](#LuaWindow_SetMousePenetrable)
[`SetAlpha`](#LuaWindow_SetAlpha)
[`SetSelfAlpha`](#LuaWindow_SetSelfAlpha)
[`GetAlpha`](#LuaWindow_GetAlpha)
[`GetType`](#LuaWindow_GetType)
[`ChangeRelation`](#LuaWindow_ChangeRelation)
[`RebuildEventArray`](#LuaWindow_RebuildEventArray)
[`GetIndex`](#LuaWindow_GetIndex)
[`SetIndex`](#LuaWindow_SetIndex)
[`GetChildCount`](#LuaWindow_GetChildCount)
[`SetPoint`](#LuaWindow_SetPoint)
[`SetAreaTestFile`](#LuaWindow_SetAreaTestFile)
[`Destroy`](#LuaWindow_Destroy)
[`GetTreePath`](#LuaWindow_GetTreePath)
[`StartMoving`](#LuaWindow_StartMoving)
[`EndMoving`](#LuaWindow_EndMoving)
[`HasTip`](#LuaWindow_HasTip)
[`IsValid`](#LuaWindow_IsValid)
[`GetBaseType`](#LuaWindow_GetBaseType)
[`GetAniParamID`](#LuaWindow_GetAniParamID)
[`PtInWindow`](#LuaWindow_PtInWindow)
[`IsMouseIn`](#LuaWindow_IsMouseIn)
[`SetBasicStatus`](#LuaWindow_SetBasicStatus)
[`SetMouseButtonStatusElement`](#LuaWindow_SetMouseButtonStatusElement)
[`ClearMouseButtonStatusElement`](#LuaWindow_ClearMouseButtonStatusElement)
[`SetHoverElement`](#LuaWindow_SetHoverElement)
[`ClearHoverElement`](#LuaWindow_ClearHoverElement)
[`SetTweenAni`](#LuaWindow_SetTweenAni)
[`GetTweenFile`](#LuaWindow_GetTweenFile)
[`SetTweenFile`](#LuaWindow_SetTweenFile)
[`GetTweenName`](#LuaWindow_GetTweenName)
[`SetTweenName`](#LuaWindow_SetTweenName)
[`GetDefaultAnchor`](#LuaWindow_GetDefaultAnchor)

* <h4 id="LuaWindow_SetRelX">SetRelX</h4>

设置窗口相对坐标 X（Lua 侧传入未缩放坐标，内部会先乘以 `UIScale`）。

 > (`void`) WndWindow:SetRelX(`number` x)

* <h4 id="LuaWindow_SetRelY">SetRelY</h4>

设置窗口相对坐标 Y（Lua 侧传入未缩放坐标，内部会先乘以 `UIScale`）。

 > (`void`) WndWindow:SetRelY(`number` y)

* <h4 id="LuaWindow_GetRelX">GetRelX</h4>

获取窗口相对坐标 X（返回前会除以 `UIScale`）。

 > (`number` x) WndWindow:GetRelX()

* <h4 id="LuaWindow_GetRelY">GetRelY</h4>

获取窗口相对坐标 Y（返回前会除以 `UIScale`）。

 > (`number` y) WndWindow:GetRelY()

* <h4 id="LuaWindow_SetAbsX">SetAbsX</h4>

设置窗口绝对坐标 X（Lua 侧传入未缩放坐标，内部会先乘以 `UIScale`）。

 > (`void`) WndWindow:SetAbsX(`number` x)

* <h4 id="LuaWindow_SetAbsY">SetAbsY</h4>

设置窗口绝对坐标 Y（Lua 侧传入未缩放坐标，内部会先乘以 `UIScale`）。

 > (`void`) WndWindow:SetAbsY(`number` y)

* <h4 id="LuaWindow_GetAbsX">GetAbsX</h4>

获取窗口绝对坐标 X（返回前会除以 `UIScale`）。

 > (`number` x) WndWindow:GetAbsX()

* <h4 id="LuaWindow_GetAbsY">GetAbsY</h4>

获取窗口绝对坐标 Y（返回前会除以 `UIScale`）。

 > (`number` y) WndWindow:GetAbsY()

* <h4 id="LuaWindow_SetW">SetW</h4>

设置窗口宽度（Lua 侧传入未缩放值，内部会先乘以 `UIScale`）。

 > (`void`) WndWindow:SetW(`number` w)

* <h4 id="LuaWindow_SetH">SetH</h4>

设置窗口高度（Lua 侧传入未缩放值，内部会先乘以 `UIScale`）。

 > (`void`) WndWindow:SetH(`number` h)

* <h4 id="LuaWindow_GetW">GetW</h4>

获取窗口宽度（返回前会除以 `UIScale`）。

 > (`number` w) WndWindow:GetW()

* <h4 id="LuaWindow_GetH">GetH</h4>

获取窗口高度（返回前会除以 `UIScale`）。

 > (`number` h) WndWindow:GetH()

* <h4 id="LuaWindow_GetRelPos">GetRelPos</h4>

获取窗口相对坐标（返回前会除以 `UIScale`）。

 > (`number` x, `number` y) WndWindow:GetRelPos()

* <h4 id="LuaWindow_GetAbsPos">GetAbsPos</h4>

获取窗口绝对坐标（返回前会除以 `UIScale`）。

 > (`number` x, `number` y) WndWindow:GetAbsPos()

* <h4 id="LuaWindow_GetSize">GetSize</h4>

获取窗口尺寸（返回前会除以 `UIScale`）。

 > (`number` w, `number` h) WndWindow:GetSize()

* <h4 id="LuaWindow_SetSize">SetSize</h4>

设置窗口尺寸（Lua 侧传入未缩放值，内部会先乘以 `UIScale`）。

 > (`void`) WndWindow:SetSize(`number` w, `number` h)

* <h4 id="LuaWindow_IsVisible">IsVisible</h4>

检查窗口是否可见。

 > (`bool` bVisible) WndWindow:IsVisible()

* <h4 id="LuaWindow_IsDisable">IsDisable</h4>

检查窗口是否处于 Disable 状态。

 > (`bool` bDisable) WndWindow:IsDisable()

* <h4 id="LuaWindow_SetRelPos">SetRelPos</h4>

设置窗口相对坐标（Lua 侧传入未缩放坐标，内部会先乘以 `UIScale`）。

 > (`void`) WndWindow:SetRelPos(`number` x, `number` y)

* <h4 id="LuaWindow_SetAbsPos">SetAbsPos</h4>

设置窗口绝对坐标（Lua 侧传入未缩放坐标，内部会先乘以 `UIScale`）。

 > (`void`) WndWindow:SetAbsPos(`number` x, `number` y)

* <h4 id="LuaWindow_SetCursorAbove">SetCursorAbove</h4>

将鼠标指针（cursor）标记为位于该窗口上方。

 > (`void`) WndWindow:SetCursorAbove()

* <h4 id="LuaWindow_Enable">Enable</h4>

设置窗口是否启用。

`bEnable` 支持传入 `bool` 或 `number`（Lua 绑定会按类型分支转换为整数布尔值）。

 > (`void`) WndWindow:Enable(`bool|number` bEnable)

* <h4 id="LuaWindow_SetVisible">SetVisible</h4>

 > (`void`) WndWindow:SetVisible(`bool` bVisible)

说明：

- 内部会调用 `Show()` / `Hide()`。

* <h4 id="LuaWindow_Show">Show</h4>

显示窗口。

实现支持可选参数 `bShow`：传入 false 时会转为调用 `Hide()`。

 > (`void`) WndWindow:Show()

 > (`void`) WndWindow:Show(`bool|number` bShow)

* <h4 id="LuaWindow_Hide">Hide</h4>

隐藏窗口。

实现支持可选参数 `bHide`：传入 false 时会转为调用 `Show()`。

 > (`void`) WndWindow:Hide()

 > (`void`) WndWindow:Hide(`bool|number` bHide)

* <h4 id="LuaWindow_ToggleVisible">ToggleVisible</h4>

在显示/隐藏之间切换。

 > (`void`) WndWindow:ToggleVisible()

* <h4 id="LuaWindow_BringToTop">BringToTop</h4>

将窗口置顶（提升到同层级最前）。

 > (`void`) WndWindow:BringToTop()

* <h4 id="LuaWindow_Scale">Scale</h4>

 > (`void`) WndWindow:Scale(`number` fXScale, `number` fYScale)

说明：

- `fXScale`/`fYScale` 必须大于 0。

* <h4 id="LuaWindow_CreateItemHandle">CreateItemHandle</h4>

 > (`void`) WndWindow:CreateItemHandle(`string` szEncoded)

 > (`void`) WndWindow:CreateItemHandle(`string` szIniFile, `string` szSection[, `string` szNewName])

说明：

- 创建一个 `ItemHandle` 并绑定到该窗口。

* <h4 id="LuaWindow_ReleaseItemHandle">ReleaseItemHandle</h4>

释放当前窗口绑定的 `ItemHandle`。

 > (`void`) WndWindow:ReleaseItemHandle()

* <h4 id="LuaWindow_Lookup">Lookup</h4>

 > (`WndWindow` Wnd) WndWindow:Lookup(`string` szTreePath)

 > (`KItem*` Item) WndWindow:Lookup(`string` szTreePath, `string` szItemTreePath)

说明：

- 当提供第 2 个参数 `szItemTreePath` 时：先 `Lookup` 子窗口，再从该窗口的 `ItemHandle` 里按 `ItemTreePath` 查找 item。
- 当 `szItemTreePath == ""` 时：返回该窗口的 `ItemHandle`（以 `ItemNull` 的 lookup 形式返回）。

* <h4 id="LuaWindow_GetName">GetName</h4>

获取窗口名称。

 > (`string` szName) WndWindow:GetName()

* <h4 id="LuaWindow_SetName">SetName</h4>

设置窗口名称。

 > (`void`) WndWindow:SetName(`string` szName)

* <h4 id="LuaWindow_GetPrev">GetPrev</h4>

获取上一个兄弟窗口；若不存在则不返回值。

 > (`WndWindow` Prev) WndWindow:GetPrev()

* <h4 id="LuaWindow_GetNext">GetNext</h4>

获取下一个兄弟窗口；若不存在则不返回值。

 > (`WndWindow` Next) WndWindow:GetNext()

* <h4 id="LuaWindow_GetParent">GetParent</h4>

获取父窗口；若不存在则不返回值。

 > (`WndWindow` Parent) WndWindow:GetParent()

* <h4 id="LuaWindow_GetRoot">GetRoot</h4>

 > (`WndFrame` RootFrame) WndWindow:GetRoot()

说明：

- 沿父链向上遍历，直到找到 `WndFrame`。

* <h4 id="LuaWindow_GetFirstChild">GetFirstChild</h4>

获取第一个子窗口；若不存在则不返回值。

 > (`WndWindow` Child) WndWindow:GetFirstChild()

* <h4 id="LuaWindow_CorrectPos">CorrectPos</h4>

 > (`void`) WndWindow:CorrectPos()

 > (`void`) WndWindow:CorrectPos(`string` szAnotherWnd)

 > (`void`) WndWindow:CorrectPos(`number` x, `number` y)

 > (`void`) WndWindow:CorrectPos(`string` szAnotherWnd, `number` nType)

 > (`void`) WndWindow:CorrectPos(`number` x, `number` y, `number` nType)

 > (`void`) WndWindow:CorrectPos(`number` x, `number` y, `number` w, `number` h[, `number` nType])

说明：

- `x/y/w/h` 在用于计算前会按 `UIScale` 缩放。

* <h4 id="LuaWindow_IsDummyWnd">IsDummyWnd</h4>

检查窗口是否设置了 `WND_S_DUMMY_WND` 样式。

 > (`bool` bDummy) WndWindow:IsDummyWnd()

* <h4 id="LuaWindow_SetDummyWnd">SetDummyWnd</h4>

设置/取消 `WND_S_DUMMY_WND` 样式。

 > (`void`) WndWindow:SetDummyWnd(`bool|number` bDummy)

* <h4 id="LuaWindow_IsMoveable">IsMoveable</h4>

检查窗口是否可移动（`WND_S_MOVEABLE`）。

 > (`bool` bMoveable) WndWindow:IsMoveable()

* <h4 id="LuaWindow_SetMoveable">SetMoveable</h4>

设置/取消窗口可移动样式（`WND_S_MOVEABLE`）。

 > (`void`) WndWindow:SetMoveable(`bool|number` bMoveable)

* <h4 id="LuaWindow_IsMousePenetrable">IsMousePenetrable</h4>

检查窗口是否鼠标穿透（`WND_S_MOUSE_PENETRABLE`）。

 > (`bool` bPenetrable) WndWindow:IsMousePenetrable()

* <h4 id="LuaWindow_SetMousePenetrable">SetMousePenetrable</h4>

设置/取消鼠标穿透样式（`WND_S_MOUSE_PENETRABLE`）。

 > (`void`) WndWindow:SetMousePenetrable(`bool|number` bPenetrable)

* <h4 id="LuaWindow_SetAlpha">SetAlpha</h4>

设置窗口 alpha（透明度）。

 > (`void`) WndWindow:SetAlpha(`number` nAlpha)

* <h4 id="LuaWindow_SetSelfAlpha">SetSelfAlpha</h4>

设置窗口自身 alpha（不一定影响子窗口，取决于底层实现）。

 > (`void`) WndWindow:SetSelfAlpha(`number` nAlpha)

* <h4 id="LuaWindow_GetAlpha">GetAlpha</h4>

获取窗口 alpha（透明度）。

 > (`number` nAlpha) WndWindow:GetAlpha()

* <h4 id="LuaWindow_GetType">GetType</h4>

获取窗口类型字符串（底层 `GetWndType()` 返回值）。

 > (`string` szWndType) WndWindow:GetType()

* <h4 id="LuaWindow_ChangeRelation">ChangeRelation</h4>

 > (`void`) WndWindow:ChangeRelation(`WndWindow|table|string` relation[, `bool|number` bBehind = true[, `bool|number` bChild = false]])

说明：

- `relation` 可以是 `WndWindow` userdata（以 table 形式传入），也可以是窗口路径字符串。

* <h4 id="LuaWindow_RebuildEventArray">RebuildEventArray</h4>

重新构建/更新窗口的事件数组（内部调用 `UpdateEvent()`）。

 > (`void`) WndWindow:RebuildEventArray()

* <h4 id="LuaWindow_GetIndex">GetIndex</h4>

获取窗口 index。

 > (`number` nIndex) WndWindow:GetIndex()

* <h4 id="LuaWindow_SetIndex">SetIndex</h4>

设置窗口 index；失败会报错。

 > (`void`) WndWindow:SetIndex(`number` nIndex)

* <h4 id="LuaWindow_GetChildCount">GetChildCount</h4>

获取子窗口数量。

 > (`number` nCount) WndWindow:GetChildCount()

* <h4 id="LuaWindow_SetPoint">SetPoint</h4>

设置窗口位置：既支持直接传入 `x/y`，也支持锚点（anchor）形式。

 > (`void`) WndWindow:SetPoint(`number` x, `number` y)

 > (`void`) WndWindow:SetPoint(`string` szSide, `number` x, `number` y, `string` szRelSide, `number` offsetX, `number` offsetY)

 > (`void`) WndWindow:SetPoint(`string` szSide, `number` x, `number` y, `WndWindow|ItemNull|table|string` rel, `string` szRelSide, `number` offsetX, `number` offsetY)

说明：

- 参数个数必须为 `3` / `7` / `8`（包含 `self`）。
- 锚点形式会调用 `LuaGetUIAnchorData`，并对 `x/y` 与 `offsetX/offsetY` 应用 `UIScale` 缩放。

* <h4 id="LuaWindow_SetAreaTestFile">SetAreaTestFile</h4>

设置命中测试（area test）文件。

若传入 `szFile`，内部会先经过 `FormatFilePath()`。

 > (`void`) WndWindow:SetAreaTestFile([`string` szFile])

* <h4 id="LuaWindow_Destroy">Destroy</h4>

销毁窗口（内部调用 `Destroy(false)`）。

 > (`void`) WndWindow:Destroy()

* <h4 id="LuaWindow_GetTreePath">GetTreePath</h4>

获取窗口在 UI 树中的路径字符串。

 > (`string` szTreePath) WndWindow:GetTreePath()

* <h4 id="LuaWindow_StartMoving">StartMoving</h4>

开始移动窗口（加入 MovingWindow 列表）。

 > (`void`) WndWindow:StartMoving()

* <h4 id="LuaWindow_EndMoving">EndMoving</h4>

结束移动窗口（从 MovingWindow 列表移除）。

 > (`void`) WndWindow:EndMoving()

* <h4 id="LuaWindow_HasTip">HasTip</h4>

检查窗口是否存在 tip。

 > (`bool` bHasTip) WndWindow:HasTip()

* <h4 id="LuaWindow_IsValid">IsValid</h4>

 > (`bool` bValid) WndWindow:IsValid()

说明：

- 仅检查该 userdata 是否能被识别为 `WndWindow`。

* <h4 id="LuaWindow_GetBaseType">GetBaseType</h4>

获取基础类型字符串。

 > (`string` szBaseType) WndWindow:GetBaseType()  // 永远返回 "Wnd"

* <h4 id="LuaWindow_GetAniParamID">GetAniParamID</h4>

 > (`userdata` ParamID) WndWindow:GetAniParamID()

说明：

- 返回一个 `LONG_PTR` userdata。

* <h4 id="LuaWindow_PtInWindow">PtInWindow</h4>

判断点是否在窗口范围内。

 > (`bool` bIn) WndWindow:PtInWindow(`number` absX, `number` absY)

说明：

- `absX/absY` 在命中测试前会按 `UIScale` 缩放。

* <h4 id="LuaWindow_IsMouseIn">IsMouseIn</h4>

检查鼠标当前是否在窗口内。

 > (`bool` bIn) WndWindow:IsMouseIn()

* <h4 id="LuaWindow_SetBasicStatus">SetBasicStatus</h4>

 > (`bool` bResult) WndWindow:SetBasicStatus(`number` nStatus, `bool` bEnable)

说明：

- 当前实现中返回值 `bResult` 始终为 `false`（为了兼容性保留）。

* <h4 id="LuaWindow_SetMouseButtonStatusElement">SetMouseButtonStatusElement</h4>

设置鼠标按键状态对应的 UI element 名称。

 > (`void`) WndWindow:SetMouseButtonStatusElement(`string` szElem)

* <h4 id="LuaWindow_ClearMouseButtonStatusElement">ClearMouseButtonStatusElement</h4>

清空鼠标按键状态 UI element。

 > (`void`) WndWindow:ClearMouseButtonStatusElement()

* <h4 id="LuaWindow_SetHoverElement">SetHoverElement</h4>

设置 Hover UI element，并开启 `WND_S_RESPONSE_HOVER` 样式。

 > (`void`) WndWindow:SetHoverElement(`string` szElem)

* <h4 id="LuaWindow_ClearHoverElement">ClearHoverElement</h4>

清空 Hover UI element，并关闭 `WND_S_RESPONSE_HOVER` 样式。

 > (`void`) WndWindow:ClearHoverElement()

* <h4 id="LuaWindow_SetTweenAni">SetTweenAni</h4>

同时设置 Tween 文件与 Tween 名称（相当于依次调用 `SetTweenFile`/`SetTweenName`）。

 > (`void`) WndWindow:SetTweenAni(`string` szTweenPath, `string` szTweenName)

* <h4 id="LuaWindow_GetTweenFile">GetTweenFile</h4>

获取 Tween 文件路径；为空时不返回值。

 > (`string` szTweenPath) WndWindow:GetTweenFile()

* <h4 id="LuaWindow_SetTweenFile">SetTweenFile</h4>

设置 Tween 文件路径。

 > (`void`) WndWindow:SetTweenFile(`string` szTweenPath)

* <h4 id="LuaWindow_GetTweenName">GetTweenName</h4>

获取 Tween 名称；为空时不返回值。

 > (`string` szTweenName) WndWindow:GetTweenName()

* <h4 id="LuaWindow_SetTweenName">SetTweenName</h4>

设置 Tween 名称。

 > (`void`) WndWindow:SetTweenName(`string` szTweenName)

* <h4 id="LuaWindow_GetDefaultAnchor">GetDefaultAnchor</h4>

 > (`table` tAnchor) WndWindow:GetDefaultAnchor()

`tAnchor` 结构：

- `path`：锚点目标 path 字符串
- `s`：源边（`string`）
- `r`：相对边（`string`）
- `x`：x 偏移（`int`）
- `y`：y 偏移（`int`）
