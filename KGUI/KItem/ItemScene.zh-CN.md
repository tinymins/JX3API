[English](./ItemScene.md) | 中文

# ItemScene（场景）

[`SetScene`](#LuaItemScene_SetScene)
[`GetScene`](#LuaItemScene_GetScene)
[`EnableRenderTerrain`](#LuaItemScene_EnableRenderTerrain)
[`EnableRenderSkyBox`](#LuaItemScene_EnableRenderSkyBox)
[`EnableAlpha`](#LuaItemScene_EnableAlpha)

* <h4 id="LuaItemScene_SetScene">SetScene</h4>
设置场景。

`sceneId` 可以是场景 `userdata`（会通过 `ToIKG3DObjID()` 转换），也可以是数字 scene id。

 > (`void`) ItemScene:SetScene(`userdata|number` sceneId)

 ````lua
 ItemScene:SetScene(Scene)
 ````

* <h4 id="LuaItemScene_GetScene">GetScene</h4>
获取当前场景。

 > (`IKG3DScene` Scene) ItemScene:GetScene()

 ````lua
 local Scene = ItemScene:GetScene()
 ````

* <h4 id="LuaItemScene_EnableRenderTerrain">EnableRenderTerrain</h4>
启用/禁用渲染地形。

 > (`void`) ItemScene:EnableRenderTerrain(`bool|number` bEnable)

 ````lua
 ItemScene:EnableRenderTerrain(true)
 ````

* <h4 id="LuaItemScene_EnableRenderSkyBox">EnableRenderSkyBox</h4>
启用/禁用渲染 SkyBox。

 > (`void`) ItemScene:EnableRenderSkyBox(`bool|number` bEnable)

 ````lua
 ItemScene:EnableRenderSkyBox(true)
 ````

* <h4 id="LuaItemScene_EnableAlpha">EnableAlpha</h4>
启用/禁用透明度。

 > (`void`) ItemScene:EnableAlpha(`bool|number` bEnable)

 ````lua
 ItemScene:EnableAlpha(true)
 ````
