[English](./Font.md) | 中文

# Font

## 函数

* <h4 id="LuaFont_SetFontOffset">SetOffset</h4>
> Font.SetOffset(nOffset)

设置全局字体的垂直偏移。

* <h4 id="LuaFont_GetFontOffset">GetOffset</h4>
> Font.GetOffset() -> nOffset

获取当前全局字体偏移。

* <h4 id="LuaFont_GetChatFontID">GetChatFontID</h4>
> Font.GetChatFontID() -> nFontID

返回聊天使用的字体 ID。

* <h4 id="LuaFont_LoadDefaultFontList">LoadDefaultFontList</h4>
> Font.LoadDefaultFontList()

加载默认字体列表。

* <h4 id="LuaFont_LoadFontList">LoadFontList</h4>
> Font.LoadFontList(pcszPath) -> bOk

从 `pcszPath` 加载字体列表。

成功返回 `true`。

* <h4 id="LuaFont_SetFont">SetFont</h4>
> Font.SetFont(dwID, pcszName, pcszPath, nSize[, tStyle]) -> bOk

定义/更新一条字体配置。

- `tStyle`（可选）：table，用布尔标记控制样式。支持键：`vertical`、`border`、`shadow`、`mipmap`。

* <h4 id="LuaFont_GetFont">GetFont</h4>
> Font.GetFont(dwID) -> pcszName, pcszPath, nSize, tStyle

获取字体配置。

- `tStyle`：包含已启用样式标记的 table。

* <h4 id="LuaFont_GetFontPathList">GetFontPathList</h4>
> Font.GetFontPathList() -> tList

返回可用的字体路径列表。

每个元素是一个 table，包含字段：`szName`、`szFile`。

* <h4 id="LuaFont_ReloadFont">ReloadFont</h4>
> Font.ReloadFont()

重新加载字体。
