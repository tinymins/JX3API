[English](./WndScene.md) | 中文

# WndScene（场景）

说明：

- `WndScene` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

[`SetScene`](#LuaScene_SetScene)
[`EnableRenderTerrain`](#LuaScene_EnableRenderTerrain)
[`EnableRenderSkyBox`](#LuaScene_EnableRenderSkyBox)
[`EnableFrameMove`](#LuaScene_EnableFrameMove)

* <h4 id="LuaScene_SetScene">SetScene</h4>

设置场景。

`scene` 参数既可以传入场景对象的 userdata（内部通过 `ToIKG3DObjID()` 转换），也可以直接传入数字 scene id。

 > (`void`) WndScene:SetScene(`userdata|number` scene)

* <h4 id="LuaScene_EnableRenderTerrain">EnableRenderTerrain</h4>

开启/关闭地形渲染。

Lua 绑定会通过 `lua_toboolean` 转换，`number` 也可作为 true/false 参与判断。

 > (`void`) WndScene:EnableRenderTerrain(`bool|number` bEnable)

* <h4 id="LuaScene_EnableRenderSkyBox">EnableRenderSkyBox</h4>

开启/关闭天空盒渲染。

Lua 绑定会通过 `lua_toboolean` 转换，`number` 也可作为 true/false 参与判断。

 > (`void`) WndScene:EnableRenderSkyBox(`bool|number` bEnable)

* <h4 id="LuaScene_EnableFrameMove">EnableFrameMove</h4>

开启/关闭场景的 FrameMove。

Lua 绑定会通过 `lua_toboolean` 转换，`number` 也可作为 true/false 参与判断。

 > (`void`) WndScene:EnableFrameMove(`bool|number` bEnable)
