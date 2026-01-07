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

Plays a movie/video file.

 > (`void`) WndMovie:Play(`string` szFile)

* <h4 id="LuaMovie_Stop">Stop</h4>

Stops playback.

 > (`void`) WndMovie:Stop()

* <h4 id="LuaMovie_SetVolume">SetVolume</h4>

Sets playback volume.

 > (`void`) WndMovie:SetVolume(`number` fVolume)

* <h4 id="LuaMovie_IsFinished">IsFinished</h4>

Returns whether playback has finished.

 > (`bool` bFinished) WndMovie:IsFinished()

* <h4 id="LuaMovie_SetLoop">SetLoop</h4>

Enables or disables looping.

 > (`void`) WndMovie:SetLoop(`bool|number` bLoop)

* <h4 id="LuaMovie_GetMovieSize">GetMovieSize</h4>

Gets the movie resolution (width/height).

 > (`number` w, `number` h) WndMovie:GetMovieSize()
