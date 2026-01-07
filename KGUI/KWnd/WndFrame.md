# WndFrame

Notes:

- `WndFrame` inherits all methods from `WndWindow`; only additional methods are listed here.

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

Enables or disables dragging for the frame.

 > (`void`) WndFrame:EnableDrag(`bool|number` bEnable)

* <h4 id="LuaFrame_IsDragable">IsDragable</h4>

Returns whether the frame is dragable.

 > (`bool` bEnable) WndFrame:IsDragable()

* <h4 id="LuaFrame_EnableFollowMouse">EnableFollowMouse</h4>

Enables or disables follow-mouse behavior.

 > (`void`) WndFrame:EnableFollowMouse(`bool|number` bEnable)

* <h4 id="LuaFrame_IsFollowMouseMove">IsFollowMouseMove</h4>

Returns whether follow-mouse movement is enabled.

 > (`bool` bEnable) WndFrame:IsFollowMouseMove()

* <h4 id="LuaFrame_SetDragArea">SetDragArea</h4>

Sets the draggable area rectangle.

 > (`void`) WndFrame:SetDragArea(`number` x, `number` y, `number` w, `number` h)

* <h4 id="LuaFrame_RegisterEvent">RegisterEvent</h4>

Registers an event handler callback.

 > (`void`) WndFrame:RegisterEvent(`string` szEvent[, `function` fnCallback])

* <h4 id="LuaFrame_UnRegisterEvent">UnRegisterEvent</h4>

Unregisters an event handler (by callback reference if provided).

 > (`void`) WndFrame:UnRegisterEvent(`string` szEvent[, `function|number` ref])

* <h4 id="LuaFrame_FocusPrev">FocusPrev</h4>

Moves focus to the previous focusable element.

 > (`bool` bOk) WndFrame:FocusPrev()

* <h4 id="LuaFrame_FocusNext">FocusNext</h4>

Moves focus to the next focusable element.

 > (`bool` bOk) WndFrame:FocusNext()

* <h4 id="LuaFrame_FocusHome">FocusHome</h4>

Moves focus to the first focusable element.

 > (`bool` bOk) WndFrame:FocusHome()

* <h4 id="LuaFrame_FocusEnd">FocusEnd</h4>

Moves focus to the last focusable element.

 > (`bool` bOk) WndFrame:FocusEnd()

* <h4 id="LuaFrame_FadeIn">FadeIn</h4>

Fades in over `dwTime`.

 > (`void`) WndFrame:FadeIn(`number` dwTime)

* <h4 id="LuaFrame_FadeOut">FadeOut</h4>

Fades out over `dwTime`.

 > (`void`) WndFrame:FadeOut(`number` dwTime)

* <h4 id="LuaFrame_IsAlwaysTop">IsAlwaysTop</h4>

Returns whether the frame is always on top.

 > (`bool` bTop) WndFrame:IsAlwaysTop()

* <h4 id="LuaFrame_SetAlwaysTop">SetAlwaysTop</h4>

Enables or disables always-on-top behavior.

 > (`void`) WndFrame:SetAlwaysTop(`bool|number` bTop)

* <h4 id="LuaFrame_ShowWhenUIHide">ShowWhenUIHide</h4>

Marks the frame to show when the UI is hidden.

 > (`void`) WndFrame:ShowWhenUIHide()

* <h4 id="LuaFrame_HideWhenUIHide">HideWhenUIHide</h4>

Marks the frame to hide when the UI is hidden.

 > (`void`) WndFrame:HideWhenUIHide()

* <h4 id="LuaFrame_IsVisibleWhenUIHide">IsVisibleWhenUIHide</h4>

Returns whether the frame is visible when the UI is hidden.

 > (`bool` bVisible) WndFrame:IsVisibleWhenUIHide()

* <h4 id="LuaFrame_IsAddOn">IsAddOn</h4>

Returns whether this frame is an addon frame.

 > (`bool` bAddOn) WndFrame:IsAddOn()

* <h4 id="LuaFrame_CreateItemData">CreateItemData</h4>

Creates an item data object from an ini section.

 > (`userdata` ItemData) WndFrame:CreateItemData(`string` szIniFile, `string` szSectionName)

* <h4 id="LuaFrame_RemoveItemData">RemoveItemData</h4>

Removes an item data object by reference.

 > (`bool` bResult) WndFrame:RemoveItemData(`table|string` ref)

* <h4 id="LuaFrame_LookUpItemData">LookUpItemData</h4>

Looks up an item data object by key.

 > (`userdata` ItemData) WndFrame:LookUpItemData(`string` szKey)

* <h4 id="LuaFrame_GetItemDataKey">GetItemDataKey</h4>

Gets the key string for an item data object.

 > (`string` szKey) WndFrame:GetItemDataKey(`userdata` ItemData)

* <h4 id="LuaFrame_SwitchLayer">SwitchLayer</h4>

Switches the frame to a specific layer.

 > (`void`) WndFrame:SwitchLayer(`string` szLayer)

* <h4 id="LuaFrame_IsVisibleInCurrentShowMode">IsVisibleInCurrentShowMode</h4>

Returns whether the frame is visible in the current show mode.

 > (`bool` bVisible) WndFrame:IsVisibleInCurrentShowMode()

* <h4 id="LuaFrame_IsVisibleInShowMode">IsVisibleInShowMode</h4>

Returns whether the frame is visible in a specific show mode.

 > (`bool` bVisible) WndFrame:IsVisibleInShowMode(`string` szMode)

* <h4 id="LuaFrame_AddShowModeByName">AddShowModeByName</h4>

Adds a show mode by name.

 > (`bool` bOk) WndFrame:AddShowModeByName(`string` szMode)

* <h4 id="LuaFrame_RemoveShowModeByName">RemoveShowModeByName</h4>

Removes a show mode by name.

 > (`bool` bOk) WndFrame:RemoveShowModeByName(`string` szMode)

* <h4 id="LuaFrame_GetViewLevel">GetViewLevel</h4>

Gets the view level.

 > (`number` nLevel) WndFrame:GetViewLevel()

* <h4 id="LuaFrame_IsViewMutex">IsViewMutex</h4>

Returns whether view-mutex is enabled.

 > (`bool` bMutex) WndFrame:IsViewMutex()

* <h4 id="LuaFrame_GetViewMutexKey">GetViewMutexKey</h4>

Gets the view-mutex key string.

 > (`string` szKey) WndFrame:GetViewMutexKey()

* <h4 id="LuaFrame_IsAddBackGround">IsAddBackGround</h4>

Returns whether the frame adds a background.

 > (`bool` bBg) WndFrame:IsAddBackGround()
