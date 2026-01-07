# IKG3DModel

该元表里有不少“查询类接口”是异步的：会向引擎投递请求，然后返回一对键值 `"_call_id", <number>` 作为本次请求的标识。

Methods:
- `RegisterEventHandler`
- `UnregisterEventHandler`
- `PlayAnimation`
- `PauseAnimation`
- `LoadMaterialFromFile`
- `SetTranslation`
- `SetRotation`
- `SetScaling`
- `GetTranslation`
- `GetRotation`
- `GetScaling`
- `BindToSocket`
- `BindToBone`
- `UnbindFromOther`
- `SetAlpha`
- `SetHighLightLevel`
- `GetHightLightLevel`
- `GetAlpha`
- `Release`
- `Attach`
- `Detach`
- `SetYaw`
- `SetFaceMotionMode`
- `SetDetail`
- `SetDetailColor`
- `Cmd`
- `SetImportance`
- `GetFaceDefinition`
- `SetFaceDefinition`
- `SetFaceBoneParams`
- `SetFaceDecals`
- `LoadFaceDefinitionINI`
- `SaveFaceDefinitionFileHD`
- `SetFacePartID`
- `GetFacePartID`
- `SetForceRealInterpolate`
- `HideMeshPointOutsideCloak`
- `ClearHideMeshPointOutsideCloak`
- `Find`
- `__eq`
- `__gc`（仅在启用 `KGUI_MODEL_GC_API` 时存在）

* <h4 id="LuaModel_RegisterEventHandler">RegisterEventHandler</h4>
> () IKG3DModel:RegisterEventHandler()

向事件适配器注册该模型的事件处理。

* <h4 id="LuaModel_UnregisterEventHandler">UnregisterEventHandler</h4>
> () IKG3DModel:UnregisterEventHandler()

取消注册该模型的事件处理。

* <h4 id="LuaModel_PlayAnimation">PlayAnimation</h4>
> () IKG3DModel:PlayAnimation(szPlayType, szAnimationName, fSpeed, nOffsetTime[, fTweenTime])

请求模型播放动画。

- 至少需要 5 个参数（包含 `self`）。
- `szPlayType` 作为字符串解析，常用值：`"loop"` / `"once"` / `"last"`。
- `szAnimationName` 读取为字符串；如果传入 `nil`，当前实现会直接当作“无需播放”并正常返回（相当于 no-op）。
- `fTweenTime` 可选：当传入第 6 个参数时读取。

该调用向引擎投递请求，不返回值。

* <h4 id="LuaModel_PauseAnimation">PauseAnimation</h4>
> () IKG3DModel:PauseAnimation(bPause)

暂停或恢复当前动画。

* <h4 id="LuaModel_LoadMaterialFromFile">LoadMaterialFromFile</h4>
> () IKG3DModel:LoadMaterialFromFile(szFilePath)

从 `szFilePath`（非空字符串）加载材质数据。

* <h4 id="LuaModel_SetTranslation">SetTranslation</h4>
> () IKG3DModel:SetTranslation(x, y, z)

设置模型位移。

* <h4 id="LuaModel_SetRotation">SetRotation</h4>
> () IKG3DModel:SetRotation(x, y, z, w)

设置模型旋转（4 个 float）。

* <h4 id="LuaModel_SetScaling">SetScaling</h4>
> () IKG3DModel:SetScaling(x, y, z)

设置模型缩放。

* <h4 id="LuaModel_GetTranslation">GetTranslation</h4>
> (string, number[, string]) IKG3DModel:GetTranslation()

异步查询模型位移。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaModel_GetRotation">GetRotation</h4>
> (string, number[, string]) IKG3DModel:GetRotation()

异步查询模型旋转。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaModel_GetScaling">GetScaling</h4>
> (string, number[, string]) IKG3DModel:GetScaling()

异步查询模型缩放。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaModel_BindToSocket">BindToSocket</h4>
> () IKG3DModel:BindToSocket(otherModel[, szSocket])

把当前模型绑定到 `otherModel` 的某个 socket 上。

- 允许 2 或 3 个参数（包含 `self`）。
- 不传 `szSocket` 时会使用空字符串。

* <h4 id="LuaModel_BindToBone">BindToBone</h4>
> () IKG3DModel:BindToBone(otherModel[, szBone])

把当前模型绑定到 `otherModel` 的某根骨骼上。

- 允许 2 或 3 个参数（包含 `self`）。
- 不传 `szBone` 时会使用空字符串。

* <h4 id="LuaModel_UnbindFromOther">UnbindFromOther</h4>
> () IKG3DModel:UnbindFromOther([parentModel])

解除当前模型与其他模型的绑定关系。

- 允许 1 或 2 个参数（包含 `self`）。
- 不传 `parentModel` 时，内部 parent id 默认是 `-1`。

* <h4 id="LuaModel_SetAlpha">SetAlpha</h4>
> () IKG3DModel:SetAlpha(fAlpha)

设置透明度（float）。

* <h4 id="LuaModel_SetHighLightLevel">SetHighLightLevel</h4>
> () IKG3DModel:SetHighLightLevel(fIllumination)

设置高亮强度（float）。

* <h4 id="LuaModel_GetHightLightLevel">GetHightLightLevel</h4>
> (string, number[, string]) IKG3DModel:GetHightLightLevel()

异步查询高亮强度。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaModel_GetAlpha">GetAlpha</h4>
> (string, number[, string]) IKG3DModel:GetAlpha()

异步查询透明度。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaModel_Release">Release</h4>
> () IKG3DModel:Release()

释放模型。

在启用 `KGUI_MODEL_GC_API` 的版本中，该操作还会把模型从内部“活跃模型集合”中移除。

* <h4 id="LuaModel_Attach">Attach</h4>
> () IKG3DModel:Attach(parentModel)

把当前模型挂接到 `parentModel`。

* <h4 id="LuaModel_Detach">Detach</h4>
> () IKG3DModel:Detach(rhsModel)

把当前模型从 `rhsModel` 分离。

* <h4 id="LuaModel_SetYaw">SetYaw</h4>
> () IKG3DModel:SetYaw(fYaw)

设置 yaw（float）。

* <h4 id="LuaModel_SetFaceMotionMode">SetFaceMotionMode</h4>
> () IKG3DModel:SetFaceMotionMode()

开启面部运动模式。

* <h4 id="LuaModel_SetDetail">SetDetail</h4>
> () IKG3DModel:SetDetail(nColorChannelTable, nColorChannel)

设置细节/通道相关参数。

* <h4 id="LuaModel_SetDetailColor">SetDetailColor</h4>
> () IKG3DModel:SetDetailColor(nColor1, nColor2, nColor3)

设置三段整型颜色参数。

* <h4 id="LuaModel_ExecuteCommand">Cmd</h4>
> () IKG3DModel:Cmd(szCommand)

向引擎投递一条模型命令字符串。

* <h4 id="LuaModel_SetImportance">SetImportance</h4>
> () IKG3DModel:SetImportance(fValue)

设置模型的重要度（第 2 个参数必须是 number）。

* <h4 id="LuaModel_GetFaceDefinition">GetFaceDefinition</h4>
> (string, number[, string]) IKG3DModel:GetFaceDefinition()

异步获取脸型定义数据。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaModel_SetFaceDefinition">SetFaceDefinition</h4>
> () IKG3DModel:SetFaceDefinition(boneParams, nRoleType, decals, nFacePartID)

设置脸型定义数据。

- `boneParams` 必须是 table（从 `0` 开始的连续下标），每个元素必须是 number。
- `nRoleType` 必须是 number。
- `decals` 必须是 table（从 `0` 开始的连续下标），每个元素是 table，至少包含 `nShowID` / `nColorID` 两个 number 字段，并可选包含 `bUse`、`fValue1/fValue2/fValue3`。
- `nFacePartID` 必须是 number。

实现会构造两段 native 数据块并投递到引擎。

* <h4 id="LuaModel_SetFaceBoneParams">SetFaceBoneParams</h4>
> () IKG3DModel:SetFaceBoneParams(boneParams)

设置面部骨骼参数数组。

- `boneParams` 必须是 table（从 `0` 开始的连续下标），每个元素必须是 number。

* <h4 id="LuaModel_SetFaceDecals">SetFaceDecals</h4>
> () IKG3DModel:SetFaceDecals(nRoleType, decals)

设置面部贴花数据。

- `nRoleType` 必须是 number。
- `decals` 是 table（从 `0` 开始的连续下标），每个元素是包含 `nShowID` / `nColorID` 以及可选 `bUse`、`fValue1/fValue2/fValue3` 的 table。

* <h4 id="LuaModel_LoadFaceDefinitionINI">LoadFaceDefinitionINI</h4>
> () IKG3DModel:LoadFaceDefinitionINI(szFileName[, bCallBack])

从 INI 文件加载脸型数据。

- 允许 2 或 3 个参数（包含 `self`）。
- `szFileName` 必须是非空字符串。
- `bCallBack`（可选）用 `lua_toboolean` 读取。

* <h4 id="LuaModel_SaveFaceDefinitionFileHD">SaveFaceDefinitionFileHD</h4>
> () IKG3DModel:SaveFaceDefinitionFileHD(szFileName[, bCallBack])

把脸型数据（HD）保存到 INI 文件。

- 允许 2 或 3 个参数（包含 `self`）。
- `szFileName` 必须是非空字符串。
- `bCallBack`（可选）用 `lua_toboolean` 读取。

* <h4 id="LuaModel_SetFacePartID">SetFacePartID</h4>
> () IKG3DModel:SetFacePartID(nFacePartID)

设置 FacePartID。

* <h4 id="LuaModel_GetFacePartID">GetFacePartID</h4>
> (string, number[, string]) IKG3DModel:GetFacePartID()

异步查询 FacePartID。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaModel_SetForceRealInterpolate">SetForceRealInterpolate</h4>
> () IKG3DModel:SetForceRealInterpolate(bForceRealInterpolate)

设置是否强制真实插值。

* <h4 id="LuaModel_HideMeshPointOutsideCloak">HideMeshPointOutsideCloak</h4>
> () IKG3DModel:HideMeshPointOutsideCloak(modelCloak)

请求隐藏披风外侧的网格点。

注意：当前实现里披风模型 ID 读取成了参数 1（即 `self`），而不是参数 2，因此 `modelCloak` 实际上被忽略。

* <h4 id="LuaModel_ClearHideMeshPointOutsideCloak">ClearHideMeshPointOutsideCloak</h4>
> () IKG3DModel:ClearHideMeshPointOutsideCloak()

清理“披风外侧网格点隐藏”状态。

* <h4 id="LuaModel_Find">Find</h4>
> (string, number[, string]) IKG3DModel:Find(pcszName)

异步查找请求。

成功时返回 `"_call_id", callID`；失败时返回 `"_error0"`。

* <h4 id="LuaModel_Equal">__eq</h4>
> (bool) IKG3DModel:__eq(other)

比较两个模型 userdata 是否相等。

* <h4 id="LuaModel_GC">__gc</h4>
> () IKG3DModel:__gc()

GC 回调（仅在启用 `KGUI_MODEL_GC_API` 时存在）。

注意：实现里刻意不在 GC 时执行 `Release`，以避免 Lua 侧资源生命周期不严谨导致的异常。
