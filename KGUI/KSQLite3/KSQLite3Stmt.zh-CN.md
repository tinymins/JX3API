[English](./KSQLite3Stmt.md) | 中文

# KSQLite3Stmt

## 方法

* <h4 id="LuaKSQLite3Stmt_Bind">Bind</h4>
> KSQLite3Stmt:Bind(nIndex, value) -> nResult

将 `value` 绑定到第 `nIndex` 个参数。

返回 `nResult`（number）。

* <h4 id="LuaKSQLite3Stmt_BindAll">BindAll</h4>
> KSQLite3Stmt:BindAll(...) -> nResult

按顺序绑定传入的所有参数值。

返回 `nResult`（number）。

* <h4 id="LuaKSQLite3Stmt_ClearBindings">ClearBindings</h4>
> KSQLite3Stmt:ClearBindings()

清除所有参数绑定并重置语句。

* <h4 id="LuaKSQLite3Stmt_GetNext">GetNext</h4>
> KSQLite3Stmt:GetNext() -> tRow, nRetCode

获取下一行。

- `tRow`：行 table；如果没有行则为 `nil`。
- `nRetCode`：number。

* <h4 id="LuaKSQLite3Stmt_GetAll">GetAll</h4>
> KSQLite3Stmt:GetAll() -> tRows, nRetCode

读取剩余的所有行。

- `tRows`：类数组的 table，元素为“行 table”。
- `nRetCode`：number。

* <h4 id="LuaKSQLite3Stmt_Execute">Execute</h4>
> KSQLite3Stmt:Execute() -> nRetCode

执行/推进一次语句并返回 `nRetCode`。

* <h4 id="LuaKSQLite3Stmt_Reset">Reset</h4>
> KSQLite3Stmt:Reset()

重置语句。

* <h4 id="LuaKSQLite3Stmt_Release">Release</h4>
> KSQLite3Stmt:Release()

Finalize 并释放该 `KSQLite3Stmt` userdata。

该实现也作为 `__gc` 元方法使用。
