[English](./ItemShadow.md) | 中文

# ItemShadow（阴影）

说明：

- `AppendTriangleFanPoint` 的 `x`/`y` 在 Lua 侧为**未缩放的 UI 坐标**；内部会乘以 `Station.GetUIScale()`。

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
设置阴影 颜色。

当参数为 `string` 时，会将 `szColorScheme` 按当前代码页转换后用于查找配色方案；若不存在该配色项，则颜色默认为 0，再叠加 alpha。

重载：

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
获取阴影 颜色 (ARGB)。

 > (`number` dwARGB) ItemShadow:GetShadowColor()

 ````lua
 local dwARGB = ItemShadow:GetShadowColor()
 ````

* <h4 id="LuaItemShadow_SetColorRGB">SetColorRGB</h4>
设置阴影 RGB（保持当前透明度不变）。

 > (`void`) ItemShadow:SetColorRGB(`number` r, `number` g, `number` b)

 ````lua
 ItemShadow:SetColorRGB(255, 255, 255)
 ````

* <h4 id="LuaItemShadow_GetColorRGB">GetColorRGB</h4>
获取阴影 RGB。

 > (`number` r, `number` g, `number` b) ItemShadow:GetColorRGB()

 ````lua
 local r, g, b = ItemShadow:GetColorRGB()
 ````

* <h4 id="LuaItemShadow_SetD3DPT">SetD3DPT</h4>
设置D3D primitive 类型。

 > (`void`) ItemShadow:SetD3DPT(`number` nD3DPT)

 ````lua
 ItemShadow:SetD3DPT(0)
 ````

* <h4 id="LuaItemShadow_SetTriangleFan">SetTriangleFan</h4>
启用/禁用triangle fan mode。

 > (`void`) ItemShadow:SetTriangleFan(`bool|number` nGType[, `number` nBold])

 ````lua
 ItemShadow:SetTriangleFan(true)
 ItemShadow:SetTriangleFan(1, 2)
 ````

* <h4 id="LuaItemShadow_IsTriangleFan">IsTriangleFan</h4>
检查是否启用了 triangle fan mode。

 > (`bool` bTriangleFan) ItemShadow:IsTriangleFan()

 ````lua
 local bTriangleFan = ItemShadow:IsTriangleFan()
 ````

* <h4 id="LuaItemShadow_AppendDoodadID">AppendDoodadID</h4>
追加 doodad ID。

`deltaOrYDelta` 可以是：

- `number`：作为 `YDelta`
- `table`：`{xDelta, yDelta, zDelta, screenXDelta, screenYDelta}`（Lua 下标从 1 开始）

 > (`void`) ItemShadow:AppendDoodadID(`number` dwDoodadID, `number` r, `number` g, `number` b, `number` a[, `number|table` deltaOrYDelta[, `number` dwFontID[, `string` szText[, `number` fSpacing[, `number` fFontScale]]]]])

 ````lua
 ItemShadow:AppendDoodadID(1, 255, 255, 255, 255)
 ItemShadow:AppendDoodadID(1, 255, 255, 255, 255, {0, 0, 0, 0, 0}, 0, "text")
 ````

* <h4 id="LuaItemShadow_AppendCharacterID">AppendCharacterID</h4>
追加角色 ID。

`nPosType` 可以是布尔值或数字。

`deltaOrYDelta` 的格式与 [`AppendDoodadID`](#LuaItemShadow_AppendDoodadID) 相同。

 > (`void`) ItemShadow:AppendCharacterID(`number` dwCharacterID, `bool|number` nPosType, `number` r, `number` g, `number` b, `number` a[, `number|table` deltaOrYDelta[, `number` dwFontID[, `string` szText[, `number` fSpacing[, `number` fFontScale]]]]])

 ````lua
 ItemShadow:AppendCharacterID(1, 0, 255, 255, 255, 255)
 ````

* <h4 id="LuaItemShadow_AppendTriangleFanPoint">AppendTriangleFanPoint</h4>
追加一个 2D 点（UI 坐标）。

`x`/`y` 在 Lua 侧为未缩放值；内部会乘以 UIScale。

 > (`void`) ItemShadow:AppendTriangleFanPoint(`number` x, `number` y, `number` r, `number` g, `number` b, `number` a[, `number` dwFontID[, `string` szText[, `number` fSpacing[, `number` fFontScale]]]])

 ````lua
 ItemShadow:AppendTriangleFanPoint(100, 100, 255, 255, 255, 255)
 ````

* <h4 id="LuaItemShadow_AppendTriangleFan3DPoint">AppendTriangleFan3DPoint</h4>
向 triangle fan 追加一个 3D 点（游戏世界坐标）。

内部会把游戏世界坐标转换为场景坐标后再使用。

`deltaOrYDelta` 的格式与 [`AppendDoodadID`](#LuaItemShadow_AppendDoodadID) 相同。

 > (`void`) ItemShadow:AppendTriangleFan3DPoint(`number` x, `number` y, `number` z, `number` r, `number` g, `number` b, `number` a[, `number|table` deltaOrYDelta[, `number` dwFontID[, `string` szText[, `number` fSpacing[, `number` fFontScale]]]]])

 ````lua
 ItemShadow:AppendTriangleFan3DPoint(0, 0, 0, 255, 255, 255, 255)
 ````

* <h4 id="LuaItemShadow_ClearTriangleFanPoint">ClearTriangleFanPoint</h4>
清除所有 triangle fan 点。

 > (`void`) ItemShadow:ClearTriangleFanPoint()

 ````lua
 ItemShadow:ClearTriangleFanPoint()
 ````

* <h4 id="LuaItemShadow_IsInRegion">IsInRegion</h4>
测试点是否位于区域内。

 > (`bool` bInRegion) ItemShadow:IsInRegion(`number` x, `number` y)

 ````lua
 local bInRegion = ItemShadow:IsInRegion(100, 100)
 ````

* <h4 id="LuaItemShadow_SetImage">SetImage</h4>
设置阴影 图片。

`szFilePath` 会经过 `FormatFilePath()` 处理后再传入底层。

成功时返回值恒为 `true`；如果参数不合法/内部报错，会报错且不返回值。

 > (`bool` bResult) ItemShadow:SetImage(`number` dwCharacterID, `string` szFilePath, `number` dwFrame, `number` fOffsetX, `number` fOffsetY, `number` fW, `number` fH, `number` dwPosType, `bool` bGray)

 ````lua
 local bOk = ItemShadow:SetImage(1, "interface/ui/image/tex.tga", 0, 0, 0, 64, 64, 0, false)
 ````

* <h4 id="LuaItemShadow_SetText">SetText</h4>
设置阴影 text。

`szText` 会按当前代码页转换为宽字符串后传入底层。

成功时返回值恒为 `true`；如果参数不合法/内部报错，会报错且不返回值。

 > (`bool` bResult) ItemShadow:SetText(`string` szText, `number` dwFontID, `number` r, `number` g, `number` b, `number` a)

 ````lua
 local bOk = ItemShadow:SetText("hello", 0, 255, 255, 255, 255)
 ````
