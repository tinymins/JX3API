[English](./ItemSFX.md) | 中文

# ItemSFX（特效）

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
加载 SFX 模型。

参数个数必须为 2 或 3；`bShowOnce` 会以 `lua_toboolean` 取值。

 > (`void`) ItemSFX:LoadSFX(`string` szFile[, `bool` bShowOnce = false])

 ````lua
 ItemSFX:LoadSFX("interface/ui/sfx/a.sfx")
 ItemSFX:LoadSFX("interface/ui/sfx/a.sfx", true)
 ````

* <h4 id="LuaItemSFX_UnloadSFX">UnloadSFX</h4>
卸载 SFX 模型。

 > (`void`) ItemSFX:UnloadSFX()

 ````lua
 ItemSFX:UnloadSFX()
 ````

* <h4 id="LuaItemSFX_Play">Play</h4>
播放特效。

 > (`void`) ItemSFX:Play([`bool` bLoop = false])

 ````lua
 ItemSFX:Play()
 ItemSFX:Play(true)
 ````

* <h4 id="LuaItemSFX_SetModelScale">SetModelScale</h4>
设置model 缩放。

 > (`void`) ItemSFX:SetModelScale(`number` fScale)

 > (`void`) ItemSFX:SetModelScale(`number` fScaleX, `number` fScaleY, `number` fScaleZ)

 ````lua
 ItemSFX:SetModelScale(1.0)
 ItemSFX:SetModelScale(1.0, 2.0, 1.0)
 ````

* <h4 id="LuaItemSFX_GetModelScale">GetModelScale</h4>
获取model 缩放。

注意：当前绑定会压入 3 个值但只返回 1 个，因此最终只会得到**一个**数值。

 > (`number` fScale) ItemSFX:GetModelScale()

 ````lua
 local fScale = ItemSFX:GetModelScale()
 ````

* <h4 id="LuaItemSFX_Get3DModel">Get3DModel</h4>
获取 3D 模型的 UserData。

 > (`IKG3DModel` Model) ItemSFX:Get3DModel()

 ````lua
 local Model = ItemSFX:Get3DModel()
 ````

* <h4 id="LuaItemSFX_Set2DRotation">Set2DRotation</h4>
设置2D 旋转。

 > (`void`) ItemSFX:Set2DRotation(`number` fAngle)

 ````lua
 ItemSFX:Set2DRotation(0)
 ````

* <h4 id="LuaItemSFX_SetAngle">SetAngle</h4>
设置角度。

 > (`void`) ItemSFX:SetAngle(`number` fAngle)

 ````lua
 ItemSFX:SetAngle(0)
 ````

* <h4 id="LuaItemSFX_SetYaw">SetYaw</h4>
设置yaw。

 > (`void`) ItemSFX:SetYaw(`number` fAngle)

 ````lua
 ItemSFX:SetYaw(0)
 ````

* <h4 id="LuaItemSFX_SetPlaySpeed">SetPlaySpeed</h4>
设置play speed。

 > (`void`) ItemSFX:SetPlaySpeed(`number` fSpeed)

 ````lua
 ItemSFX:SetPlaySpeed(1.0)
 ````
