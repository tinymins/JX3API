# WndScene

Notes:

- `WndScene` inherits all methods from `WndWindow`; only additional methods are listed here.

[`SetScene`](#LuaScene_SetScene)
[`EnableRenderTerrain`](#LuaScene_EnableRenderTerrain)
[`EnableRenderSkyBox`](#LuaScene_EnableRenderSkyBox)
[`EnableFrameMove`](#LuaScene_EnableFrameMove)

* <h4 id="LuaScene_SetScene">SetScene</h4>

Sets the scene (accepts either a scene userdata or a numeric scene id).

 > (`void`) WndScene:SetScene(`userdata|number` scene)

* <h4 id="LuaScene_EnableRenderTerrain">EnableRenderTerrain</h4>

Enables or disables terrain rendering.

 > (`void`) WndScene:EnableRenderTerrain(`bool|number` bEnable)

* <h4 id="LuaScene_EnableRenderSkyBox">EnableRenderSkyBox</h4>

Enables or disables skybox rendering.

 > (`void`) WndScene:EnableRenderSkyBox(`bool|number` bEnable)

* <h4 id="LuaScene_EnableFrameMove">EnableFrameMove</h4>

Enables or disables scene framemove/update.

 > (`void`) WndScene:EnableFrameMove(`bool|number` bEnable)
