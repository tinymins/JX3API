# IKG3DSceneCameraMovement

Methods:
- `GetCurrentAnimation`
- `SetCurrentAnimation`
- `GetAnimationCount`
- `FindAnimation`
- `Clear`
- `LoadFromFile`

* <h4 id="LuaCameraMovement_GetCurrentAnimation">GetCurrentAnimation</h4>
> (IKG3DSceneCameraAnimation) IKG3DSceneCameraMovement:GetCurrentAnimation()

Returns the current camera animation userdata.

* <h4 id="LuaCameraMovement_SetCurrentAnimation">SetCurrentAnimation</h4>
> () IKG3DSceneCameraMovement:SetCurrentAnimation(nCameraAnimationIndex)

Sets the current animation by index.

* <h4 id="LuaCameraMovement_GetAnimationCount">GetAnimationCount</h4>
> (number) IKG3DSceneCameraMovement:GetAnimationCount()

Returns the number of animations.

* <h4 id="LuaCameraMovement_FindAnimation">FindAnimation</h4>
> (number) IKG3DSceneCameraMovement:FindAnimation(szCameraAnimation)

Finds an animation by name and returns its index.

* <h4 id="LuaCameraMovement_Clear">Clear</h4>
> () IKG3DSceneCameraMovement:Clear()

Clears camera movement animations/state.

* <h4 id="LuaCameraMovement_LoadFromFile">LoadFromFile</h4>
> () IKG3DSceneCameraMovement:LoadFromFile(szFilePath)

Loads camera movement data from a non-empty file path.
