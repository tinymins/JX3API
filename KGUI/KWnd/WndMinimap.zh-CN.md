[English](./WndMinimap.md) | 中文

# WndMinimap（小地图）

说明：

- `WndMinimap` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

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

设置小地图对应的地图资源/路径。

 > (`void`) WndMinimap:SetMapPath(`string` szPath)

* <h4 id="LuaMinimap_SetScale">SetScale</h4>

设置小地图缩放系数。

 > (`void`) WndMinimap:SetScale(`number` fScale)

* <h4 id="LuaMinimap_GetScale">GetScale</h4>

获取当前小地图缩放系数。

 > (`number` fScale) WndMinimap:GetScale()

* <h4 id="LuaMinimap_GetPointCount">GetPointCount</h4>

获取当前小地图点的数量。

 > (`number` nCount) WndMinimap:GetPointCount()

* <h4 id="LuaMinimap_UpdateStaticPoint">UpdataStaticPoint</h4>

 > (`void`) WndMinimap:UpdataStaticPoint(`number` dwType, `number` dwID, `number` nFrame[, `number` fX, `number` fY[, `number` nLeftCount[, `number` nOutOfFrame[, `number` fScale]]]])

说明：

- 必填参数为 `dwType`、`dwID`、`nFrame`（不含 self）。
- 可选 `fX`、`fY` 用于指定点的位置；未提供时，底层使用默认值（实现中初值为 -10000）。
- 可选 `nLeftCount`、`nOutOfFrame`、`fScale` 会原样传给底层更新逻辑。

* <h4 id="LuaMinimap_UpdateAnimatePoint">UpdataAnimatePoint</h4>

 > (`void`) WndMinimap:UpdataAnimatePoint(`number` dwType, `number` dwID, `number` nGroup[, `number` fX, `number` fY[, `number` nLeftCount[, `number` fScale]]])

说明：

- 必填参数为 `dwType`、`dwID`、`nGroup`。
- 可选 `fX`、`fY` 指定位置；可选 `nLeftCount`、`fScale` 控制显示/缩放等行为（按底层实现处理）。

* <h4 id="LuaMinimap_UpdateArrowPoint">UpdataArrowPoint</h4>

 > (`void`) WndMinimap:UpdataArrowPoint(`number` dwType, `number` dwID, `number` nFrame, `number` nArrowFrame[, `number` fX, `number` fY[, `number` nLeftCount[, `number` fScale]]])

说明：

- 必填参数为 `dwType`、`dwID`、`nFrame`、`nArrowFrame`。
- 可选 `fX`、`fY` 指定位置；可选 `nLeftCount`、`fScale` 传给底层更新逻辑。

* <h4 id="LuaMinimap_UpdateRegion">UpdateRegion</h4>

 > (`void`) WndMinimap:UpdateRegion(`number` dwType, `number` dwID, `table` tVertexs[, `table` tColor[, `table` tLineColor[, `number` nBlod=1[, `number` nLeftCount[, `number` nOutOfFrame]]]]])

说明：

- `tVertexs` 为顶点数组；每个元素是一个 table，形如 `{x, y}`（实现中读取索引 1/2）。
- `tColor` / `tLineColor` 为颜色 table，按索引 1..4 读取 RGBA。
- `nBlod` 为线条粗细（默认 1）。
- 可选 `nLeftCount`、`nOutOfFrame` 会原样传给底层区域更新逻辑。

* <h4 id="LuaMinimap_RemovePoint">RemovePoint</h4>

 > (`void`) WndMinimap:RemovePoint(`number` dwType[, `number` dwID])

说明：

- 仅传 `dwType` 时移除该类型下的点。
- 同时传 `dwType`、`dwID` 时移除指定点。

* <h4 id="LuaMinimap_UpdateSelfPos">UpdataSelfPos</h4>

 > (`void`) WndMinimap:UpdataSelfPos(`number` nLayer, `number` fX, `number` fY, `number` fDirection)

说明：

- 更新自身位置与朝向；参数数量必须严格为 4 个（不含 self）。

* <h4 id="LuaMinimap_Clear">Clear</h4>

清空小地图上的点/区域等内容。

 > (`void`) WndMinimap:Clear()

* <h4 id="LuaMinimap_GetOverObj">GetOverObj</h4>

获取鼠标当前悬停的对象（类型与 ID）。

 > (`number` nObjType, `number` nObjID) WndMinimap:GetOverObj()

* <h4 id="LuaMinimap_GetSendPos">GetSendPos</h4>

获取小地图用于交互/发送的坐标（由控件当前状态决定）。

 > (`number` x, `number` y) WndMinimap:GetSendPos()
