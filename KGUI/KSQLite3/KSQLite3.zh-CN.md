[English](./KSQLite3.md) | 中文

# KSQLite3

## 方法

* <h4 id="LuaKSQLite3_Execute">Execute</h4>
> KSQLite3:Execute(pszSQL) -> tRows, nRetCode

执行 SQL 语句并返回：

- `tRows`：类数组的 table，元素为“行 table”；失败时为 `nil`。
- `nRetCode`：number。

* <h4 id="LuaKSQLite3_GetValue">GetValue</h4>
> KSQLite3:GetValue(pszSQL) -> value, nRetCode

执行 SQL 语句并返回“第一行第一列”的值。

- `value`：结果值；若无行或失败则为 `nil`。
- `nRetCode`：number。

* <h4 id="LuaKSQLite3_Prepare">Prepare</h4>
> KSQLite3:Prepare(pszSQL) -> KSQLite3Stmt

预编译 SQL 语句并返回 `KSQLite3Stmt` userdata。

失败时不返回任何值。

* <h4 id="LuaKSQLite3_Release">Release</h4>
> KSQLite3:Release()

释放该 `KSQLite3` userdata。

该实现也作为 `__gc` 元方法使用。
