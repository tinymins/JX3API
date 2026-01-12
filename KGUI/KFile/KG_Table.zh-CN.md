[English](./KG_Table.md) | 中文

# KG_Table

## 函数

* <h4 id="LuaTable_Load">Load</h4>
> KG_Table.Load(pcszFilePath, tTitle[, nMode[, bAdjust]]) -> TableFile

加载表格文件并返回 `TableFile` userdata。

- `pcszFilePath`：string。
- `tTitle`：类似数组的 table，用于描述列。每个元素都是 table，包含：
  - `t`：列标题（string）
  - `f`：类型标记（string，仅使用第一个字符）
- `nMode`（可选）：number。
- `bAdjust`（可选）：boolean。

类型标记（`f`）：

- `i`：整数
- `f`：浮点
- `b`：布尔
- `s` / `S` / `p`：字符串（从内部指针字段读取）

失败时不返回任何值。
