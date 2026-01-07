# WndWindow

Notes:

- Position/size-related APIs are affected by `UIScale`:
  - `Set*` methods usually multiply Lua inputs by `Station.GetUIScale()` before applying.
  - `Get*` methods usually divide internal values by `UIScale` before returning.
- `SetPoint` anchor parsing applies `UIScale` scaling to `x/y` and `offsetX/offsetY`.

Each API below includes a short behavior note based on the C++ Lua bindings.

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

Sets the window relative X position. Lua input is multiplied by `UIScale` before applying.

 > (`void`) WndWindow:SetRelX(`number` x)

* <h4 id="LuaWindow_SetRelY">SetRelY</h4>

Sets the window relative Y position. Lua input is multiplied by `UIScale` before applying.

 > (`void`) WndWindow:SetRelY(`number` y)

* <h4 id="LuaWindow_GetRelX">GetRelX</h4>

Gets the window relative X position. Internal value is divided by `UIScale` before returning.

 > (`number` x) WndWindow:GetRelX()

* <h4 id="LuaWindow_GetRelY">GetRelY</h4>

Gets the window relative Y position. Internal value is divided by `UIScale` before returning.

 > (`number` y) WndWindow:GetRelY()

* <h4 id="LuaWindow_SetAbsX">SetAbsX</h4>

Sets the window absolute X position. Lua input is multiplied by `UIScale` before applying.

 > (`void`) WndWindow:SetAbsX(`number` x)

* <h4 id="LuaWindow_SetAbsY">SetAbsY</h4>

Sets the window absolute Y position. Lua input is multiplied by `UIScale` before applying.

 > (`void`) WndWindow:SetAbsY(`number` y)

* <h4 id="LuaWindow_GetAbsX">GetAbsX</h4>

Gets the window absolute X position. Internal value is divided by `UIScale` before returning.

 > (`number` x) WndWindow:GetAbsX()

* <h4 id="LuaWindow_GetAbsY">GetAbsY</h4>

Gets the window absolute Y position. Internal value is divided by `UIScale` before returning.

 > (`number` y) WndWindow:GetAbsY()

* <h4 id="LuaWindow_SetW">SetW</h4>

Sets the window width. Lua input is multiplied by `UIScale` before applying.

 > (`void`) WndWindow:SetW(`number` w)

* <h4 id="LuaWindow_SetH">SetH</h4>

Sets the window height. Lua input is multiplied by `UIScale` before applying.

 > (`void`) WndWindow:SetH(`number` h)

* <h4 id="LuaWindow_GetW">GetW</h4>

Gets the window width. Internal value is divided by `UIScale` before returning.

 > (`number` w) WndWindow:GetW()

* <h4 id="LuaWindow_GetH">GetH</h4>

Gets the window height. Internal value is divided by `UIScale` before returning.

 > (`number` h) WndWindow:GetH()

* <h4 id="LuaWindow_GetRelPos">GetRelPos</h4>

Gets the window relative position. Internal values are divided by `UIScale` before returning.

 > (`number` x, `number` y) WndWindow:GetRelPos()

* <h4 id="LuaWindow_GetAbsPos">GetAbsPos</h4>

Gets the window absolute position. Internal values are divided by `UIScale` before returning.

 > (`number` x, `number` y) WndWindow:GetAbsPos()

* <h4 id="LuaWindow_GetSize">GetSize</h4>

Gets the window size. Internal values are divided by `UIScale` before returning.

 > (`number` w, `number` h) WndWindow:GetSize()

* <h4 id="LuaWindow_SetSize">SetSize</h4>

Sets the window size. Lua inputs are multiplied by `UIScale` before applying.

 > (`void`) WndWindow:SetSize(`number` w, `number` h)

* <h4 id="LuaWindow_IsVisible">IsVisible</h4>

Returns whether the window is currently visible.

 > (`bool` bVisible) WndWindow:IsVisible()

* <h4 id="LuaWindow_IsDisable">IsDisable</h4>

Returns whether the window is currently disabled.

 > (`bool` bDisable) WndWindow:IsDisable()

* <h4 id="LuaWindow_SetRelPos">SetRelPos</h4>

Sets the window relative position. Lua inputs are multiplied by `UIScale` before applying.

 > (`void`) WndWindow:SetRelPos(`number` x, `number` y)

* <h4 id="LuaWindow_SetAbsPos">SetAbsPos</h4>

Sets the window absolute position. Lua inputs are multiplied by `UIScale` before applying.

 > (`void`) WndWindow:SetAbsPos(`number` x, `number` y)

* <h4 id="LuaWindow_SetCursorAbove">SetCursorAbove</h4>

Marks the cursor as being above this window (affects hover/response logic).

 > (`void`) WndWindow:SetCursorAbove()

* <h4 id="LuaWindow_Enable">Enable</h4>

Enables or disables the window.

 > (`void`) WndWindow:Enable(`bool|number` bEnable)

* <h4 id="LuaWindow_SetVisible">SetVisible</h4>

Shows or hides the window.

 > (`void`) WndWindow:SetVisible(`bool` bVisible)

Notes:

- Internally calls `Show()` / `Hide()`.

* <h4 id="LuaWindow_Show">Show</h4>

Shows the window. With an optional boolean, `false` will route to `Hide()`.

 > (`void`) WndWindow:Show()

 > (`void`) WndWindow:Show(`bool|number` bShow)

* <h4 id="LuaWindow_Hide">Hide</h4>

Hides the window. With an optional boolean, `false` will route to `Show()`.

 > (`void`) WndWindow:Hide()

 > (`void`) WndWindow:Hide(`bool|number` bHide)

* <h4 id="LuaWindow_ToggleVisible">ToggleVisible</h4>

Toggles the window visibility.

 > (`void`) WndWindow:ToggleVisible()

* <h4 id="LuaWindow_BringToTop">BringToTop</h4>

Brings the window to the top within its sibling order.

 > (`void`) WndWindow:BringToTop()

* <h4 id="LuaWindow_Scale">Scale</h4>

Sets the window scale. `fXScale` and `fYScale` must be greater than 0.

 > (`void`) WndWindow:Scale(`number` fXScale, `number` fYScale)

Notes:

- `fXScale`/`fYScale` must be greater than 0.

* <h4 id="LuaWindow_CreateItemHandle">CreateItemHandle</h4>

Creates and binds an `ItemHandle` to this window.

 > (`void`) WndWindow:CreateItemHandle(`string` szEncoded)

 > (`void`) WndWindow:CreateItemHandle(`string` szIniFile, `string` szSection[, `string` szNewName])

Notes:

- Creates and binds an `ItemHandle` to this window.

* <h4 id="LuaWindow_ReleaseItemHandle">ReleaseItemHandle</h4>

Releases the `ItemHandle` currently bound to this window.

 > (`void`) WndWindow:ReleaseItemHandle()

* <h4 id="LuaWindow_Lookup">Lookup</h4>

Finds a child window (and optionally an item under that child's `ItemHandle`) by tree path.

 > (`WndWindow` Wnd) WndWindow:Lookup(`string` szTreePath)

 > (`KItem*` Item) WndWindow:Lookup(`string` szTreePath, `string` szItemTreePath)

Notes:

- When the 2nd parameter `szItemTreePath` is provided: first `Lookup` the child window, then look up the item by `ItemTreePath` from that window's `ItemHandle`.
- When `szItemTreePath == ""`: returns this window's `ItemHandle` (as an `ItemNull` lookup).

* <h4 id="LuaWindow_GetName">GetName</h4>

Gets the window name string.

 > (`string` szName) WndWindow:GetName()

* <h4 id="LuaWindow_SetName">SetName</h4>

Sets the window name string.

 > (`void`) WndWindow:SetName(`string` szName)

* <h4 id="LuaWindow_GetPrev">GetPrev</h4>

Gets the previous sibling window; returns nothing if not found.

 > (`WndWindow` Prev) WndWindow:GetPrev()

* <h4 id="LuaWindow_GetNext">GetNext</h4>

Gets the next sibling window; returns nothing if not found.

 > (`WndWindow` Next) WndWindow:GetNext()

* <h4 id="LuaWindow_GetParent">GetParent</h4>

Gets the parent window; returns nothing if not found.

 > (`WndWindow` Parent) WndWindow:GetParent()

* <h4 id="LuaWindow_GetRoot">GetRoot</h4>

Walks up the parent chain until a `WndFrame` is found.

 > (`WndFrame` RootFrame) WndWindow:GetRoot()

Notes:

- Walks up the parent chain until a `WndFrame` is found.

* <h4 id="LuaWindow_GetFirstChild">GetFirstChild</h4>

Gets the first child window; returns nothing if not found.

 > (`WndWindow` Child) WndWindow:GetFirstChild()

* <h4 id="LuaWindow_CorrectPos">CorrectPos</h4>

Runs position correction logic. Any `x/y/w/h` inputs are scaled by `UIScale` before use.

 > (`void`) WndWindow:CorrectPos()

 > (`void`) WndWindow:CorrectPos(`string` szAnotherWnd)

 > (`void`) WndWindow:CorrectPos(`number` x, `number` y)

 > (`void`) WndWindow:CorrectPos(`string` szAnotherWnd, `number` nType)

 > (`void`) WndWindow:CorrectPos(`number` x, `number` y, `number` nType)

 > (`void`) WndWindow:CorrectPos(`number` x, `number` y, `number` w, `number` h[, `number` nType])

Notes:

- `x/y/w/h` are scaled by `UIScale` before being used in the calculation.

* <h4 id="LuaWindow_IsDummyWnd">IsDummyWnd</h4>

Returns whether the window has `WND_S_DUMMY_WND` set.

 > (`bool` bDummy) WndWindow:IsDummyWnd()

* <h4 id="LuaWindow_SetDummyWnd">SetDummyWnd</h4>

Enables/disables the `WND_S_DUMMY_WND` style.

 > (`void`) WndWindow:SetDummyWnd(`bool|number` bDummy)

* <h4 id="LuaWindow_IsMoveable">IsMoveable</h4>

Returns whether the window has the moveable style.

 > (`bool` bMoveable) WndWindow:IsMoveable()

* <h4 id="LuaWindow_SetMoveable">SetMoveable</h4>

Enables/disables the moveable style.

 > (`void`) WndWindow:SetMoveable(`bool|number` bMoveable)

* <h4 id="LuaWindow_IsMousePenetrable">IsMousePenetrable</h4>

Returns whether the window is mouse-penetrable.

 > (`bool` bPenetrable) WndWindow:IsMousePenetrable()

* <h4 id="LuaWindow_SetMousePenetrable">SetMousePenetrable</h4>

Enables/disables the mouse-penetrable style.

 > (`void`) WndWindow:SetMousePenetrable(`bool|number` bPenetrable)

* <h4 id="LuaWindow_SetAlpha">SetAlpha</h4>

Sets the window alpha value.

 > (`void`) WndWindow:SetAlpha(`number` nAlpha)

* <h4 id="LuaWindow_SetSelfAlpha">SetSelfAlpha</h4>

Sets the window self alpha value (exact effect depends on the underlying UI implementation).

 > (`void`) WndWindow:SetSelfAlpha(`number` nAlpha)

* <h4 id="LuaWindow_GetAlpha">GetAlpha</h4>

Gets the window alpha value.

 > (`number` nAlpha) WndWindow:GetAlpha()

* <h4 id="LuaWindow_GetType">GetType</h4>

Gets the window type string.

 > (`string` szWndType) WndWindow:GetType()

* <h4 id="LuaWindow_ChangeRelation">ChangeRelation</h4>

Changes the window relation/ordering relative to another window.

 > (`void`) WndWindow:ChangeRelation(`WndWindow|table|string` relation[, `bool|number` bBehind = true[, `bool|number` bChild = false]])

Notes:

- `relation` can be a `WndWindow` userdata (passed in as a table) or a window path string.

* <h4 id="LuaWindow_RebuildEventArray">RebuildEventArray</h4>

Rebuilds the event array by calling the underlying `UpdateEvent()`.

 > (`void`) WndWindow:RebuildEventArray()

* <h4 id="LuaWindow_GetIndex">GetIndex</h4>

Gets the window index.

 > (`number` nIndex) WndWindow:GetIndex()

* <h4 id="LuaWindow_SetIndex">SetIndex</h4>

Sets the window index.

 > (`void`) WndWindow:SetIndex(`number` nIndex)

* <h4 id="LuaWindow_GetChildCount">GetChildCount</h4>

Gets the number of child windows.

 > (`number` nCount) WndWindow:GetChildCount()

* <h4 id="LuaWindow_SetPoint">SetPoint</h4>

Sets the position either directly (`x/y`) or by anchor parameters.

 > (`void`) WndWindow:SetPoint(`number` x, `number` y)

 > (`void`) WndWindow:SetPoint(`string` szSide, `number` x, `number` y, `string` szRelSide, `number` offsetX, `number` offsetY)

 > (`void`) WndWindow:SetPoint(`string` szSide, `number` x, `number` y, `WndWindow|ItemNull|table|string` rel, `string` szRelSide, `number` offsetX, `number` offsetY)

Notes:

- Parameter count must be `3` / `7` / `8` (including `self`).
- The anchor form calls `LuaGetUIAnchorData` and applies `UIScale` scaling to `x/y` and `offsetX/offsetY`.

* <h4 id="LuaWindow_SetAreaTestFile">SetAreaTestFile</h4>

Sets the hit-test (area test) file. When provided, the path is normalized via `FormatFilePath()`.

 > (`void`) WndWindow:SetAreaTestFile([`string` szFile])

* <h4 id="LuaWindow_Destroy">Destroy</h4>

Destroys the window (binding calls `Destroy(false)`).

 > (`void`) WndWindow:Destroy()

* <h4 id="LuaWindow_GetTreePath">GetTreePath</h4>

Gets the window tree path string.

 > (`string` szTreePath) WndWindow:GetTreePath()

* <h4 id="LuaWindow_StartMoving">StartMoving</h4>

Starts moving the window (adds it into the moving-window list).

 > (`void`) WndWindow:StartMoving()

* <h4 id="LuaWindow_EndMoving">EndMoving</h4>

Ends moving the window (removes it from the moving-window list).

 > (`void`) WndWindow:EndMoving()

* <h4 id="LuaWindow_HasTip">HasTip</h4>

Returns whether the window has a tip.

 > (`bool` bHasTip) WndWindow:HasTip()

* <h4 id="LuaWindow_IsValid">IsValid</h4>

Checks whether the userdata can be recognized as a `WndWindow`.

 > (`bool` bValid) WndWindow:IsValid()

Notes:

- Only checks whether the userdata can be recognized as `WndWindow`.

* <h4 id="LuaWindow_GetBaseType">GetBaseType</h4>

Returns the base type string (always `"Wnd"`).

 > (`string` szBaseType) WndWindow:GetBaseType()  // Always returns "Wnd"

* <h4 id="LuaWindow_GetAniParamID">GetAniParamID</h4>

Returns a `LONG_PTR` packed as userdata.

 > (`userdata` ParamID) WndWindow:GetAniParamID()

Notes:

- Returns a `LONG_PTR` userdata.

* <h4 id="LuaWindow_PtInWindow">PtInWindow</h4>

Tests whether a point is inside the window. `absX/absY` are scaled by `UIScale` before hit-testing.

 > (`bool` bIn) WndWindow:PtInWindow(`number` absX, `number` absY)

Notes:

- `absX/absY` are scaled by `UIScale` before hit-testing.

* <h4 id="LuaWindow_IsMouseIn">IsMouseIn</h4>

Returns whether the mouse is currently inside the window.

 > (`bool` bIn) WndWindow:IsMouseIn()

* <h4 id="LuaWindow_SetBasicStatus">SetBasicStatus</h4>

Sets a basic status flag. In the current binding implementation the return value is always `false`.

 > (`bool` bResult) WndWindow:SetBasicStatus(`number` nStatus, `bool` bEnable)

Notes:

- In the current implementation, return value `bResult` is always `false` (kept for compatibility).

* <h4 id="LuaWindow_SetMouseButtonStatusElement">SetMouseButtonStatusElement</h4>

Sets the UI element name used for mouse-button status.

 > (`void`) WndWindow:SetMouseButtonStatusElement(`string` szElem)

* <h4 id="LuaWindow_ClearMouseButtonStatusElement">ClearMouseButtonStatusElement</h4>

Clears the mouse-button status UI element.

 > (`void`) WndWindow:ClearMouseButtonStatusElement()

* <h4 id="LuaWindow_SetHoverElement">SetHoverElement</h4>

Sets the hover UI element and enables the hover-response style.

 > (`void`) WndWindow:SetHoverElement(`string` szElem)

* <h4 id="LuaWindow_ClearHoverElement">ClearHoverElement</h4>

Clears the hover UI element and disables the hover-response style.

 > (`void`) WndWindow:ClearHoverElement()

* <h4 id="LuaWindow_SetTweenAni">SetTweenAni</h4>

Sets both tween file and tween name.

 > (`void`) WndWindow:SetTweenAni(`string` szTweenPath, `string` szTweenName)

* <h4 id="LuaWindow_GetTweenFile">GetTweenFile</h4>

Gets the tween file path; may return an empty string.

 > (`string` szTweenPath) WndWindow:GetTweenFile()

* <h4 id="LuaWindow_SetTweenFile">SetTweenFile</h4>

Sets the tween file path.

 > (`void`) WndWindow:SetTweenFile(`string` szTweenPath)

* <h4 id="LuaWindow_GetTweenName">GetTweenName</h4>

Gets the tween name; may return an empty string.

 > (`string` szTweenName) WndWindow:GetTweenName()

* <h4 id="LuaWindow_SetTweenName">SetTweenName</h4>

Sets the tween name.

 > (`void`) WndWindow:SetTweenName(`string` szTweenName)

* <h4 id="LuaWindow_GetDefaultAnchor">GetDefaultAnchor</h4>

Returns the default anchor table used by the UI system.

 > (`table` tAnchor) WndWindow:GetDefaultAnchor()

`tAnchor` structure:

- `path`: anchor target path string
- `s`: source edge (`string`)
- `r`: relative edge (`string`)
- `x`: x offset (`int`)
- `y`: y offset (`int`)
