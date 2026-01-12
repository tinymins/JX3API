English | [中文](./ITabFile.zh-CN.md)

# ITabFile

## Methods

* <h4 id="LuaTab_Save">Save</h4>
> ITabFile:Save(pcszFileName)

Saves this tab file.

* <h4 id="LuaTab_Close">Close</h4>
> ITabFile:Close()

Releases this `ITabFile` userdata.

* <h4 id="LuaTab_FindColumn">FindColumn</h4>
> ITabFile:FindColumn(szColumn) -> nColumn

Finds a column by name.

Returns nothing on failure.

* <h4 id="LuaTab_GetWidth">GetWidth</h4>
> ITabFile:GetWidth() -> nWidth

Returns the number of columns.

* <h4 id="LuaTab_GetHeight">GetHeight</h4>
> ITabFile:GetHeight() -> nHeight

Returns the number of rows.

* <h4 id="LuaTab_GetString">GetString</h4>
> ITabFile:GetString(...) -> szValue

Supported call patterns:

- `ITabFile:GetString(nRow, nColumn, szDefault)`
- `ITabFile:GetString(nRow, szColumn, szDefault[, bColumnLab])`
- `ITabFile:GetString(szRow, szColumn, szDefault)`

* <h4 id="LuaTab_GetInteger">GetInteger</h4>
> ITabFile:GetInteger(...) -> nValue

Supported call patterns:

- `ITabFile:GetInteger(nRow, nColumn, nDefault)`
- `ITabFile:GetInteger(nRow, szColumn, nDefault[, bColumnLab])`
- `ITabFile:GetInteger(szRow, szColumn, nDefault)`

Returns nothing on failure.

* <h4 id="LuaTab_GetFloat">GetFloat</h4>
> ITabFile:GetFloat(...) -> fValue

Supported call patterns:

- `ITabFile:GetFloat(nRow, nColumn, fDefault)`
- `ITabFile:GetFloat(nRow, szColumn, fDefault[, bColumnLab])`
- `ITabFile:GetFloat(szRow, szColumn, fDefault)`

Returns nothing on failure.
