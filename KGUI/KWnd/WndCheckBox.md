# WndCheckBox

Notes:

- `WndCheckBox` inherits all methods from `WndWindow`; only additional methods are listed here.

[`IsCheckBoxActive`](#LuaCheckBox_IsCheckBoxActive)
[`Enable`](#LuaCheckBox_Enable)
[`IsEnabled`](#LuaCheckBox_IsEnabled)
[`IsCheckBoxChecked`](#LuaCheckBox_IsCheckBoxChecked)
[`Check`](#LuaCheckBox_Check)
[`ToggleCheck`](#LuaCheckBox_ToggleCheck)
[`SetAnimation`](#LuaCheckBox_SetAnimation)
[`SetStatus`](#LuaCheckBox_SetStatus)
[`IsStatus`](#LuaCheckBox_IsStatus)

* <h4 id="LuaCheckBox_IsCheckBoxActive">IsCheckBoxActive</h4>

Returns whether the checkbox is active.

 > (`bool` bActive) WndCheckBox:IsCheckBoxActive()

* <h4 id="LuaCheckBox_Enable">Enable</h4>

Enables or disables the checkbox.

 > (`void`) WndCheckBox:Enable(`bool|number` bEnable)

* <h4 id="LuaCheckBox_IsEnabled">IsEnabled</h4>

Returns whether the checkbox is enabled.

 > (`bool` bEnable) WndCheckBox:IsEnabled()

* <h4 id="LuaCheckBox_IsCheckBoxChecked">IsCheckBoxChecked</h4>

Returns whether the checkbox is currently checked.

 > (`bool` bChecked) WndCheckBox:IsCheckBoxChecked()

* <h4 id="LuaCheckBox_Check">Check</h4>

Sets the checked state.

 > (`void`) WndCheckBox:Check(`bool|number` bChecked)

* <h4 id="LuaCheckBox_ToggleCheck">ToggleCheck</h4>

Toggles the checked state.

 > (`void`) WndCheckBox:ToggleCheck()

* <h4 id="LuaCheckBox_SetAnimation">SetAnimation</h4>

Sets animation groups and animation path for different checkbox states.

 > (`void`) WndCheckBox:SetAnimation(`number` nGroupNormal, `number` nGroupMouseOver, `number` nGroupMouseDown, `number` nGroupDisable, `string` szPath)

* <h4 id="LuaCheckBox_SetStatus">SetStatus</h4>

Enables or disables a specific status flag on the checkbox.

 > (`void`) WndCheckBox:SetStatus(`number` dwStatus, `bool` bEnable)

* <h4 id="LuaCheckBox_IsStatus">IsStatus</h4>

Checks whether a specific status flag is enabled.

 > (`bool` bEnable) WndCheckBox:IsStatus(`number` dwStatus)
