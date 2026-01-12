<!-- markdownlint-disable MD041 MD033 MD032 MD004 -->

English | [中文](./KUnQLite.zh-CN.md)

# KUnQLite

## Methods

* <h4 id="LuaKUnQLite_Set">Set</h4>
> KUnQLite:Set(szKey, valueOrNil) -> nRetCode

Sets a key-value pair.

- `szKey`: string.
- `valueOrNil`: string|number|boolean|table|nil.
  - If `nil`, this call deletes the key.

Returns:
- `nRetCode`: number.

Returns nothing on failure.

* <h4 id="LuaKUnQLite_Get">Get</h4>
> KUnQLite:Get(szKey) -> valueOrNil, nRetCode

Gets a value by key.

- `szKey`: string.

Returns:
- `valueOrNil`: string|number|boolean|table|nil.
- `nRetCode`: number.

Returns nothing on failure.

* <h4 id="LuaKUnQLite_Delete">Delete</h4>
> KUnQLite:Delete(szKey) -> nRetCode

Deletes a key.

- `szKey`: string.

Returns:
- `nRetCode`: number.

Returns nothing on failure.

* <h4 id="LuaKUnQLite_Release">Release</h4>
> KUnQLite:Release()

Releases this `KUnQLite` userdata.

This is also used as the `__gc` metamethod.
