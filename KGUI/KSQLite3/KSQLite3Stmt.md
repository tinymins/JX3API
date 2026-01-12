English | [中文](./KSQLite3Stmt.zh-CN.md)

# KSQLite3Stmt

## Methods

* <h4 id="LuaKSQLite3Stmt_Bind">Bind</h4>
> KSQLite3Stmt:Bind(nIndex, value) -> nResult

Binds `value` to parameter `nIndex`.

Returns `nResult` as a number.

* <h4 id="LuaKSQLite3Stmt_BindAll">BindAll</h4>
> KSQLite3Stmt:BindAll(...) -> nResult

Binds all provided values in order.

Returns `nResult` as a number.

* <h4 id="LuaKSQLite3Stmt_ClearBindings">ClearBindings</h4>
> KSQLite3Stmt:ClearBindings()

Clears all parameter bindings and resets the statement.

* <h4 id="LuaKSQLite3Stmt_GetNext">GetNext</h4>
> KSQLite3Stmt:GetNext() -> tRow, nRetCode

Steps to the next row.

- `tRow`: a row table, or `nil` if there is no row.
- `nRetCode`: number.

* <h4 id="LuaKSQLite3Stmt_GetAll">GetAll</h4>
> KSQLite3Stmt:GetAll() -> tRows, nRetCode

Reads all remaining rows.

- `tRows`: an array-like table of row tables.
- `nRetCode`: number.

* <h4 id="LuaKSQLite3Stmt_Execute">Execute</h4>
> KSQLite3Stmt:Execute() -> nRetCode

Executes/steps the statement once and returns `nRetCode`.

* <h4 id="LuaKSQLite3Stmt_Reset">Reset</h4>
> KSQLite3Stmt:Reset()

Resets the statement.

* <h4 id="LuaKSQLite3Stmt_Release">Release</h4>
> KSQLite3Stmt:Release()

Finalizes and releases this `KSQLite3Stmt` userdata.

This is also used as the `__gc` metamethod.
