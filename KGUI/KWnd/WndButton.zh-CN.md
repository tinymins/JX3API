[English](./WndButton.md) | 中文

# WndButton（按钮）

说明：

- `WndButton` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

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

获取按钮当前是否启用。

 > (`bool` bEnable) WndButton:IsEnabled()

* <h4 id="LuaButton_Enable">Enable</h4>

设置按钮是否启用。

`bEnable` 支持传入 `bool` 或 `number`（Lua 绑定会按类型分支转换为整数布尔值）。

若 `bOnlyUserAction` 为 true，则调用底层 `EnableUserAction`；否则调用 `Enable`。

参数个数必须为 2 或 3，否则会报错。

 > (`void`) WndButton:Enable(`bool|number` bEnable[, `bool|number` bOnlyUserAction = false])

* <h4 id="LuaButton_SetAnimatePath">SetAnimatePath</h4>

设置按钮使用的动画资源路径。

内部会使用当前的 4 个 group（Normal/MouseOver/MouseDown/Disable）与 `szPath` 一并调用 `SetAnimation(...)`。

 > (`void`) WndButton:SetAnimatePath(`string` szPath)

* <h4 id="LuaButton_GetAnimatePath">GetAnimatePath</h4>

获取当前动画资源路径。

 > (`string` szPath) WndButton:GetAnimatePath()

* <h4 id="LuaButton_SetAnimateGroupNormal">SetAnimateGroupNormal</h4>

设置 Normal 状态使用的动画 group。

 > (`void`) WndButton:SetAnimateGroupNormal(`number` nGroup)

* <h4 id="LuaButton_GetAnimateGroupNormal">GetAnimateGroupNormal</h4>

获取 Normal 状态使用的动画 group。

 > (`number` nGroup) WndButton:GetAnimateGroupNormal()

* <h4 id="LuaButton_SetAnimateGroupMouseOver">SetAnimateGroupMouseOver</h4>

设置 MouseOver 状态使用的动画 group。

 > (`void`) WndButton:SetAnimateGroupMouseOver(`number` nGroup)

* <h4 id="LuaButton_GetAnimateGroupMouseOver">GetAnimateGroupMouseOver</h4>

获取 MouseOver 状态使用的动画 group。

 > (`number` nGroup) WndButton:GetAnimateGroupMouseOver()

* <h4 id="LuaButton_SetAnimateGroupMouseDown">SetAnimateGroupMouseDown</h4>

设置 MouseDown 状态使用的动画 group。

 > (`void`) WndButton:SetAnimateGroupMouseDown(`number` nGroup)

* <h4 id="LuaButton_GetAnimateGroupMouseDown">GetAnimateGroupMouseDown</h4>

获取 MouseDown 状态使用的动画 group。

 > (`number` nGroup) WndButton:GetAnimateGroupMouseDown()

* <h4 id="LuaButton_SetAnimateGroupDisable">SetAnimateGroupDisable</h4>

设置 Disable 状态使用的动画 group。

 > (`void`) WndButton:SetAnimateGroupDisable(`number` nGroup)

* <h4 id="LuaButton_GetAnimateGroupDisable">GetAnimateGroupDisable</h4>

获取 Disable 状态使用的动画 group。

 > (`number` nGroup) WndButton:GetAnimateGroupDisable()

* <h4 id="LuaButton_RegisterLButtonDrag">RegisterLButtonDrag</h4>

注册左键拖拽支持。

 > (`void`) WndButton:RegisterLButtonDrag()

* <h4 id="LuaButton_UnregisterLButtonDrag">UnregisterLButtonDrag</h4>

取消注册左键拖拽支持。

 > (`void`) WndButton:UnregisterLButtonDrag()

* <h4 id="LuaButton_IsLButtonDragable">IsLButtonDragable</h4>

检查是否已启用左键拖拽。

 > (`bool` bDragable) WndButton:IsLButtonDragable()

* <h4 id="LuaButton_RegisterRButtonDrag">RegisterRButtonDrag</h4>

注册右键拖拽支持。

 > (`void`) WndButton:RegisterRButtonDrag()

* <h4 id="LuaButton_UnregisterRButtonDrag">UnregisterRButtonDrag</h4>

取消注册右键拖拽支持。

 > (`void`) WndButton:UnregisterRButtonDrag()

* <h4 id="LuaButton_IsRButtonDragable">IsRButtonDragable</h4>

检查是否已启用右键拖拽。

 > (`bool` bDragable) WndButton:IsRButtonDragable()

* <h4 id="LuaButton_SetStatus">SetStatus</h4>

设置指定状态位。

参数类型要求：`dwStatus` 必须为 number，`bEnable` 必须为 bool；否则会报错。

 > (`void`) WndButton:SetStatus(`number` dwStatus, `bool` bEnable)

* <h4 id="LuaButton_IsStatus">IsStatus</h4>

检查指定状态位是否启用。

参数类型要求：`dwStatus` 必须为 number；否则会报错。

 > (`bool` bEnable) WndButton:IsStatus(`number` dwStatus)
