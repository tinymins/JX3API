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

 > (`void`) WndContainer:SetContainerType(`number` nType)

* <h4 id="LuaContainer_FormatAllContentPos">FormatAllContentPos</h4>

 > (`void`) WndContainer:FormatAllContentPos()

* <h4 id="LuaContainer_GetAllContentSize">GetAllContentSize</h4>

 > (`number` w, `number` h) WndContainer:GetAllContentSize()

* <h4 id="LuaContainer_AppendContentFromIni">AppendContentFromIni</h4>

 > (`WndWindow` Content) WndContainer:AppendContentFromIni(`string` szIniFile, `string` szSectionName[, `string` szNewName])

* <h4 id="LuaContainer_Clear">Clear</h4>

 > (`void`) WndContainer:Clear()

* <h4 id="LuaContainer_GetAllContentCount">GetAllContentCount</h4>

 > (`number` nCount) WndContainer:GetAllContentCount()

* <h4 id="LuaContainer_SetColumn">SetColumn</h4>

 > (`void`) WndContainer:SetColumn(`number` nColumn)

* <h4 id="LuaContainer_SetDrawStyle">SetDrawStyle</h4>

 > (`void`) WndContainer:SetDrawStyle(`number` dwStyle)

* <h4 id="LuaContainer_LookupContent">LookupContent</h4>

 > (`WndWindow` Content) WndContainer:LookupContent(`number|string` ref)

* <h4 id="LuaContainer_SetStartRelPos">SetStartRelPos</h4>

 > (`void`) WndContainer:SetStartRelPos(`number` x, `number` y)

* <h4 id="LuaContainer_GetStartRelPos">GetStartRelPos</h4>

 > (`number` x, `number` y) WndContainer:GetStartRelPos()

* <h4 id="LuaContainer_SetVAlign">SetVAlign</h4>

 > (`void`) WndContainer:SetVAlign(`number` nValign)

* <h4 id="LuaContainer_GetVAlign">GetVAlign</h4>

 > (`number` nValign) WndContainer:GetVAlign()

* <h4 id="LuaContainer_SetHAlign">SetHAlign</h4>

 > (`void`) WndContainer:SetHAlign(`number` nHalign)

* <h4 id="LuaContainer_GetHAlign">GetHAlign</h4>

 > (`number` nHalign) WndContainer:GetHAlign()

* <h4 id="LuaContainer_LoadShapTexture">LoadShapTexture</h4>

 > (`void`) WndContainer:LoadShapTexture(`string` szFile)

* <h4 id="LuaContainer_UnloadShapTexture">UnloadShapTexture</h4>

 > (`void`) WndContainer:UnloadShapTexture()
