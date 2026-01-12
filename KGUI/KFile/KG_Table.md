English | [中文](./KG_Table.zh-CN.md)

# KG_Table

## Functions

* <h4 id="LuaTable_Load">Load</h4>
> KG_Table.Load(pcszFilePath, tTitle[, nMode[, bAdjust]]) -> TableFile

Loads a table file and returns a `TableFile` userdata.

- `pcszFilePath`: string.
- `tTitle`: array-like table describing columns. Each element is a table with:
  - `t`: column title (string)
  - `f`: type tag (string, first character is used)
- `nMode` (optional): number.
- `bAdjust` (optional): boolean.

Type tags (`f`):

- `i`: integer
- `f`: float
- `b`: boolean
- `s` / `S` / `p`: string (reads from an internal pointer field)

Returns nothing on failure.
