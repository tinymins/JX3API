# WndWindow

Notes:

- Position/size-related APIs are affected by `UIScale`:
  - `Set*` methods usually multiply Lua inputs by `Station.GetUIScale()` before applying.
  - `Get*` methods usually divide internal values by `UIScale` before returning.
- `SetPoint` anchor parsing applies `UIScale` scaling to `x/y` and `offsetX/offsetY`.

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

 > (`void`) WndWindow:SetRelX(`number` x)

* <h4 id="LuaWindow_SetRelY">SetRelY</h4>

 > (`void`) WndWindow:SetRelY(`number` y)

* <h4 id="LuaWindow_GetRelX">GetRelX</h4>

 > (`number` x) WndWindow:GetRelX()

* <h4 id="LuaWindow_GetRelY">GetRelY</h4>

 > (`number` y) WndWindow:GetRelY()

* <h4 id="LuaWindow_SetAbsX">SetAbsX</h4>

 > (`void`) WndWindow:SetAbsX(`number` x)

* <h4 id="LuaWindow_SetAbsY">SetAbsY</h4>

 > (`void`) WndWindow:SetAbsY(`number` y)

* <h4 id="LuaWindow_GetAbsX">GetAbsX</h4>

 > (`number` x) WndWindow:GetAbsX()

* <h4 id="LuaWindow_GetAbsY">GetAbsY</h4>

 > (`number` y) WndWindow:GetAbsY()

* <h4 id="LuaWindow_SetW">SetW</h4>

 > (`void`) WndWindow:SetW(`number` w)

* <h4 id="LuaWindow_SetH">SetH</h4>

 > (`void`) WndWindow:SetH(`number` h)

* <h4 id="LuaWindow_GetW">GetW</h4>

 > (`number` w) WndWindow:GetW()

* <h4 id="LuaWindow_GetH">GetH</h4>

 > (`number` h) WndWindow:GetH()

* <h4 id="LuaWindow_GetRelPos">GetRelPos</h4>

 > (`number` x, `number` y) WndWindow:GetRelPos()

* <h4 id="LuaWindow_GetAbsPos">GetAbsPos</h4>

 > (`number` x, `number` y) WndWindow:GetAbsPos()

* <h4 id="LuaWindow_GetSize">GetSize</h4>

 > (`number` w, `number` h) WndWindow:GetSize()

* <h4 id="LuaWindow_SetSize">SetSize</h4>

 > (`void`) WndWindow:SetSize(`number` w, `number` h)

* <h4 id="LuaWindow_IsVisible">IsVisible</h4>

 > (`bool` bVisible) WndWindow:IsVisible()

* <h4 id="LuaWindow_IsDisable">IsDisable</h4>

 > (`bool` bDisable) WndWindow:IsDisable()

* <h4 id="LuaWindow_SetRelPos">SetRelPos</h4>

 > (`void`) WndWindow:SetRelPos(`number` x, `number` y)

* <h4 id="LuaWindow_SetAbsPos">SetAbsPos</h4>

 > (`void`) WndWindow:SetAbsPos(`number` x, `number` y)

* <h4 id="LuaWindow_SetCursorAbove">SetCursorAbove</h4>

 > (`void`) WndWindow:SetCursorAbove()

* <h4 id="LuaWindow_Enable">Enable</h4>

 > (`void`) WndWindow:Enable(`bool|number` bEnable)

* <h4 id="LuaWindow_SetVisible">SetVisible</h4>

 > (`void`) WndWindow:SetVisible(`bool` bVisible)

Notes:

- Internally calls `Show()` / `Hide()`.

* <h4 id="LuaWindow_Show">Show</h4>

 > (`void`) WndWindow:Show()

 > (`void`) WndWindow:Show(`bool|number` bShow)

* <h4 id="LuaWindow_Hide">Hide</h4>

 > (`void`) WndWindow:Hide()

 > (`void`) WndWindow:Hide(`bool|number` bHide)

* <h4 id="LuaWindow_ToggleVisible">ToggleVisible</h4>

 > (`void`) WndWindow:ToggleVisible()

* <h4 id="LuaWindow_BringToTop">BringToTop</h4>

 > (`void`) WndWindow:BringToTop()

* <h4 id="LuaWindow_Scale">Scale</h4>

 > (`void`) WndWindow:Scale(`number` fXScale, `number` fYScale)

Notes:

- `fXScale`/`fYScale` must be greater than 0.

* <h4 id="LuaWindow_CreateItemHandle">CreateItemHandle</h4>

 > (`void`) WndWindow:CreateItemHandle(`string` szEncoded)

 > (`void`) WndWindow:CreateItemHandle(`string` szIniFile, `string` szSection[, `string` szNewName])

Notes:

- Creates and binds an `ItemHandle` to this window.

* <h4 id="LuaWindow_ReleaseItemHandle">ReleaseItemHandle</h4>

 > (`void`) WndWindow:ReleaseItemHandle()

* <h4 id="LuaWindow_Lookup">Lookup</h4>

 > (`WndWindow` Wnd) WndWindow:Lookup(`string` szTreePath)

 > (`KItem*` Item) WndWindow:Lookup(`string` szTreePath, `string` szItemTreePath)

Notes:

- When the 2nd parameter `szItemTreePath` is provided: first `Lookup` the child window, then look up the item by `ItemTreePath` from that window's `ItemHandle`.
- When `szItemTreePath == ""`: returns this window's `ItemHandle` (as an `ItemNull` lookup).

* <h4 id="LuaWindow_GetName">GetName</h4>

 > (`string` szName) WndWindow:GetName()

* <h4 id="LuaWindow_SetName">SetName</h4>

 > (`void`) WndWindow:SetName(`string` szName)

* <h4 id="LuaWindow_GetPrev">GetPrev</h4>

 > (`WndWindow` Prev) WndWindow:GetPrev()

* <h4 id="LuaWindow_GetNext">GetNext</h4>

 > (`WndWindow` Next) WndWindow:GetNext()

* <h4 id="LuaWindow_GetParent">GetParent</h4>

 > (`WndWindow` Parent) WndWindow:GetParent()

* <h4 id="LuaWindow_GetRoot">GetRoot</h4>

 > (`WndFrame` RootFrame) WndWindow:GetRoot()

Notes:

- Walks up the parent chain until a `WndFrame` is found.

* <h4 id="LuaWindow_GetFirstChild">GetFirstChild</h4>

 > (`WndWindow` Child) WndWindow:GetFirstChild()

* <h4 id="LuaWindow_CorrectPos">CorrectPos</h4>

 > (`void`) WndWindow:CorrectPos()

 > (`void`) WndWindow:CorrectPos(`string` szAnotherWnd)

 > (`void`) WndWindow:CorrectPos(`number` x, `number` y)

 > (`void`) WndWindow:CorrectPos(`string` szAnotherWnd, `number` nType)

 > (`void`) WndWindow:CorrectPos(`number` x, `number` y, `number` nType)

 > (`void`) WndWindow:CorrectPos(`number` x, `number` y, `number` w, `number` h[, `number` nType])

Notes:

- `x/y/w/h` are scaled by `UIScale` before being used in the calculation.

* <h4 id="LuaWindow_IsDummyWnd">IsDummyWnd</h4>

 > (`bool` bDummy) WndWindow:IsDummyWnd()

* <h4 id="LuaWindow_SetDummyWnd">SetDummyWnd</h4>

 > (`void`) WndWindow:SetDummyWnd(`bool|number` bDummy)

* <h4 id="LuaWindow_IsMoveable">IsMoveable</h4>

 > (`bool` bMoveable) WndWindow:IsMoveable()

* <h4 id="LuaWindow_SetMoveable">SetMoveable</h4>

 > (`void`) WndWindow:SetMoveable(`bool|number` bMoveable)

* <h4 id="LuaWindow_IsMousePenetrable">IsMousePenetrable</h4>

 > (`bool` bPenetrable) WndWindow:IsMousePenetrable()

* <h4 id="LuaWindow_SetMousePenetrable">SetMousePenetrable</h4>

 > (`void`) WndWindow:SetMousePenetrable(`bool|number` bPenetrable)

* <h4 id="LuaWindow_SetAlpha">SetAlpha</h4>

 > (`void`) WndWindow:SetAlpha(`number` nAlpha)

* <h4 id="LuaWindow_SetSelfAlpha">SetSelfAlpha</h4>

 > (`void`) WndWindow:SetSelfAlpha(`number` nAlpha)

* <h4 id="LuaWindow_GetAlpha">GetAlpha</h4>

 > (`number` nAlpha) WndWindow:GetAlpha()

* <h4 id="LuaWindow_GetType">GetType</h4>

 > (`string` szWndType) WndWindow:GetType()

* <h4 id="LuaWindow_ChangeRelation">ChangeRelation</h4>

 > (`void`) WndWindow:ChangeRelation(`WndWindow|table|string` relation[, `bool|number` bBehind = true[, `bool|number` bChild = false]])

Notes:

- `relation` can be a `WndWindow` userdata (passed in as a table) or a window path string.

* <h4 id="LuaWindow_RebuildEventArray">RebuildEventArray</h4>

 > (`void`) WndWindow:RebuildEventArray()

* <h4 id="LuaWindow_GetIndex">GetIndex</h4>

 > (`number` nIndex) WndWindow:GetIndex()

* <h4 id="LuaWindow_SetIndex">SetIndex</h4>

 > (`void`) WndWindow:SetIndex(`number` nIndex)

* <h4 id="LuaWindow_GetChildCount">GetChildCount</h4>

 > (`number` nCount) WndWindow:GetChildCount()

* <h4 id="LuaWindow_SetPoint">SetPoint</h4>

 > (`void`) WndWindow:SetPoint(`number` x, `number` y)

 > (`void`) WndWindow:SetPoint(`...`)  // 7 or 8 parameter anchor form

Notes:

- Parameter count must be `3` / `7` / `8` (including `self`).
- The anchor form calls `LuaGetUIAnchorData` and applies `UIScale` scaling to `x/y` and `offsetX/offsetY`.

* <h4 id="LuaWindow_SetAreaTestFile">SetAreaTestFile</h4>

 > (`void`) WndWindow:SetAreaTestFile([`string` szFile])

* <h4 id="LuaWindow_Destroy">Destroy</h4>

 > (`void`) WndWindow:Destroy()

* <h4 id="LuaWindow_GetTreePath">GetTreePath</h4>

 > (`string` szTreePath) WndWindow:GetTreePath()

* <h4 id="LuaWindow_StartMoving">StartMoving</h4>

 > (`void`) WndWindow:StartMoving()

* <h4 id="LuaWindow_EndMoving">EndMoving</h4>

 > (`void`) WndWindow:EndMoving()

* <h4 id="LuaWindow_HasTip">HasTip</h4>

 > (`bool` bHasTip) WndWindow:HasTip()

* <h4 id="LuaWindow_IsValid">IsValid</h4>

 > (`bool` bValid) WndWindow:IsValid()

Notes:

- Only checks whether the userdata can be recognized as `WndWindow`.

* <h4 id="LuaWindow_GetBaseType">GetBaseType</h4>

 > (`string` szBaseType) WndWindow:GetBaseType()  // Always returns "Wnd"

* <h4 id="LuaWindow_GetAniParamID">GetAniParamID</h4>

 > (`userdata` ParamID) WndWindow:GetAniParamID()

Notes:

- Returns a `LONG_PTR` userdata.

* <h4 id="LuaWindow_PtInWindow">PtInWindow</h4>

 > (`bool` bIn) WndWindow:PtInWindow(`number` absX, `number` absY)

Notes:

- `absX/absY` are scaled by `UIScale` before hit-testing.

* <h4 id="LuaWindow_IsMouseIn">IsMouseIn</h4>

 > (`bool` bIn) WndWindow:IsMouseIn()

* <h4 id="LuaWindow_SetBasicStatus">SetBasicStatus</h4>

 > (`bool` bResult) WndWindow:SetBasicStatus(`number` nStatus, `bool` bEnable)

Notes:

- In the current implementation, return value `bResult` is always `false` (kept for compatibility).

* <h4 id="LuaWindow_SetMouseButtonStatusElement">SetMouseButtonStatusElement</h4>

 > (`void`) WndWindow:SetMouseButtonStatusElement(`string` szElem)

* <h4 id="LuaWindow_ClearMouseButtonStatusElement">ClearMouseButtonStatusElement</h4>

 > (`void`) WndWindow:ClearMouseButtonStatusElement()

* <h4 id="LuaWindow_SetHoverElement">SetHoverElement</h4>

 > (`void`) WndWindow:SetHoverElement(`string` szElem)

* <h4 id="LuaWindow_ClearHoverElement">ClearHoverElement</h4>

 > (`void`) WndWindow:ClearHoverElement()

* <h4 id="LuaWindow_SetTweenAni">SetTweenAni</h4>

 > (`void`) WndWindow:SetTweenAni(`string` szTweenPath, `string` szTweenName)

* <h4 id="LuaWindow_GetTweenFile">GetTweenFile</h4>

 > (`string` szTweenPath) WndWindow:GetTweenFile()

* <h4 id="LuaWindow_SetTweenFile">SetTweenFile</h4>

 > (`void`) WndWindow:SetTweenFile(`string` szTweenPath)

* <h4 id="LuaWindow_GetTweenName">GetTweenName</h4>

 > (`string` szTweenName) WndWindow:GetTweenName()

* <h4 id="LuaWindow_SetTweenName">SetTweenName</h4>

 > (`void`) WndWindow:SetTweenName(`string` szTweenName)

* <h4 id="LuaWindow_GetDefaultAnchor">GetDefaultAnchor</h4>

 > (`table` tAnchor) WndWindow:GetDefaultAnchor()

`tAnchor` structure:

- `path`: anchor target path string
- `s`: source edge (`string`)
- `r`: relative edge (`string`)
- `x`: x offset (`int`)
- `y`: y offset (`int`)
