# WndButton

Notes:

- `WndButton` inherits all methods from `WndWindow`; only additional methods are listed here.

[`IsEnabled`](#LuaButton_IsEnabled)
[`Enable`](#LuaButton_Enable)
[`SetAnimatePath`](#LuaButton_SetAnimatePath)
[`GetAnimatePath`](#LuaButton_GetAnimatePath)
[`SetAnimateGroupNormal`](#LuaButton_SetAnimateGroupNormal)
[`GetAnimateGroupNormal`](#LuaButton_GetAnimateGroupNormal)
[`SetAnimateGroupMouseOver`](#LuaButton_SetAnimateGroupMouseOver)
[`GetAnimateGroupMouseOver`](#LuaButton_GetAnimateGroupMouseOver)
[`SetAnimateGroupMouseDown`](#LuaButton_SetAnimateGroupMouseDown)
[`GetAnimateGroupMouseDown`](#LuaButton_GetAnimateGroupMouseDown)
[`SetAnimateGroupDisable`](#LuaButton_SetAnimateGroupDisable)
[`GetAnimateGroupDisable`](#LuaButton_GetAnimateGroupDisable)
[`RegisterLButtonDrag`](#LuaButton_RegisterLButtonDrag)
[`UnregisterLButtonDrag`](#LuaButton_UnregisterLButtonDrag)
[`IsLButtonDragable`](#LuaButton_IsLButtonDragable)
[`RegisterRButtonDrag`](#LuaButton_RegisterRButtonDrag)
[`UnregisterRButtonDrag`](#LuaButton_UnregisterRButtonDrag)
[`IsRButtonDragable`](#LuaButton_IsRButtonDragable)
[`SetStatus`](#LuaButton_SetStatus)
[`IsStatus`](#LuaButton_IsStatus)

* <h4 id="LuaButton_IsEnabled">IsEnabled</h4>

 > (`bool` bEnable) WndButton:IsEnabled()

* <h4 id="LuaButton_Enable">Enable</h4>

 > (`void`) WndButton:Enable(`bool|number` bEnable[, `bool|number` bOnlyUserAction = false])

Notes:

- When `bOnlyUserAction` is true, calls `EnableUserAction`; otherwise calls `Enable`.

* <h4 id="LuaButton_SetAnimatePath">SetAnimatePath</h4>

 > (`void`) WndButton:SetAnimatePath(`string` szPath)

* <h4 id="LuaButton_GetAnimatePath">GetAnimatePath</h4>

 > (`string` szPath) WndButton:GetAnimatePath()

* <h4 id="LuaButton_SetAnimateGroupNormal">SetAnimateGroupNormal</h4>

 > (`void`) WndButton:SetAnimateGroupNormal(`number` nGroup)

* <h4 id="LuaButton_GetAnimateGroupNormal">GetAnimateGroupNormal</h4>

 > (`number` nGroup) WndButton:GetAnimateGroupNormal()

* <h4 id="LuaButton_SetAnimateGroupMouseOver">SetAnimateGroupMouseOver</h4>

 > (`void`) WndButton:SetAnimateGroupMouseOver(`number` nGroup)

* <h4 id="LuaButton_GetAnimateGroupMouseOver">GetAnimateGroupMouseOver</h4>

 > (`number` nGroup) WndButton:GetAnimateGroupMouseOver()

* <h4 id="LuaButton_SetAnimateGroupMouseDown">SetAnimateGroupMouseDown</h4>

 > (`void`) WndButton:SetAnimateGroupMouseDown(`number` nGroup)

* <h4 id="LuaButton_GetAnimateGroupMouseDown">GetAnimateGroupMouseDown</h4>

 > (`number` nGroup) WndButton:GetAnimateGroupMouseDown()

* <h4 id="LuaButton_SetAnimateGroupDisable">SetAnimateGroupDisable</h4>

 > (`void`) WndButton:SetAnimateGroupDisable(`number` nGroup)

* <h4 id="LuaButton_GetAnimateGroupDisable">GetAnimateGroupDisable</h4>

 > (`number` nGroup) WndButton:GetAnimateGroupDisable()

* <h4 id="LuaButton_RegisterLButtonDrag">RegisterLButtonDrag</h4>

 > (`void`) WndButton:RegisterLButtonDrag()

* <h4 id="LuaButton_UnregisterLButtonDrag">UnregisterLButtonDrag</h4>

 > (`void`) WndButton:UnregisterLButtonDrag()

* <h4 id="LuaButton_IsLButtonDragable">IsLButtonDragable</h4>

 > (`bool` bDragable) WndButton:IsLButtonDragable()

* <h4 id="LuaButton_RegisterRButtonDrag">RegisterRButtonDrag</h4>

 > (`void`) WndButton:RegisterRButtonDrag()

* <h4 id="LuaButton_UnregisterRButtonDrag">UnregisterRButtonDrag</h4>

 > (`void`) WndButton:UnregisterRButtonDrag()

* <h4 id="LuaButton_IsRButtonDragable">IsRButtonDragable</h4>

 > (`bool` bDragable) WndButton:IsRButtonDragable()

* <h4 id="LuaButton_SetStatus">SetStatus</h4>

 > (`void`) WndButton:SetStatus(`number` dwStatus, `bool` bEnable)

* <h4 id="LuaButton_IsStatus">IsStatus</h4>

 > (`bool` bEnable) WndButton:IsStatus(`number` dwStatus)
