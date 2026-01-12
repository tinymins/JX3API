[English](./Hotkey.md) | 中文

# Hotkey

## 函数

* <h4 id="Lua_Load">Load</h4>
> Hotkey.Load(pcszFile)

从文件加载按键绑定。

* <h4 id="Lua_LoadAsAdd">LoadAsAdd</h4>
> Hotkey.LoadAsAdd(pcszFile)

从文件加载按键绑定，并以“追加/合并”的方式生效。

* <h4 id="Lua_LoadDefault">LoadDefault</h4>
> Hotkey.LoadDefault()

加载默认按键绑定。

* <h4 id="Lua_LoadFromLuaAsAdd">LoadFromLuaAsAdd</h4>
> Hotkey.LoadFromLuaAsAdd(...) -> nResult

从 Lua 数据加载并以“追加/合并”的方式生效。

参数形式取决于调用方提供的 Lua 数据结构。

* <h4 id="Lua_GetBinding">GetBinding</h4>
> Hotkey.GetBinding([bDefault]) -> tBindings

以类数组 table 的形式返回当前按键绑定列表。

- `bDefault`（可选）：boolean/number。为真时尝试返回默认绑定键值。

* <h4 id="Lua_Save">Save</h4>
> Hotkey.Save(pcszFile)

保存按键绑定到文件。

* <h4 id="Lua_SaveAsAdd">SaveAsAdd</h4>
> Hotkey.SaveAsAdd(pcszFile)

以“追加/合并”格式保存按键绑定到文件。

* <h4 id="Lua_SaveToLuaAsAdd">SaveToLuaAsAdd</h4>
> Hotkey.SaveToLuaAsAdd(...) -> nResult

将绑定保存到 Lua 数据形式（用于“追加/合并”）。

参数形式取决于调用方提供的 Lua 容器。

* <h4 id="Lua_Clear">Clear</h4>
> Hotkey.Clear()

清空所有绑定。

* <h4 id="Lua_Set">Set</h4>
> Hotkey.Set(pcszCommand, nIndex, nKey[, bShift[, bCtrl[, bAlt]]])

设置 `pcszCommand` 的第 `nIndex` 个绑定槽。

- `nKey`：number。
- `bShift`/`bCtrl`/`bAlt`（可选）：boolean 或 number。

* <h4 id="Lua_Get">Get</h4>
> Hotkey.Get(pcszCommand[, nIndex]) -> nKey, bShift, bCtrl, bAlt, bExist

获取 `pcszCommand` 的绑定信息。

* <h4 id="Lua_IsUsed">IsUsed</h4>
> Hotkey.IsUsed(nKey[, bShift[, bCtrl[, bAlt]]]) -> bUsed

判断指定按键组合是否已被占用。

* <h4 id="Lua_IsKeyDown">IsKeyDown</h4>
> Hotkey.IsKeyDown(nKey[, bShift[, bCtrl[, bAlt]]]) -> bDown

判断指定按键组合当前是否处于按下状态。

* <h4 id="Lua_IsCapsLockOn">IsCapsLockOn</h4>
> Hotkey.IsCapsLockOn() -> bOn

判断 CapsLock 是否开启。

* <h4 id="Lua_IsKeyDoubleDown">IsKeyDoubleDown</h4>
> Hotkey.IsKeyDoubleDown() -> bDown

返回是否检测到“双击按下”状态。

* <h4 id="Lua_GetKeyTimeInterval">GetKeyTimeInterval</h4>
> Hotkey.GetKeyTimeInterval() -> dwTime

返回系统使用的按键时间间隔。

* <h4 id="Lua_SetCapture">SetCapture</h4>
> Hotkey.SetCapture(bCap)

开启/关闭按键捕获。

- `bCap`：boolean 或 number。

* <h4 id="Lua_AddBinding">AddBinding</h4>
> Hotkey.AddBinding(szName, szDesc, szHeader, fnDown, fnUp[, arg6[, arg7]])

新增一个绑定条目（主要用于 addon）。

- `szName`：string。
- `szDesc`：string。
- `szHeader`：string 或 `nil`。
- `fnDown`：function 或 `nil`。
- `fnUp`：function 或 `nil`。
- `arg6`（可选）：
  - boolean/number：视为 `bUnchangeable`，或
  - string：视为 `szTip`。
- `arg7`（可选）：boolean/number，当 `arg6` 为 `szTip` 时用作 `bUnchangeable`。

* <h4 id="Lua_Enable">Enable</h4>
> Hotkey.Enable(bEnable)

全局启用/禁用按键系统。

* <h4 id="Lua_IsEnable">IsEnable</h4>
> Hotkey.IsEnable() -> bEnable

返回按键系统是否启用。

* <h4 id="Lua_GetCaptureKey">GetCaptureKey</h4>
> Hotkey.GetCaptureKey() -> nKey, bShift, bCtrl, bAlt

获取最近一次捕获到的按键组合。

* <h4 id="Lua_ClearEnvBinding">ClearEnvBinding</h4>
> Hotkey.ClearEnvBinding(bAddon)

清除环境绑定。

- `bAddon`：boolean。

* <h4 id="Lua_Remove">Remove</h4>
> Hotkey.Remove(nKey[, bShift[, bCtrl[, bAlt]]])

按按键组合移除绑定。

* <h4 id="LuaBinding_GetCommand">GetCommand</h4>
> Hotkey.GetCommand(nIndex) -> szCommand

返回索引 `nIndex` 对应的命令名。

* <h4 id="LuaBinding_Popback">PopbackBinding</h4>
> Hotkey.PopbackBinding()

回退（弹出）最近一次绑定。

* <h4 id="LuaBinding_GetCount">GetBindingCount</h4>
> Hotkey.GetBindingCount() -> nCount

返回绑定条目数量。

* <h4 id="Lua_ShieldAll">ShieldAll</h4>
> Hotkey.ShieldAll(bShield)

全局屏蔽/取消屏蔽按键。

* <h4 id="Lua_ModifyShield">ModifyShield</h4>
> Hotkey.ModifyShield(bShield, nKey[, bShift[, bCtrl[, bAlt]]])

修改某个按键组合的屏蔽状态。

* <h4 id="Lua_EnableNewMode">EnableNewMode</h4>
> Hotkey.EnableNewMode(bEnable)

启用/禁用按键“新模式”。
