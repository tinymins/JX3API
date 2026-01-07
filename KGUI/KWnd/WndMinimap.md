# WndMinimap

Notes:

- `WndMinimap` inherits all methods from `WndWindow`; only additional methods are listed here.

[`SetMapPath`](#LuaMinimap_SetMapPath)
[`SetScale`](#LuaMinimap_SetScale)
[`GetScale`](#LuaMinimap_GetScale)
[`GetPointCount`](#LuaMinimap_GetPointCount)
[`UpdataStaticPoint`](#LuaMinimap_UpdateStaticPoint)
[`UpdataAnimatePoint`](#LuaMinimap_UpdateAnimatePoint)
[`UpdataArrowPoint`](#LuaMinimap_UpdateArrowPoint)
[`UpdateRegion`](#LuaMinimap_UpdateRegion)
[`RemovePoint`](#LuaMinimap_RemovePoint)
[`UpdataSelfPos`](#LuaMinimap_UpdateSelfPos)
[`Clear`](#LuaMinimap_Clear)
[`GetOverObj`](#LuaMinimap_GetOverObj)
[`GetSendPos`](#LuaMinimap_GetSendPos)

* <h4 id="LuaMinimap_SetMapPath">SetMapPath</h4>

Sets the minimap map resource/path.

 > (`void`) WndMinimap:SetMapPath(`string` szPath)

* <h4 id="LuaMinimap_SetScale">SetScale</h4>

Sets the minimap scale factor.

 > (`void`) WndMinimap:SetScale(`number` fScale)

* <h4 id="LuaMinimap_GetScale">GetScale</h4>

Gets the current minimap scale factor.

 > (`number` fScale) WndMinimap:GetScale()

* <h4 id="LuaMinimap_GetPointCount">GetPointCount</h4>

Gets the number of points currently managed by the minimap.

 > (`number` nCount) WndMinimap:GetPointCount()

* <h4 id="LuaMinimap_UpdateStaticPoint">UpdataStaticPoint</h4>

Updates/creates a static point. Optional `fX/fY` specify the point position.

 > (`void`) WndMinimap:UpdataStaticPoint(`number` dwType, `number` dwID, `number` nFrame[, `number` fX, `number` fY[, `number` nLeftCount[, `number` nOutOfFrame[, `number` fScale]]]])

* <h4 id="LuaMinimap_UpdateAnimatePoint">UpdataAnimatePoint</h4>

Updates/creates an animated point. Optional `fX/fY` specify the point position.

 > (`void`) WndMinimap:UpdataAnimatePoint(`number` dwType, `number` dwID, `number` nGroup[, `number` fX, `number` fY[, `number` nLeftCount[, `number` fScale]]])

* <h4 id="LuaMinimap_UpdateArrowPoint">UpdataArrowPoint</h4>

Updates/creates an arrow point. Optional `fX/fY` specify the point position.

 > (`void`) WndMinimap:UpdataArrowPoint(`number` dwType, `number` dwID, `number` nFrame, `number` nArrowFrame[, `number` fX, `number` fY[, `number` nLeftCount[, `number` fScale]]])

* <h4 id="LuaMinimap_UpdateRegion">UpdateRegion</h4>

Updates/creates a region polygon/line based on vertex and color tables.

 > (`void`) WndMinimap:UpdateRegion(`number` dwType, `number` dwID, `table` tVertexs[, `table` tColor[, `table` tLineColor[, `number` nBlod=1[, `number` nLeftCount[, `number` nOutOfFrame]]]]])

* <h4 id="LuaMinimap_RemovePoint">RemovePoint</h4>

Removes points by type, or by type + id.

 > (`void`) WndMinimap:RemovePoint(`number` dwType[, `number` dwID])

* <h4 id="LuaMinimap_UpdateSelfPos">UpdataSelfPos</h4>

Updates the player's/self position and direction on the minimap.

 > (`void`) WndMinimap:UpdataSelfPos(`number` nLayer, `number` fX, `number` fY, `number` fDirection)

* <h4 id="LuaMinimap_Clear">Clear</h4>

Clears minimap points/regions.

 > (`void`) WndMinimap:Clear()

* <h4 id="LuaMinimap_GetOverObj">GetOverObj</h4>

Gets the object currently under the cursor (type and id).

 > (`number` nObjType, `number` nObjID) WndMinimap:GetOverObj()

* <h4 id="LuaMinimap_GetSendPos">GetSendPos</h4>

Gets the position used for sending/interaction (as reported by the minimap).

 > (`number` x, `number` y) WndMinimap:GetSendPos()
