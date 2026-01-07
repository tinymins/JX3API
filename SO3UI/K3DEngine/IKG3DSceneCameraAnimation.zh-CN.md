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

开始播放动画。

`bLoop` 允许传 boolean 或 number（非 0 视为 true）。

* <h4 id="LuaCameraAnimation_Stop">Stop</h4>
> () IKG3DSceneCameraAnimation:Stop()

停止播放。

* <h4 id="LuaCameraAnimation_Pause">Pause</h4>
> (table) IKG3DSceneCameraAnimation:Pause()

暂停播放，并返回一个关键帧 table，包含以下字段：

- `position`: `{ x, y, z }`
- `lookat`: `{ x, y, z }`
- `tangentposition`: `{ x, y, z }`
- `tangentlookat`: `{ x, y, z }`

* <h4 id="LuaCameraAnimation_GetName">GetName</h4>
> (string) IKG3DSceneCameraAnimation:GetName()

返回动画名称（非空字符串）。

* <h4 id="LuaCameraAnimation_SetName">SetName</h4>
> () IKG3DSceneCameraAnimation:SetName(szName)

设置动画名称（非空字符串）。

* <h4 id="LuaCameraAnimation_IsPlaying">IsPlaying</h4>
> (bool) IKG3DSceneCameraAnimation:IsPlaying()

返回当前是否正在播放。
