# ItemScene

[`SetScene`](#LuaItemScene_SetScene)
[`GetScene`](#LuaItemScene_GetScene)
[`EnableRenderTerrain`](#LuaItemScene_EnableRenderTerrain)
[`EnableRenderSkyBox`](#LuaItemScene_EnableRenderSkyBox)
[`EnableAlpha`](#LuaItemScene_EnableAlpha)

* <h4 id="LuaItemScene_SetScene">SetScene</h4>
Set scene.

Argument can be a scene userdata or a numeric scene id.

 > (`void`) ItemScene:SetScene(`userdata|number` sceneId)

 ````lua
 ItemScene:SetScene(Scene)
 ````

* <h4 id="LuaItemScene_GetScene">GetScene</h4>
Get current scene.

 > (`IKG3DScene` Scene) ItemScene:GetScene()

 ````lua
 local Scene = ItemScene:GetScene()
 ````

* <h4 id="LuaItemScene_EnableRenderTerrain">EnableRenderTerrain</h4>
Enable/disable rendering terrain.

 > (`void`) ItemScene:EnableRenderTerrain(`bool|number` bEnable)

 ````lua
 ItemScene:EnableRenderTerrain(true)
 ````

* <h4 id="LuaItemScene_EnableRenderSkyBox">EnableRenderSkyBox</h4>
Enable/disable rendering sky box.

 > (`void`) ItemScene:EnableRenderSkyBox(`bool|number` bEnable)

 ````lua
 ItemScene:EnableRenderSkyBox(true)
 ````

* <h4 id="LuaItemScene_EnableAlpha">EnableAlpha</h4>
Enable/disable alpha.

 > (`void`) ItemScene:EnableAlpha(`bool|number` bEnable)

 ````lua
 ItemScene:EnableAlpha(true)
 ````
