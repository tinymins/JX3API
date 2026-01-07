# WndSFX

Notes:

- `WndSFX` inherits all methods from `WndWindow`; only additional methods are listed here.

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

Loads a special effect resource into this window.

 > (`void`) WndSFX:LoadSFX(`string` szFile[, `bool|number` bShowOnce=false])

* <h4 id="LuaWndSFX_UnloadSFX">UnloadSFX</h4>

Unloads the currently loaded special effect.

 > (`void`) WndSFX:UnloadSFX()

* <h4 id="LuaWndSFX_Play">Play</h4>

Plays the loaded effect. Optional `bLoop` controls looping.

 > (`void`) WndSFX:Play([`bool` bLoop = false])

* <h4 id="LuaWndSFX_SetModelScale">SetModelScale</h4>

Sets the 3D model scale. The binding allows an extra unused argument.

 > (`void`) WndSFX:SetModelScale(`number` fScale[, `any` unused])

* <h4 id="LuaWndSFX_GetModelScale">GetModelScale</h4>

Gets the current 3D model scale.

 > (`number` fScale) WndSFX:GetModelScale()

* <h4 id="LuaWndSFX_Get3DModel">Get3DModel</h4>

Gets the underlying `IKG3DModel` object.

 > (`IKG3DModel` Model) WndSFX:Get3DModel()

* <h4 id="LuaWndSFX_Set2DRotation">Set2DRotation</h4>

Sets the 2D rotation angle.

 > (`void`) WndSFX:Set2DRotation(`number` fAngle)

* <h4 id="LuaWndSFX_SetAngle">SetAngle</h4>

Sets the 3D angle.

 > (`void`) WndSFX:SetAngle(`number` fAngle)

* <h4 id="LuaWndSFX_SetYaw">SetYaw</h4>

Sets the yaw angle.

 > (`void`) WndSFX:SetYaw(`number` fYaw)

* <h4 id="LuaWndSFX_SetPlaySpeed">SetPlaySpeed</h4>

Sets the playback speed.

 > (`void`) WndSFX:SetPlaySpeed(`number` fSpeed)
