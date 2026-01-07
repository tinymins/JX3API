# IKG3DScene

部分“查询类接口”实现为异步请求，会返回 `"_call_id", <number>`。

Methods:
- `EnablePostRenderEffect`
- `AddRenderEntity`
- `RemoveRenderEntity`
- `GetCameraMovement`
- `GetLoadingProcess`
- `SetFocus`
- `LoadEnvironment`
- `LoadEnvironmentProperty`
- `ResetDefaultEnvironment`
- `SetCurrentPackageIndex`
- `GetCameraPosition`
- `SetCameraPosition`
- `SetCameraLookAtPosition`
- `GetCameraLookAtPosition`
- `GetCameraUpDirection`
- `SetCameraUpDirection`
- `GetCameraCurrentState`
- `UpdateCamera`
- `SetCameraPerspective`
- `SetCameraOrthogonal`
- `PlayCameraAni`
- `StopCameraAni`
- `PauseCameraAni`
- `IsPlayingCameraAni`
- `SetMainPlayerPosition`
- `SetName`

* <h4 id="LuaScene_EnablePostRenderEffect">EnablePostRenderEffect</h4>
> () IKG3DScene:EnablePostRenderEffect(nPostRenderEffectType, bEnable)

按类型开关后处理效果。

* <h4 id="LuaScene_AddRenderEntity">AddRenderEntity</h4>
> () IKG3DScene:AddRenderEntity(model[, bLight[, bSelectable]])

把 `model` 加入当前场景。

- 允许 2/3/4 个参数（包含 `self`）。
- `bLight`、`bSelectable`（可选）用 `lua_toboolean` 读取。

* <h4 id="LuaScene_RemoveRenderEntity">RemoveRenderEntity</h4>
> () IKG3DScene:RemoveRenderEntity(model[, bSelectable])

把 `model` 从当前场景移除。

- 允许 2 或 3 个参数（包含 `self`）。

* <h4 id="LuaScene_GetCameraMovement">GetCameraMovement</h4>
> (IKG3DSceneCameraMovement) IKG3DScene:GetCameraMovement()

返回场景相机运动对象。

* <h4 id="LuaScene_GetLoadingProcess">GetLoadingProcess</h4>
> (string, number[, string]) IKG3DScene:GetLoadingProcess()

异步查询加载进度。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaScene_SetFocus">SetFocus</h4>
> () IKG3DScene:SetFocus(x, y, z)

设置场景焦点位置。

* <h4 id="LuaScene_LoadEnvironment">LoadEnvironment</h4>
> () IKG3DScene:LoadEnvironment(pcszEnvFile)

加载环境文件路径（非空字符串）。

* <h4 id="LuaScene_LoadEnvironmentProperty">LoadEnvironmentProperty</h4>
> () IKG3DScene:LoadEnvironmentProperty(pcszMapFileDir, pcszMapName)

用两个字符串参数加载环境属性。

* <h4 id="LuaScene_ResetDefaultEnvironment">ResetDefaultEnvironment</h4>
> () IKG3DScene:ResetDefaultEnvironment()

重置默认环境。

* <h4 id="LuaScene_SetCurrentPackageIndex">SetCurrentPackageIndex</h4>
> () IKG3DScene:SetCurrentPackageIndex(dwPackageIndex)

设置当前包索引。

* <h4 id="LuaScene_GetCameraPosition">GetCameraPosition</h4>
> (string, number, string) IKG3DScene:GetCameraPosition()

异步查询相机位置。

注意：当前实现里 `nResult` 被无条件设为 `false`，因此即使成功投递请求，也会额外返回 `"_error0"`。但 `"_call_id"` 仍然会生成。

* <h4 id="LuaScene_SetCameraPosition">SetCameraPosition</h4>
> () IKG3DScene:SetCameraPosition(x, y, z)

设置场景相机位置。

* <h4 id="LuaScene_SetCameraLookAtPosition">SetCameraLookAtPosition</h4>
> () IKG3DScene:SetCameraLookAtPosition(x, y, z)

设置场景相机 look-at 位置。

* <h4 id="LuaScene_GetCameraLookAtPosition">GetCameraLookAtPosition</h4>
> (string, number, string) IKG3DScene:GetCameraLookAtPosition()

异步查询相机 look-at 位置。

注意：与 `GetCameraPosition` 相同，当前实现会因为内部标志被设为 `false` 而总是额外返回 `"_error0"`。

* <h4 id="LuaScene_GetCameraUpDirection">GetCameraUpDirection</h4>
> (string, number[, string]) IKG3DScene:GetCameraUpDirection()

异步查询相机上方向。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaScene_SetCameraUpDirection">SetCameraUpDirection</h4>
> () IKG3DScene:SetCameraUpDirection(x, y, z)

设置场景相机上方向。

* <h4 id="LuaScene_GetCameraCurrentState">GetCameraCurrentState</h4>
> (string, number[, string]) IKG3DScene:GetCameraCurrentState()

异步查询相机当前状态。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaScene_UpdateCamera">UpdateCamera</h4>
> () IKG3DScene:UpdateCamera(px, py, pz, ax, ay, az, fLookAtOffset, fTargetSpeed)

用 8 个 number 参数更新场景相机。

* <h4 id="LuaScene_SetCameraPerspective">SetCameraPerspective</h4>
> () IKG3DScene:SetCameraPerspective(fFovy, fAspect, fZNear, fZFar)

设置场景相机的透视参数。

* <h4 id="LuaScene_SetCameraOrthogonal">SetCameraOrthogonal</h4>
> () IKG3DScene:SetCameraOrthogonal(fWidth, fHeight, fZNear, fZFar)

设置场景相机的正交投影参数。

* <h4 id="LuaScene_PlayCameraAni">PlayCameraAni</h4>
> () IKG3DScene:PlayCameraAni(pcszFile, bLoop)

播放相机动画文件。

- `pcszFile` 必须是非空字符串。
- 第 3 个参数必须是 boolean。

* <h4 id="LuaScene_StopCameraAni">StopCameraAni</h4>
> () IKG3DScene:StopCameraAni()

停止相机动画。

* <h4 id="LuaScene_PauseCameraAni">PauseCameraAni</h4>
> () IKG3DScene:PauseCameraAni()

暂停相机动画。

* <h4 id="LuaScene_IsPlayingCameraAni">IsPlayingCameraAni</h4>
> () IKG3DScene:IsPlayingCameraAni()

投递“是否正在播放相机动画”的查询请求。

注意：当前实现不返回值（只投递事件）。

* <h4 id="LuaScene_SetMainPlayerPosition">SetMainPlayerPosition</h4>
> () IKG3DScene:SetMainPlayerPosition(x, y, z)

设置场景中的主角位置。

* <h4 id="LuaScene_SetName">SetName</h4>
> () IKG3DScene:SetName(pcszName)

设置 MiniScene 名称（非空字符串）。
