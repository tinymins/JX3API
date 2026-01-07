# IKG3DSceneCameraAnimation

Methods:
- `Play`
- `Stop`
- `Pause`
- `GetName`
- `SetName`
- `IsPlaying`

* <h4 id="LuaCameraAnimation_Play">Play</h4>
> () IKG3DSceneCameraAnimation:Play(bLoop)

Starts playing the animation.

`bLoop` is accepted as either a boolean or a number (non-zero treated as true).

* <h4 id="LuaCameraAnimation_Stop">Stop</h4>
> () IKG3DSceneCameraAnimation:Stop()

Stops playing the animation.

* <h4 id="LuaCameraAnimation_Pause">Pause</h4>
> (table) IKG3DSceneCameraAnimation:Pause()

Pauses playing and returns a keyframe table with the following fields:

- `position`: `{ x, y, z }`
- `lookat`: `{ x, y, z }`
- `tangentposition`: `{ x, y, z }`
- `tangentlookat`: `{ x, y, z }`

* <h4 id="LuaCameraAnimation_GetName">GetName</h4>
> (string) IKG3DSceneCameraAnimation:GetName()

Returns the animation name (non-empty string).

* <h4 id="LuaCameraAnimation_SetName">SetName</h4>
> () IKG3DSceneCameraAnimation:SetName(szName)

Sets the animation name (non-empty string).

* <h4 id="LuaCameraAnimation_IsPlaying">IsPlaying</h4>
> (bool) IKG3DSceneCameraAnimation:IsPlaying()

Returns whether the animation is currently playing.
