[English](./WndSFX.md) | 中文

# WndSFX（特效）

说明：

- `WndSFX` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

[`LoadSFX`](#LuaWndSFX_LoadSFX)
[`UnloadSFX`](#LuaWndSFX_UnloadSFX)
[`Play`](#LuaWndSFX_Play)
[`Scale`](#LuaWndSFX_SetModelScale)
[`SetModelScale`](#LuaWndSFX_SetModelScale)
[`GetModelScale`](#LuaWndSFX_GetModelScale)
[`Get3DModel`](#LuaWndSFX_Get3DModel)
[`Set2DRotation`](#LuaWndSFX_Set2DRotation)
[`SetAngle`](#LuaWndSFX_SetAngle)
[`SetYaw`](#LuaWndSFX_SetYaw)
[`SetPlaySpeed`](#LuaWndSFX_SetPlaySpeed)

* <h4 id="LuaWndSFX_LoadSFX">LoadSFX</h4>

 > (`void`) WndSFX:LoadSFX(`string` szFile[, `bool|number` bShowOnce=false])

说明：

- 参数数量只能是 1 或 2 个（不含 self）。
- `bShowOnce` 为可选参数；绑定直接用 `lua_toboolean` 读取，因此传 `0/1` 也会被当作布尔。

* <h4 id="LuaWndSFX_UnloadSFX">UnloadSFX</h4>

卸载当前已加载的特效资源。

 > (`void`) WndSFX:UnloadSFX()

* <h4 id="LuaWndSFX_Play">Play</h4>

播放已加载的特效；可选 `bLoop` 控制是否循环。

 > (`void`) WndSFX:Play([`bool` bLoop = false])

* <h4 id="LuaWndSFX_SetModelScale">SetModelScale</h4>

 > (`void`) WndSFX:SetModelScale(`number` fScale[, `any` unused])

说明：

- 参数数量允许为 1 或 2 个（不含 self），但实现只读取第 1 个参数 `fScale`；第 2 个参数会被忽略。
- `fScale` 必须是 `number` 且 `> 0`。

* <h4 id="LuaWndSFX_GetModelScale">GetModelScale</h4>

获取当前 3D 模型缩放系数。

 > (`number` fScale) WndSFX:GetModelScale()

* <h4 id="LuaWndSFX_Get3DModel">Get3DModel</h4>

获取内部的 `IKG3DModel` 对象。

 > (`IKG3DModel` Model) WndSFX:Get3DModel()

* <h4 id="LuaWndSFX_Set2DRotation">Set2DRotation</h4>

设置 2D 旋转角度。

 > (`void`) WndSFX:Set2DRotation(`number` fAngle)

* <h4 id="LuaWndSFX_SetAngle">SetAngle</h4>

设置特效角度（具体含义按底层实现）。

 > (`void`) WndSFX:SetAngle(`number` fAngle)

* <h4 id="LuaWndSFX_SetYaw">SetYaw</h4>

设置 yaw 角度。

 > (`void`) WndSFX:SetYaw(`number` fYaw)

* <h4 id="LuaWndSFX_SetPlaySpeed">SetPlaySpeed</h4>

设置播放速度。

 > (`void`) WndSFX:SetPlaySpeed(`number` fSpeed)
