English | [中文](./KSQLite3.zh-CN.md)

# KSQLite3

## Methods

* <h4 id="LuaKSQLite3_Execute">Execute</h4>
> KSQLite3:Execute(pszSQL) -> tRows, nRetCode

Executes a SQL statement and returns:

- `tRows`: an array-like table of rows (each row is a table), or `nil` on failure.
- `nRetCode`: number.

* <h4 id="LuaKSQLite3_GetValue">GetValue</h4>
> KSQLite3:GetValue(pszSQL) -> value, nRetCode

Executes a SQL statement and returns the first column of the first row.

- `value`: the value, or `nil` if there is no row or on failure.
- `nRetCode`: number.

* <h4 id="LuaKSQLite3_Prepare">Prepare</h4>
> KSQLite3:Prepare(pszSQL) -> KSQLite3Stmt

Prepares a SQL statement and returns a `KSQLite3Stmt` userdata.

Returns nothing on failure.

* <h4 id="LuaKSQLite3_Release">Release</h4>
> KSQLite3:Release()

Releases this `KSQLite3` userdata.

This is also used as the `__gc` metamethod.
