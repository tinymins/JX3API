<!-- markdownlint-disable MD041 MD033 MD032 MD004 -->

[English](./KUnQLite.md) | 中文

# KUnQLite

## 方法

* <h4 id="LuaKUnQLite_Set">Set</h4>
> KUnQLite:Set(szKey, valueOrNil) -> nRetCode

设置键值对。

- `szKey`：string。
- `valueOrNil`：string|number|boolean|table|nil。
  - 若为 `nil`，则等价于删除该键。

返回值：
- `nRetCode`：number。

失败时不返回任何值。

* <h4 id="LuaKUnQLite_Get">Get</h4>
> KUnQLite:Get(szKey) -> valueOrNil, nRetCode

按键获取值。

- `szKey`：string。

返回值：
- `valueOrNil`：string|number|boolean|table|nil。
- `nRetCode`：number。

失败时不返回任何值。

* <h4 id="LuaKUnQLite_Delete">Delete</h4>
> KUnQLite:Delete(szKey) -> nRetCode

删除指定键。

- `szKey`：string。

返回值：
- `nRetCode`：number。

失败时不返回任何值。

* <h4 id="LuaKUnQLite_Release">Release</h4>
> KUnQLite:Release()

释放该 `KUnQLite` userdata。

同时作为 `__gc` 元方法使用。
