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

 > (`void`) WndFrame:EnableDrag(`bool|number` bEnable)

* <h4 id="LuaFrame_IsDragable">IsDragable</h4>

 > (`bool` bEnable) WndFrame:IsDragable()

* <h4 id="LuaFrame_EnableFollowMouse">EnableFollowMouse</h4>

 > (`void`) WndFrame:EnableFollowMouse(`bool|number` bEnable)

* <h4 id="LuaFrame_IsFollowMouseMove">IsFollowMouseMove</h4>

 > (`bool` bEnable) WndFrame:IsFollowMouseMove()

* <h4 id="LuaFrame_SetDragArea">SetDragArea</h4>

 > (`void`) WndFrame:SetDragArea(`number` x, `number` y, `number` w, `number` h)

* <h4 id="LuaFrame_RegisterEvent">RegisterEvent</h4>

 > (`void`) WndFrame:RegisterEvent(`number` nEvent)

* <h4 id="LuaFrame_UnRegisterEvent">UnRegisterEvent</h4>

 > (`void`) WndFrame:UnRegisterEvent(`number` nEvent)

* <h4 id="LuaFrame_FocusPrev">FocusPrev</h4>

 > (`void`) WndFrame:FocusPrev()

* <h4 id="LuaFrame_FocusNext">FocusNext</h4>

 > (`void`) WndFrame:FocusNext()

* <h4 id="LuaFrame_FocusHome">FocusHome</h4>

 > (`void`) WndFrame:FocusHome()

* <h4 id="LuaFrame_FocusEnd">FocusEnd</h4>

 > (`void`) WndFrame:FocusEnd()

* <h4 id="LuaFrame_FadeIn">FadeIn</h4>

 > (`void`) WndFrame:FadeIn(`number` dwTime)

* <h4 id="LuaFrame_FadeOut">FadeOut</h4>

 > (`void`) WndFrame:FadeOut(`number` dwTime)

* <h4 id="LuaFrame_IsAlwaysTop">IsAlwaysTop</h4>

 > (`bool` bTop) WndFrame:IsAlwaysTop()

* <h4 id="LuaFrame_SetAlwaysTop">SetAlwaysTop</h4>

 > (`void`) WndFrame:SetAlwaysTop(`bool|number` bTop)

* <h4 id="LuaFrame_ShowWhenUIHide">ShowWhenUIHide</h4>

 > (`void`) WndFrame:ShowWhenUIHide()

* <h4 id="LuaFrame_HideWhenUIHide">HideWhenUIHide</h4>

 > (`void`) WndFrame:HideWhenUIHide()

* <h4 id="LuaFrame_IsVisibleWhenUIHide">IsVisibleWhenUIHide</h4>

 > (`bool` bVisible) WndFrame:IsVisibleWhenUIHide()

* <h4 id="LuaFrame_IsAddOn">IsAddOn</h4>

 > (`bool` bAddOn) WndFrame:IsAddOn()

* <h4 id="LuaFrame_CreateItemData">CreateItemData</h4>

 > (`userdata` ItemData) WndFrame:CreateItemData(`string` szKey)

* <h4 id="LuaFrame_RemoveItemData">RemoveItemData</h4>

 > (`void`) WndFrame:RemoveItemData(`string` szKey)

* <h4 id="LuaFrame_LookUpItemData">LookUpItemData</h4>

 > (`userdata` ItemData) WndFrame:LookUpItemData(`string` szKey)

* <h4 id="LuaFrame_GetItemDataKey">GetItemDataKey</h4>

 > (`string` szKey) WndFrame:GetItemDataKey(`userdata` ItemData)

* <h4 id="LuaFrame_SwitchLayer">SwitchLayer</h4>

 > (`void`) WndFrame:SwitchLayer(`number` nLayer)

* <h4 id="LuaFrame_IsVisibleInCurrentShowMode">IsVisibleInCurrentShowMode</h4>

 > (`bool` bVisible) WndFrame:IsVisibleInCurrentShowMode()

* <h4 id="LuaFrame_IsVisibleInShowMode">IsVisibleInShowMode</h4>

 > (`bool` bVisible) WndFrame:IsVisibleInShowMode(`string` szMode)

* <h4 id="LuaFrame_AddShowModeByName">AddShowModeByName</h4>

 > (`void`) WndFrame:AddShowModeByName(`string` szMode)

* <h4 id="LuaFrame_RemoveShowModeByName">RemoveShowModeByName</h4>

 > (`void`) WndFrame:RemoveShowModeByName(`string` szMode)

* <h4 id="LuaFrame_GetViewLevel">GetViewLevel</h4>

 > (`number` nLevel) WndFrame:GetViewLevel()

* <h4 id="LuaFrame_IsViewMutex">IsViewMutex</h4>

 > (`bool` bMutex) WndFrame:IsViewMutex()

* <h4 id="LuaFrame_GetViewMutexKey">GetViewMutexKey</h4>

 > (`string` szKey) WndFrame:GetViewMutexKey()

* <h4 id="LuaFrame_IsAddBackGround">IsAddBackGround</h4>

 > (`bool` bBg) WndFrame:IsAddBackGround()
