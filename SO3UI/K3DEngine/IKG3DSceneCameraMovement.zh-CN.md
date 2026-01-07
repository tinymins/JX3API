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

返回当前相机动画的 userdata。

* <h4 id="LuaCameraMovement_SetCurrentAnimation">SetCurrentAnimation</h4>
> () IKG3DSceneCameraMovement:SetCurrentAnimation(nCameraAnimationIndex)

按索引设置当前动画。

* <h4 id="LuaCameraMovement_GetAnimationCount">GetAnimationCount</h4>
> (number) IKG3DSceneCameraMovement:GetAnimationCount()

返回动画数量。

* <h4 id="LuaCameraMovement_FindAnimation">FindAnimation</h4>
> (number) IKG3DSceneCameraMovement:FindAnimation(szCameraAnimation)

按名称查找动画并返回索引。

* <h4 id="LuaCameraMovement_Clear">Clear</h4>
> () IKG3DSceneCameraMovement:Clear()

清空相机运动的动画/状态。

* <h4 id="LuaCameraMovement_LoadFromFile">LoadFromFile</h4>
> () IKG3DSceneCameraMovement:LoadFromFile(szFilePath)

从非空路径加载相机运动数据。
