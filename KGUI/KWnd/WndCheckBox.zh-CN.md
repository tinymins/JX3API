[English](./WndCheckBox.md) | 中文

# WndCheckBox（复选框）

说明：

- `WndCheckBox` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

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

检查复选框是否处于 Active 状态。

 > (`bool` bActive) WndCheckBox:IsCheckBoxActive()

* <h4 id="LuaCheckBox_Enable">Enable</h4>

设置复选框是否可用。

`bEnable` 支持传入 `bool` 或 `number`（Lua 绑定会按类型分支转换为整数布尔值），内部调用 `EnableCheck`。

 > (`void`) WndCheckBox:Enable(`bool|number` bEnable)

* <h4 id="LuaCheckBox_IsEnabled">IsEnabled</h4>

获取复选框是否可用。

 > (`bool` bEnable) WndCheckBox:IsEnabled()

* <h4 id="LuaCheckBox_IsCheckBoxChecked">IsCheckBoxChecked</h4>

获取复选框是否已勾选。

 > (`bool` bChecked) WndCheckBox:IsCheckBoxChecked()

* <h4 id="LuaCheckBox_Check">Check</h4>

设置复选框的勾选状态。

`bChecked` 支持传入 `bool` 或 `number`。

可选参数 `eFireType` 为事件触发类型（数值枚举）；参数个数必须为 2 或 3。

 > (`void`) WndCheckBox:Check(`bool|number` bChecked)

* <h4 id="LuaCheckBox_ToggleCheck">ToggleCheck</h4>

切换勾选状态：若当前已勾选则取消，否则勾选。

 > (`void`) WndCheckBox:ToggleCheck()

* <h4 id="LuaCheckBox_SetAnimation">SetAnimation</h4>

设置复选框动画资源。

实现要求参数个数必须为 12（含 self）。其中第 2 个参数为 `szPath`（会先经过 `FormatFilePath()`），第 3~12 个参数为一组动画 group 值，按实现顺序依次为：

- `nUnCheckAndEnable`
- `nCheckAndEnable`
- `nUnCheckAndDisable`
- `nCheckAndDisable`
- `nChecking`
- `nUnChecking`
- `nCheckedAndEnableWhenMouseOver`
- `nUncheckedAndEnableWhenMouseOver`
- `nCheckedAndDisableWhenMouseOver`
- `nUncheckedAndDisableWhenMouseOver`

 > (`void`) WndCheckBox:SetAnimation(`number` nGroupNormal, `number` nGroupMouseOver, `number` nGroupMouseDown, `number` nGroupDisable, `string` szPath)

* <h4 id="LuaCheckBox_SetStatus">SetStatus</h4>

设置指定状态位。

参数类型要求：`dwStatus` 必须为 number，`bEnable` 必须为 bool；否则会报错。

 > (`void`) WndCheckBox:SetStatus(`number` dwStatus, `bool` bEnable)

* <h4 id="LuaCheckBox_IsStatus">IsStatus</h4>

检查指定状态位是否启用。

参数类型要求：`dwStatus` 必须为 number；否则会报错。

 > (`bool` bEnable) WndCheckBox:IsStatus(`number` dwStatus)
