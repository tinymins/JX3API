# WndContainer

Notes:

- `WndContainer` inherits all methods from `WndWindow`; only additional methods are listed here.

[`SetContainerType`](#LuaContainer_SetContainerType)
[`FormatAllContentPos`](#LuaContainer_FormatAllContentPos)
[`GetAllContentSize`](#LuaContainer_GetAllContentSize)
[`AppendContentFromIni`](#LuaContainer_AppendContentFromIni)
[`Clear`](#LuaContainer_Clear)
[`GetAllContentCount`](#LuaContainer_GetAllContentCount)
[`SetColumn`](#LuaContainer_SetColumn)
[`SetDrawStyle`](#LuaContainer_SetDrawStyle)
[`LookupContent`](#LuaContainer_LookupContent)
[`SetStartRelPos`](#LuaContainer_SetStartRelPos)
[`GetStartRelPos`](#LuaContainer_GetStartRelPos)
[`SetVAlign`](#LuaContainer_SetVAlign)
[`GetVAlign`](#LuaContainer_GetVAlign)
[`SetHAlign`](#LuaContainer_SetHAlign)
[`GetHAlign`](#LuaContainer_GetHAlign)
[`LoadShapTexture`](#LuaContainer_LoadShapTexture)
[`UnloadShapTexture`](#LuaContainer_UnloadShapTexture)

* <h4 id="LuaContainer_SetContainerType">SetContainerType</h4>

Sets the container layout/type.

 > (`void`) WndContainer:SetContainerType(`number` nType)

* <h4 id="LuaContainer_FormatAllContentPos">FormatAllContentPos</h4>

Reformats/reflows all child content positions. Optional `bNotifyLua` controls whether Lua is notified.

 > (`void`) WndContainer:FormatAllContentPos([`bool|number` bNotifyLua = false])

* <h4 id="LuaContainer_GetAllContentSize">GetAllContentSize</h4>

Gets the total content size (width/height).

 > (`number` w, `number` h) WndContainer:GetAllContentSize()

* <h4 id="LuaContainer_AppendContentFromIni">AppendContentFromIni</h4>

Appends content defined in an ini section, optionally renaming and enabling caching.

 > (`WndWindow` Content) WndContainer:AppendContentFromIni(`string` szIniFile, `string` szSectionName[, `string` szNewName[, `bool|number` bEnableCache]])

* <h4 id="LuaContainer_Clear">Clear</h4>

Clears all content from the container.

 > (`void`) WndContainer:Clear()

* <h4 id="LuaContainer_GetAllContentCount">GetAllContentCount</h4>

Gets the number of content items.

 > (`number` nCount) WndContainer:GetAllContentCount()

* <h4 id="LuaContainer_SetColumn">SetColumn</h4>

Enables or disables column layout.

 > (`void`) WndContainer:SetColumn(`bool|number` bColumn)

* <h4 id="LuaContainer_SetDrawStyle">SetDrawStyle</h4>

Sets draw style flags.

 > (`void`) WndContainer:SetDrawStyle(`number` dwStyle)

* <h4 id="LuaContainer_LookupContent">LookupContent</h4>

Looks up a content window by index.

 > (`WndWindow` Content) WndContainer:LookupContent(`number` nIndex)

* <h4 id="LuaContainer_SetStartRelPos">SetStartRelPos</h4>

Sets the start relative position for laying out content.

 > (`void`) WndContainer:SetStartRelPos(`number` x, `number` y)

* <h4 id="LuaContainer_GetStartRelPos">GetStartRelPos</h4>

Gets the start relative position for laying out content.

 > (`number` x, `number` y) WndContainer:GetStartRelPos()

* <h4 id="LuaContainer_SetVAlign">SetVAlign</h4>

Sets vertical alignment. `nReserved` is reserved by the underlying UI implementation.

 > (`void`) WndContainer:SetVAlign(`number` nValign, `number` nReserved)

* <h4 id="LuaContainer_GetVAlign">GetVAlign</h4>

Gets vertical alignment.

 > (`number` nValign) WndContainer:GetVAlign()

* <h4 id="LuaContainer_SetHAlign">SetHAlign</h4>

Sets horizontal alignment. `nReserved` is reserved by the underlying UI implementation.

 > (`void`) WndContainer:SetHAlign(`number` nHalign, `number` nReserved)

* <h4 id="LuaContainer_GetHAlign">GetHAlign</h4>

Gets horizontal alignment.

 > (`number` nHalign) WndContainer:GetHAlign()

* <h4 id="LuaContainer_LoadShapTexture">LoadShapTexture</h4>

Loads a shape texture resource for the container.

 > (`void`) WndContainer:LoadShapTexture(`string` szFile)

* <h4 id="LuaContainer_UnloadShapTexture">UnloadShapTexture</h4>

Unloads the shape texture resource.

 > (`void`) WndContainer:UnloadShapTexture()
