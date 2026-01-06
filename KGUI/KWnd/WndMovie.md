# WndMovie

Notes:

- `WndMovie` inherits all methods from `WndWindow`; only additional methods are listed here.

[`Play`](#LuaMovie_Play)
[`Stop`](#LuaMovie_Stop)
[`SetVolume`](#LuaMovie_SetVolume)
[`IsFinished`](#LuaMovie_IsFinished)
[`SetLoop`](#LuaMovie_SetLoop)
[`GetMovieSize`](#LuaMovie_GetMovieSize)

* <h4 id="LuaMovie_Play">Play</h4>

 > (`void`) WndMovie:Play(`string` szFile)

* <h4 id="LuaMovie_Stop">Stop</h4>

 > (`void`) WndMovie:Stop()

* <h4 id="LuaMovie_SetVolume">SetVolume</h4>

 > (`void`) WndMovie:SetVolume(`number` fVolume)

* <h4 id="LuaMovie_IsFinished">IsFinished</h4>

 > (`bool` bFinished) WndMovie:IsFinished()

* <h4 id="LuaMovie_SetLoop">SetLoop</h4>

 > (`void`) WndMovie:SetLoop(`bool|number` bLoop)

* <h4 id="LuaMovie_GetMovieSize">GetMovieSize</h4>

 > (`number` w, `number` h) WndMovie:GetMovieSize()
