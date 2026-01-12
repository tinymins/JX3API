[English](./ITabFile.md) | 中文

# ITabFile

## 方法

* <h4 id="LuaTab_Save">Save</h4>
> ITabFile:Save(pcszFileName)

保存该 tab 文件。

* <h4 id="LuaTab_Close">Close</h4>
> ITabFile:Close()

释放该 `ITabFile` userdata。

* <h4 id="LuaTab_FindColumn">FindColumn</h4>
> ITabFile:FindColumn(szColumn) -> nColumn

按列名查找列索引。

失败时不返回任何值。

* <h4 id="LuaTab_GetWidth">GetWidth</h4>
> ITabFile:GetWidth() -> nWidth

返回列数。

* <h4 id="LuaTab_GetHeight">GetHeight</h4>
> ITabFile:GetHeight() -> nHeight

返回行数。

* <h4 id="LuaTab_GetString">GetString</h4>
> ITabFile:GetString(...) -> szValue

支持的调用形式：

- `ITabFile:GetString(nRow, nColumn, szDefault)`
- `ITabFile:GetString(nRow, szColumn, szDefault[, bColumnLab])`
- `ITabFile:GetString(szRow, szColumn, szDefault)`

* <h4 id="LuaTab_GetInteger">GetInteger</h4>
> ITabFile:GetInteger(...) -> nValue

支持的调用形式：

- `ITabFile:GetInteger(nRow, nColumn, nDefault)`
- `ITabFile:GetInteger(nRow, szColumn, nDefault[, bColumnLab])`
- `ITabFile:GetInteger(szRow, szColumn, nDefault)`

失败时不返回任何值。

* <h4 id="LuaTab_GetFloat">GetFloat</h4>
> ITabFile:GetFloat(...) -> fValue

支持的调用形式：

- `ITabFile:GetFloat(nRow, nColumn, fDefault)`
- `ITabFile:GetFloat(nRow, szColumn, fDefault[, bColumnLab])`
- `ITabFile:GetFloat(szRow, szColumn, fDefault)`

失败时不返回任何值。
