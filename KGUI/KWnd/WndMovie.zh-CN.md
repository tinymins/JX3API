[English](./WndMovie.md) | 中文

# WndMovie（影片）

说明：

- `WndMovie` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

[`Play`](#LuaMovie_Play)
[`Stop`](#LuaMovie_Stop)
[`SetVolume`](#LuaMovie_SetVolume)
[`IsFinished`](#LuaMovie_IsFinished)
[`SetLoop`](#LuaMovie_SetLoop)
[`GetMovieSize`](#LuaMovie_GetMovieSize)

* <h4 id="LuaMovie_Play">Play</h4>

播放视频。

`szFile` 必须为非空字符串，否则会报错。

 > (`void`) WndMovie:Play(`string` szFile)

* <h4 id="LuaMovie_Stop">Stop</h4>

停止播放。

 > (`void`) WndMovie:Stop()

* <h4 id="LuaMovie_SetVolume">SetVolume</h4>

设置音量。

 > (`void`) WndMovie:SetVolume(`number` fVolume)

* <h4 id="LuaMovie_IsFinished">IsFinished</h4>

检查当前是否播放完毕。

 > (`bool` bFinished) WndMovie:IsFinished()

* <h4 id="LuaMovie_SetLoop">SetLoop</h4>

设置是否循环播放。

Lua 绑定会通过 `lua_toboolean` 转换，`number` 也可作为 true/false 参与判断。

 > (`void`) WndMovie:SetLoop(`bool|number` bLoop)

* <h4 id="LuaMovie_GetMovieSize">GetMovieSize</h4>

获取视频尺寸（像素）。

 > (`number` w, `number` h) WndMovie:GetMovieSize()
