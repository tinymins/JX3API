# ItemShadow

Notes:

- Some APIs using screen positions (like `AppendTriangleFanPoint`) use **unscaled UI coordinates** on Lua side; internally they are multiplied by `Station.GetUIScale()`.

[`SetShadowColor`](#LuaItemShadow_SetShadowColor)
[`GetShadowColor`](#LuaItemShadow_GetShadowColor)
[`GetColorRGB`](#LuaItemShadow_GetColorRGB)
[`SetColorRGB`](#LuaItemShadow_SetColorRGB)
[`SetD3DPT`](#LuaItemShadow_SetD3DPT)
[`SetTriangleFan`](#LuaItemShadow_SetTriangleFan)
[`IsTriangleFan`](#LuaItemShadow_IsTriangleFan)
[`AppendDoodadID`](#LuaItemShadow_AppendDoodadID)
[`AppendCharacterID`](#LuaItemShadow_AppendCharacterID)
[`AppendTriangleFanPoint`](#LuaItemShadow_AppendTriangleFanPoint)
[`AppendTriangleFan3DPoint`](#LuaItemShadow_AppendTriangleFan3DPoint)
[`ClearTriangleFanPoint`](#LuaItemShadow_ClearTriangleFanPoint)
[`IsInRegion`](#LuaItemShadow_IsInRegion)
[`SetImage`](#LuaItemShadow_SetImage)
[`SetText`](#LuaItemShadow_SetText)

* <h4 id="LuaItemShadow_SetShadowColor">SetShadowColor</h4>
Set shadow color.

Overloads:

- `SetShadowColor(dwARGB)`
- `SetShadowColor(szColorScheme)`
- `SetShadowColor(szColorScheme, nAlpha)`

 > (`void`) ItemShadow:SetShadowColor(`number` dwARGB)

 > (`void`) ItemShadow:SetShadowColor(`string` szColorScheme[, `number` nAlpha = 255])

 ````lua
 ItemShadow:SetShadowColor(0xFFFFFFFF)
 ItemShadow:SetShadowColor("Gold")
 ItemShadow:SetShadowColor("Gold", 128)
 ````

* <h4 id="LuaItemShadow_GetShadowColor">GetShadowColor</h4>
Get shadow color (ARGB).

 > (`number` dwARGB) ItemShadow:GetShadowColor()

 ````lua
 local dwARGB = ItemShadow:GetShadowColor()
 ````

* <h4 id="LuaItemShadow_SetColorRGB">SetColorRGB</h4>
Set shadow RGB (keeps current alpha).

 > (`void`) ItemShadow:SetColorRGB(`number` r, `number` g, `number` b)

 ````lua
 ItemShadow:SetColorRGB(255, 255, 255)
 ````

* <h4 id="LuaItemShadow_GetColorRGB">GetColorRGB</h4>
Get shadow RGB.

 > (`number` r, `number` g, `number` b) ItemShadow:GetColorRGB()

 ````lua
 local r, g, b = ItemShadow:GetColorRGB()
 ````

* <h4 id="LuaItemShadow_SetD3DPT">SetD3DPT</h4>
Set D3D primitive type.

 > (`void`) ItemShadow:SetD3DPT(`number` nD3DPT)

 ````lua
 ItemShadow:SetD3DPT(0)
 ````

* <h4 id="LuaItemShadow_SetTriangleFan">SetTriangleFan</h4>
Enable/disable triangle fan mode.

 > (`void`) ItemShadow:SetTriangleFan(`bool|number` nGType[, `number` nBold])

 ````lua
 ItemShadow:SetTriangleFan(true)
 ItemShadow:SetTriangleFan(1, 2)
 ````

* <h4 id="LuaItemShadow_IsTriangleFan">IsTriangleFan</h4>
Check whether triangle fan mode is enabled.

 > (`bool` bTriangleFan) ItemShadow:IsTriangleFan()

 ````lua
 local bTriangleFan = ItemShadow:IsTriangleFan()
 ````

* <h4 id="LuaItemShadow_AppendDoodadID">AppendDoodadID</h4>
Append doodad id.

`deltaOrYDelta` can be:

- `number`: treated as `YDelta`
- `table`: `{xDelta, yDelta, zDelta, screenXDelta, screenYDelta}` (1-based indices)

 > (`void`) ItemShadow:AppendDoodadID(`number` dwDoodadID, `number` r, `number` g, `number` b, `number` a[, `number|table` deltaOrYDelta[, `number` dwFontID[, `string` szText[, `number` fSpacing[, `number` fFontScale]]]]])

 ````lua
 ItemShadow:AppendDoodadID(1, 255, 255, 255, 255)
 ItemShadow:AppendDoodadID(1, 255, 255, 255, 255, {0, 0, 0, 0, 0}, 0, "text")
 ````

* <h4 id="LuaItemShadow_AppendCharacterID">AppendCharacterID</h4>
Append character id.

`nPosType` can be boolean or number.

`deltaOrYDelta` format is the same as [`AppendDoodadID`](#LuaItemShadow_AppendDoodadID).

 > (`void`) ItemShadow:AppendCharacterID(`number` dwCharacterID, `bool|number` nPosType, `number` r, `number` g, `number` b, `number` a[, `number|table` deltaOrYDelta[, `number` dwFontID[, `string` szText[, `number` fSpacing[, `number` fFontScale]]]]])

 ````lua
 ItemShadow:AppendCharacterID(1, 0, 255, 255, 255, 255)
 ````

* <h4 id="LuaItemShadow_AppendTriangleFanPoint">AppendTriangleFanPoint</h4>
Append a 2D point (UI position).

`x`/`y` are unscaled values on Lua side; internally they are multiplied by UIScale.

 > (`void`) ItemShadow:AppendTriangleFanPoint(`number` x, `number` y, `number` r, `number` g, `number` b, `number` a[, `number` dwFontID[, `string` szText[, `number` fSpacing[, `number` fFontScale]]]])

 ````lua
 ItemShadow:AppendTriangleFanPoint(100, 100, 255, 255, 255, 255)
 ````

* <h4 id="LuaItemShadow_AppendTriangleFan3DPoint">AppendTriangleFan3DPoint</h4>
Append a 3D point (game world position) to triangle fan.

`deltaOrYDelta` format is the same as [`AppendDoodadID`](#LuaItemShadow_AppendDoodadID).

 > (`void`) ItemShadow:AppendTriangleFan3DPoint(`number` x, `number` y, `number` z, `number` r, `number` g, `number` b, `number` a[, `number|table` deltaOrYDelta[, `number` dwFontID[, `string` szText[, `number` fSpacing[, `number` fFontScale]]]]])

 ````lua
 ItemShadow:AppendTriangleFan3DPoint(0, 0, 0, 255, 255, 255, 255)
 ````

* <h4 id="LuaItemShadow_ClearTriangleFanPoint">ClearTriangleFanPoint</h4>
Clear all triangle fan points.

 > (`void`) ItemShadow:ClearTriangleFanPoint()

 ````lua
 ItemShadow:ClearTriangleFanPoint()
 ````

* <h4 id="LuaItemShadow_IsInRegion">IsInRegion</h4>
Test if point is in region.

 > (`bool` bInRegion) ItemShadow:IsInRegion(`number` x, `number` y)

 ````lua
 local bInRegion = ItemShadow:IsInRegion(100, 100)
 ````

* <h4 id="LuaItemShadow_SetImage">SetImage</h4>
Set shadow image.

 > (`bool` bResult) ItemShadow:SetImage(`number` dwCharacterID, `string` szFilePath, `number` dwFrame, `number` fOffsetX, `number` fOffsetY, `number` fW, `number` fH, `number` dwPosType, `bool` bGray)

 ````lua
 local bOk = ItemShadow:SetImage(1, "interface/ui/image/tex.tga", 0, 0, 0, 64, 64, 0, false)
 ````

* <h4 id="LuaItemShadow_SetText">SetText</h4>
Set shadow text.

 > (`bool` bResult) ItemShadow:SetText(`string` szText, `number` dwFontID, `number` r, `number` g, `number` b, `number` a)

 ````lua
 local bOk = ItemShadow:SetText("hello", 0, 255, 255, 255, 255)
 ````
