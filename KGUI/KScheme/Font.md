English | [中文](./Font.zh-CN.md)

# Font

## Functions

* <h4 id="LuaFont_SetFontOffset">SetOffset</h4>
> Font.SetOffset(nOffset)

Sets the global font vertical offset.

* <h4 id="LuaFont_GetFontOffset">GetOffset</h4>
> Font.GetOffset() -> nOffset

Gets the current global font offset.

* <h4 id="LuaFont_GetChatFontID">GetChatFontID</h4>
> Font.GetChatFontID() -> nFontID

Returns the font ID used for chat.

* <h4 id="LuaFont_LoadDefaultFontList">LoadDefaultFontList</h4>
> Font.LoadDefaultFontList()

Loads the default font list.

* <h4 id="LuaFont_LoadFontList">LoadFontList</h4>
> Font.LoadFontList(pcszPath) -> bOk

Loads a font list from `pcszPath`.

Returns `true` on success.

* <h4 id="LuaFont_SetFont">SetFont</h4>
> Font.SetFont(dwID, pcszName, pcszPath, nSize[, tStyle]) -> bOk

Defines/updates a font entry.

- `tStyle` (optional): table of boolean flags. Supported keys: `vertical`, `border`, `shadow`, `mipmap`.

* <h4 id="LuaFont_GetFont">GetFont</h4>
> Font.GetFont(dwID) -> pcszName, pcszPath, nSize, tStyle

Gets a font entry.

- `tStyle`: a table containing the enabled style flags.

* <h4 id="LuaFont_GetFontPathList">GetFontPathList</h4>
> Font.GetFontPathList() -> tList

Returns a list of available font paths.

Each element is a table with fields: `szName`, `szFile`.

* <h4 id="LuaFont_ReloadFont">ReloadFont</h4>
> Font.ReloadFont()

Reloads fonts.
