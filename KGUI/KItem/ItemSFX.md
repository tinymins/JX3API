# ItemSFX

[`LoadSFX`](#LuaItemSFX_LoadSFX)
[`UnloadSFX`](#LuaItemSFX_UnloadSFX)
[`Play`](#LuaItemSFX_Play)
[`SetModelScale`](#LuaItemSFX_SetModelScale)
[`GetModelScale`](#LuaItemSFX_GetModelScale)
[`Get3DModel`](#LuaItemSFX_Get3DModel)
[`Set2DRotation`](#LuaItemSFX_Set2DRotation)
[`SetAngle`](#LuaItemSFX_SetAngle)
[`SetYaw`](#LuaItemSFX_SetYaw)
[`SetPlaySpeed`](#LuaItemSFX_SetPlaySpeed)

* <h4 id="LuaItemSFX_LoadSFX">LoadSFX</h4>
Load SFX model.

 > (`void`) ItemSFX:LoadSFX(`string` szFile[, `bool` bShowOnce = false])

 ````lua
 ItemSFX:LoadSFX("interface/ui/sfx/a.sfx")
 ItemSFX:LoadSFX("interface/ui/sfx/a.sfx", true)
 ````

* <h4 id="LuaItemSFX_UnloadSFX">UnloadSFX</h4>
Unload SFX model.

 > (`void`) ItemSFX:UnloadSFX()

 ````lua
 ItemSFX:UnloadSFX()
 ````

* <h4 id="LuaItemSFX_Play">Play</h4>
Play SFX.

 > (`void`) ItemSFX:Play([`bool` bLoop = false])

 ````lua
 ItemSFX:Play()
 ItemSFX:Play(true)
 ````

* <h4 id="LuaItemSFX_SetModelScale">SetModelScale</h4>
Set model scale.

 > (`void`) ItemSFX:SetModelScale(`number` fScale)

 > (`void`) ItemSFX:SetModelScale(`number` fScaleX, `number` fScaleY, `number` fScaleZ)

 ````lua
 ItemSFX:SetModelScale(1.0)
 ItemSFX:SetModelScale(1.0, 2.0, 1.0)
 ````

* <h4 id="LuaItemSFX_GetModelScale">GetModelScale</h4>
Get model scale.

Note: current binding pushes 3 values but returns 1, so only **one** number is returned.

 > (`number` fScale) ItemSFX:GetModelScale()

 ````lua
 local fScale = ItemSFX:GetModelScale()
 ````

* <h4 id="LuaItemSFX_Get3DModel">Get3DModel</h4>
Get 3D model userdata.

 > (`IKG3DModel` Model) ItemSFX:Get3DModel()

 ````lua
 local Model = ItemSFX:Get3DModel()
 ````

* <h4 id="LuaItemSFX_Set2DRotation">Set2DRotation</h4>
Set 2D rotation.

 > (`void`) ItemSFX:Set2DRotation(`number` fAngle)

 ````lua
 ItemSFX:Set2DRotation(0)
 ````

* <h4 id="LuaItemSFX_SetAngle">SetAngle</h4>
Set angle.

 > (`void`) ItemSFX:SetAngle(`number` fAngle)

 ````lua
 ItemSFX:SetAngle(0)
 ````

* <h4 id="LuaItemSFX_SetYaw">SetYaw</h4>
Set yaw.

 > (`void`) ItemSFX:SetYaw(`number` fAngle)

 ````lua
 ItemSFX:SetYaw(0)
 ````

* <h4 id="LuaItemSFX_SetPlaySpeed">SetPlaySpeed</h4>
Set play speed.

 > (`void`) ItemSFX:SetPlaySpeed(`number` fSpeed)

 ````lua
 ItemSFX:SetPlaySpeed(1.0)
 ````
