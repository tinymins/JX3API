English | [中文](./Hotkey.zh-CN.md)

# Hotkey

## Functions

* <h4 id="Lua_Load">Load</h4>
> Hotkey.Load(pcszFile)

Loads hotkey bindings from a file.

* <h4 id="Lua_LoadAsAdd">LoadAsAdd</h4>
> Hotkey.LoadAsAdd(pcszFile)

Loads hotkey bindings from a file and merges/adds them.

* <h4 id="Lua_LoadDefault">LoadDefault</h4>
> Hotkey.LoadDefault()

Loads default hotkey bindings.

* <h4 id="Lua_LoadFromLuaAsAdd">LoadFromLuaAsAdd</h4>
> Hotkey.LoadFromLuaAsAdd(...) -> nResult

Loads bindings from Lua data and merges/adds them.

The accepted parameters depend on the caller-provided Lua data format.

* <h4 id="Lua_GetBinding">GetBinding</h4>
> Hotkey.GetBinding([bDefault]) -> tBindings

Returns current hotkey bindings as an array-like table.

- `bDefault` (optional): boolean/number. If true, attempts to return default binding keys.

* <h4 id="Lua_Save">Save</h4>
> Hotkey.Save(pcszFile)

Saves hotkey bindings to a file.

* <h4 id="Lua_SaveAsAdd">SaveAsAdd</h4>
> Hotkey.SaveAsAdd(pcszFile)

Saves hotkey bindings to a file as an “add/merge” format.

* <h4 id="Lua_SaveToLuaAsAdd">SaveToLuaAsAdd</h4>
> Hotkey.SaveToLuaAsAdd(...) -> nResult

Saves bindings into a Lua data form for “add/merge”.

The accepted parameters depend on the caller-provided Lua container.

* <h4 id="Lua_Clear">Clear</h4>
> Hotkey.Clear()

Clears all bindings.

* <h4 id="Lua_Set">Set</h4>
> Hotkey.Set(pcszCommand, nIndex, nKey[, bShift[, bCtrl[, bAlt]]])

Sets a binding for command `pcszCommand` at slot `nIndex`.

- `nKey`: number.
- `bShift`/`bCtrl`/`bAlt` (optional): boolean or number.

* <h4 id="Lua_Get">Get</h4>
> Hotkey.Get(pcszCommand[, nIndex]) -> nKey, bShift, bCtrl, bAlt, bExist

Gets the binding for command `pcszCommand`.

* <h4 id="Lua_IsUsed">IsUsed</h4>
> Hotkey.IsUsed(nKey[, bShift[, bCtrl[, bAlt]]]) -> bUsed

Checks whether the specified hotkey is already used.

* <h4 id="Lua_IsKeyDown">IsKeyDown</h4>
> Hotkey.IsKeyDown(nKey[, bShift[, bCtrl[, bAlt]]]) -> bDown

Checks whether the specified hotkey is currently pressed.

* <h4 id="Lua_IsCapsLockOn">IsCapsLockOn</h4>
> Hotkey.IsCapsLockOn() -> bOn

Checks whether CapsLock is on.

* <h4 id="Lua_IsKeyDoubleDown">IsKeyDoubleDown</h4>
> Hotkey.IsKeyDoubleDown() -> bDown

Returns whether a “double key down” state is detected.

* <h4 id="Lua_GetKeyTimeInterval">GetKeyTimeInterval</h4>
> Hotkey.GetKeyTimeInterval() -> dwTime

Returns the key time interval used by the system.

* <h4 id="Lua_SetCapture">SetCapture</h4>
> Hotkey.SetCapture(bCap)

Enables/disables capturing hotkeys.

- `bCap`: boolean or number.

* <h4 id="Lua_AddBinding">AddBinding</h4>
> Hotkey.AddBinding(szName, szDesc, szHeader, fnDown, fnUp[, arg6[, arg7]])

Adds a binding entry (primarily for addon usage).

- `szName`: string.
- `szDesc`: string.
- `szHeader`: string or `nil`.
- `fnDown`: function or `nil`.
- `fnUp`: function or `nil`.
- `arg6` (optional):
  - boolean/number: treated as `bUnchangeable`, OR
  - string: treated as `szTip`.
- `arg7` (optional): boolean/number, used as `bUnchangeable` when `arg6` is `szTip`.

* <h4 id="Lua_Enable">Enable</h4>
> Hotkey.Enable(bEnable)

Enables/disables hotkeys globally.

* <h4 id="Lua_IsEnable">IsEnable</h4>
> Hotkey.IsEnable() -> bEnable

Returns whether hotkeys are enabled.

* <h4 id="Lua_GetCaptureKey">GetCaptureKey</h4>
> Hotkey.GetCaptureKey() -> nKey, bShift, bCtrl, bAlt

Gets the last captured hotkey.

* <h4 id="Lua_ClearEnvBinding">ClearEnvBinding</h4>
> Hotkey.ClearEnvBinding(bAddon)

Clears environment bindings.

- `bAddon`: boolean.

* <h4 id="Lua_Remove">Remove</h4>
> Hotkey.Remove(nKey[, bShift[, bCtrl[, bAlt]]])

Removes a binding by hotkey.

* <h4 id="LuaBinding_GetCommand">GetCommand</h4>
> Hotkey.GetCommand(nIndex) -> szCommand

Returns command name at index `nIndex`.

* <h4 id="LuaBinding_Popback">PopbackBinding</h4>
> Hotkey.PopbackBinding()

Pops back the latest binding.

* <h4 id="LuaBinding_GetCount">GetBindingCount</h4>
> Hotkey.GetBindingCount() -> nCount

Returns the number of binding entries.

* <h4 id="Lua_ShieldAll">ShieldAll</h4>
> Hotkey.ShieldAll(bShield)

Enables/disables shielding all hotkeys.

* <h4 id="Lua_ModifyShield">ModifyShield</h4>
> Hotkey.ModifyShield(bShield, nKey[, bShift[, bCtrl[, bAlt]]])

Modifies shielding for a specific hotkey.

* <h4 id="Lua_EnableNewMode">EnableNewMode</h4>
> Hotkey.EnableNewMode(bEnable)

Enables/disables the “new mode” for hotkeys.
