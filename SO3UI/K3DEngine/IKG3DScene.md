# IKG3DScene

Some scene queries are implemented as async requests and return `"_call_id", <number>`.

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

Enables/disables a post-render effect by type.

* <h4 id="LuaScene_AddRenderEntity">AddRenderEntity</h4>
> () IKG3DScene:AddRenderEntity(model[, bLight[, bSelectable]])

Adds `model` into this scene.

- Accepts 2, 3 or 4 arguments (including `self`).
- `bLight` and `bSelectable` are read via `lua_toboolean` when provided.

* <h4 id="LuaScene_RemoveRenderEntity">RemoveRenderEntity</h4>
> () IKG3DScene:RemoveRenderEntity(model[, bSelectable])

Removes `model` from this scene.

- Accepts 2 or 3 arguments (including `self`).

* <h4 id="LuaScene_GetCameraMovement">GetCameraMovement</h4>
> (IKG3DSceneCameraMovement) IKG3DScene:GetCameraMovement()

Returns the scene camera movement object.

* <h4 id="LuaScene_GetLoadingProcess">GetLoadingProcess</h4>
> (string, number[, string]) IKG3DScene:GetLoadingProcess()

Posts an async query for loading progress.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaScene_SetFocus">SetFocus</h4>
> () IKG3DScene:SetFocus(x, y, z)

Sets scene focus position.

* <h4 id="LuaScene_LoadEnvironment">LoadEnvironment</h4>
> () IKG3DScene:LoadEnvironment(pcszEnvFile)

Loads an environment file path (non-empty string).

* <h4 id="LuaScene_LoadEnvironmentProperty">LoadEnvironmentProperty</h4>
> () IKG3DScene:LoadEnvironmentProperty(pcszMapFileDir, pcszMapName)

Loads environment properties using two string parameters.

* <h4 id="LuaScene_ResetDefaultEnvironment">ResetDefaultEnvironment</h4>
> () IKG3DScene:ResetDefaultEnvironment()

Resets the default environment.

* <h4 id="LuaScene_SetCurrentPackageIndex">SetCurrentPackageIndex</h4>
> () IKG3DScene:SetCurrentPackageIndex(dwPackageIndex)

Sets current package index.

* <h4 id="LuaScene_GetCameraPosition">GetCameraPosition</h4>
> (string, number, string) IKG3DScene:GetCameraPosition()

Posts an async query for camera position.

Note: the current implementation sets an internal `nResult` flag to `false` unconditionally, so it always appends `"_error0"` even after posting the request. The returned `"_call_id"` is still generated.

* <h4 id="LuaScene_SetCameraPosition">SetCameraPosition</h4>
> () IKG3DScene:SetCameraPosition(x, y, z)

Sets the scene camera position.

* <h4 id="LuaScene_SetCameraLookAtPosition">SetCameraLookAtPosition</h4>
> () IKG3DScene:SetCameraLookAtPosition(x, y, z)

Sets the scene camera look-at position.

* <h4 id="LuaScene_GetCameraLookAtPosition">GetCameraLookAtPosition</h4>
> (string, number, string) IKG3DScene:GetCameraLookAtPosition()

Posts an async query for camera look-at position.

Note: same as `GetCameraPosition`, the current implementation always appends `"_error0"` due to an internal flag being set to `false`.

* <h4 id="LuaScene_GetCameraUpDirection">GetCameraUpDirection</h4>
> (string, number[, string]) IKG3DScene:GetCameraUpDirection()

Posts an async query for camera up direction.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaScene_SetCameraUpDirection">SetCameraUpDirection</h4>
> () IKG3DScene:SetCameraUpDirection(x, y, z)

Sets the scene camera up direction.

* <h4 id="LuaScene_GetCameraCurrentState">GetCameraCurrentState</h4>
> (string, number[, string]) IKG3DScene:GetCameraCurrentState()

Posts an async query for current camera state.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaScene_UpdateCamera">UpdateCamera</h4>
> () IKG3DScene:UpdateCamera(px, py, pz, ax, ay, az, fLookAtOffset, fTargetSpeed)

Updates the scene camera using 8 numeric parameters.

* <h4 id="LuaScene_SetCameraPerspective">SetCameraPerspective</h4>
> () IKG3DScene:SetCameraPerspective(fFovy, fAspect, fZNear, fZFar)

Sets scene camera perspective values.

* <h4 id="LuaScene_SetCameraOrthogonal">SetCameraOrthogonal</h4>
> () IKG3DScene:SetCameraOrthogonal(fWidth, fHeight, fZNear, fZFar)

Sets scene camera orthogonal projection values.

* <h4 id="LuaScene_PlayCameraAni">PlayCameraAni</h4>
> () IKG3DScene:PlayCameraAni(pcszFile, bLoop)

Plays a camera animation file.

- `pcszFile` must be a non-empty string.
- Argument 3 must be a boolean.

* <h4 id="LuaScene_StopCameraAni">StopCameraAni</h4>
> () IKG3DScene:StopCameraAni()

Stops camera animation.

* <h4 id="LuaScene_PauseCameraAni">PauseCameraAni</h4>
> () IKG3DScene:PauseCameraAni()

Pauses camera animation.

* <h4 id="LuaScene_IsPlayingCameraAni">IsPlayingCameraAni</h4>
> () IKG3DScene:IsPlayingCameraAni()

Posts a request to query whether camera animation is playing.

Note: the current implementation returns no values (it only posts an event).

* <h4 id="LuaScene_SetMainPlayerPosition">SetMainPlayerPosition</h4>
> () IKG3DScene:SetMainPlayerPosition(x, y, z)

Sets the main player position in the scene.

* <h4 id="LuaScene_SetName">SetName</h4>
> () IKG3DScene:SetName(pcszName)

Sets mini-scene name.
