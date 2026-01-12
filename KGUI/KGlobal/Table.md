English | [中文](./Table.zh-CN.md)

# Table Functions

Functions for table file operations.

## Functions

[`KG_Table.Load`](#KG_Table_Load)
[`Tab_IniFile`](#Tab_IniFile)
[`Tab_LoadData`](#Tab_LoadData)
[`OpenIniFile`](#OpenIniFile)
[`OpenTabFile`](#OpenTabFile)

---

* <h4 id="KG_Table_Load">KG_Table.Load</h4>

Loads a table file.

 > ([`KG_Table`](../KFile/KG_Table.md) table) KG_Table.Load(`string` szFile)

See also: [KFile/KG_Table](../KFile/KG_Table.md)

* <h4 id="Tab_IniFile">Tab_IniFile</h4>

Opens an INI file for reading.

 > (`KIniFile` iniFile) Tab_IniFile(`string` szFile)

* <h4 id="Tab_LoadData">Tab_LoadData</h4>

Loads data from a table file.

 > (`table` tData) Tab_LoadData(`string` szFile, `string` szSection)

* <h4 id="OpenIniFile">OpenIniFile</h4>

Opens an INI file.

 > (`KIniFile` iniFile) OpenIniFile(`string` szFile)

* <h4 id="OpenTabFile">OpenTabFile</h4>

Opens a Tab file.

 > ([`ITabFile`](../KFile/ITabFile.md) tabFile) OpenTabFile(`string` szFile)

See also: [KFile](../KFile/index.md) for file operations.
