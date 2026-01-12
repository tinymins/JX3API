[English](./Table.md) | 中文

# 表格函数

表格文件操作相关函数。

## 函数

[`KG_Table.Load`](#KG_Table_Load)
[`Tab_IniFile`](#Tab_IniFile)
[`Tab_LoadData`](#Tab_LoadData)
[`OpenIniFile`](#OpenIniFile)
[`OpenTabFile`](#OpenTabFile)

---

* <h4 id="KG_Table_Load">KG_Table.Load</h4>

加载表格文件。

 > ([`KG_Table`](../KFile/KG_Table.zh-CN.md) table) KG_Table.Load(`string` szFile)

另见：[KFile/KG_Table](../KFile/KG_Table.zh-CN.md)

* <h4 id="Tab_IniFile">Tab_IniFile</h4>

打开 INI 文件以读取。

 > (`KIniFile` iniFile) Tab_IniFile(`string` szFile)

* <h4 id="Tab_LoadData">Tab_LoadData</h4>

从表格文件加载数据。

 > (`table` tData) Tab_LoadData(`string` szFile, `string` szSection)

* <h4 id="OpenIniFile">OpenIniFile</h4>

打开 INI 文件。

 > (`KIniFile` iniFile) OpenIniFile(`string` szFile)

* <h4 id="OpenTabFile">OpenTabFile</h4>

打开 Tab 文件。

 > ([`ITabFile`](../KFile/ITabFile.zh-CN.md) tabFile) OpenTabFile(`string` szFile)

另见：[KFile](../KFile/index.zh-CN.md) 了解文件操作。
