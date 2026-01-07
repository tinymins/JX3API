# IKG3DModel

Many getters in this metatable are asynchronous: they post a request and return a key/value pair `"_call_id", <number>`.

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
- `__gc` (only when `KGUI_MODEL_GC_API` is enabled)

* <h4 id="LuaModel_RegisterEventHandler">RegisterEventHandler</h4>
> () IKG3DModel:RegisterEventHandler()

Registers the model's event handler with the underlying event adaptor.

* <h4 id="LuaModel_UnregisterEventHandler">UnregisterEventHandler</h4>
> () IKG3DModel:UnregisterEventHandler()

Unregisters the model's event handler.

* <h4 id="LuaModel_PlayAnimation">PlayAnimation</h4>
> () IKG3DModel:PlayAnimation(szPlayType, szAnimationName, fSpeed, nOffsetTime[, fTweenTime])

Requests the model to play an animation.

- Requires at least 5 Lua stack values (including `self`).
- `szPlayType` is interpreted as a string; recognized values are `"loop"`, `"once"`, `"last"`.
- `szAnimationName` is read as string; if it is `nil` the function becomes a no-op and still returns normally.
- `fTweenTime` is optional and read from argument 6 when provided.

This call posts an async model API request and returns no values.

* <h4 id="LuaModel_PauseAnimation">PauseAnimation</h4>
> () IKG3DModel:PauseAnimation(bPause)

Pauses or resumes the current animation.

* <h4 id="LuaModel_LoadMaterialFromFile">LoadMaterialFromFile</h4>
> () IKG3DModel:LoadMaterialFromFile(szFilePath)

Loads material data from `szFilePath` (non-empty string).

* <h4 id="LuaModel_SetTranslation">SetTranslation</h4>
> () IKG3DModel:SetTranslation(x, y, z)

Sets the model translation.

* <h4 id="LuaModel_SetRotation">SetRotation</h4>
> () IKG3DModel:SetRotation(x, y, z, w)

Sets the model rotation (4 floats).

* <h4 id="LuaModel_SetScaling">SetScaling</h4>
> () IKG3DModel:SetScaling(x, y, z)

Sets the model scaling.

* <h4 id="LuaModel_GetTranslation">GetTranslation</h4>
> (string, number[, string]) IKG3DModel:GetTranslation()

Posts an async query for the model translation.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaModel_GetRotation">GetRotation</h4>
> (string, number[, string]) IKG3DModel:GetRotation()

Posts an async query for the model rotation.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaModel_GetScaling">GetScaling</h4>
> (string, number[, string]) IKG3DModel:GetScaling()

Posts an async query for the model scaling.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaModel_BindToSocket">BindToSocket</h4>
> () IKG3DModel:BindToSocket(otherModel[, szSocket])

Binds this model to another model at a socket name.

- Accepts 2 or 3 arguments (including `self`).
- If `szSocket` is omitted, an empty string is used.

* <h4 id="LuaModel_BindToBone">BindToBone</h4>
> () IKG3DModel:BindToBone(otherModel[, szBone])

Binds this model to another model at a bone name.

- Accepts 2 or 3 arguments (including `self`).
- If `szBone` is omitted, an empty string is used.

* <h4 id="LuaModel_UnbindFromOther">UnbindFromOther</h4>
> () IKG3DModel:UnbindFromOther([parentModel])

Unbinds this model from another model.

- Accepts 1 or 2 arguments (including `self`).
- If `parentModel` is omitted, the internal parent id argument defaults to `-1`.

* <h4 id="LuaModel_SetAlpha">SetAlpha</h4>
> () IKG3DModel:SetAlpha(fAlpha)

Sets alpha (float).

* <h4 id="LuaModel_SetHighLightLevel">SetHighLightLevel</h4>
> () IKG3DModel:SetHighLightLevel(fIllumination)

Sets highlight level (float).

* <h4 id="LuaModel_GetHightLightLevel">GetHightLightLevel</h4>
> (string, number[, string]) IKG3DModel:GetHightLightLevel()

Posts an async query for the highlight level.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaModel_GetAlpha">GetAlpha</h4>
> (string, number[, string]) IKG3DModel:GetAlpha()

Posts an async query for alpha.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaModel_Release">Release</h4>
> () IKG3DModel:Release()

Releases the model.

In builds with `KGUI_MODEL_GC_API`, this also removes the model from the internal active-model tracking set.

* <h4 id="LuaModel_Attach">Attach</h4>
> () IKG3DModel:Attach(parentModel)

Attaches this model to `parentModel`.

* <h4 id="LuaModel_Detach">Detach</h4>
> () IKG3DModel:Detach(rhsModel)

Detaches this model from `rhsModel`.

* <h4 id="LuaModel_SetYaw">SetYaw</h4>
> () IKG3DModel:SetYaw(fYaw)

Sets yaw (float).

* <h4 id="LuaModel_SetFaceMotionMode">SetFaceMotionMode</h4>
> () IKG3DModel:SetFaceMotionMode()

Enables face motion mode for this model.

* <h4 id="LuaModel_SetDetail">SetDetail</h4>
> () IKG3DModel:SetDetail(nColorChannelTable, nColorChannel)

Sets face detail/channel configuration.

* <h4 id="LuaModel_SetDetailColor">SetDetailColor</h4>
> () IKG3DModel:SetDetailColor(nColor1, nColor2, nColor3)

Sets three integer color parameters.

* <h4 id="LuaModel_ExecuteCommand">Cmd</h4>
> () IKG3DModel:Cmd(szCommand)

Posts a model command string to the underlying engine.

* <h4 id="LuaModel_SetImportance">SetImportance</h4>
> () IKG3DModel:SetImportance(fValue)

Sets model importance (requires argument 2 to be a number).

* <h4 id="LuaModel_GetFaceDefinition">GetFaceDefinition</h4>
> (string, number[, string]) IKG3DModel:GetFaceDefinition()

Posts an async request for the model face definition.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaModel_SetFaceDefinition">SetFaceDefinition</h4>
> () IKG3DModel:SetFaceDefinition(boneParams, nRoleType, decals, nFacePartID)

Sets face definition data.

- `boneParams` must be a table indexed from `0` upwards; each entry must be a number.
- `nRoleType` must be a number.
- `decals` must be a table indexed from `0` upwards; each entry is a table containing at least `nShowID` and `nColorID` numeric fields, plus optional fields `bUse` and `fValue1/fValue2/fValue3`.
- `nFacePartID` must be a number.

The function builds native data blobs and posts them to the engine.

* <h4 id="LuaModel_SetFaceBoneParams">SetFaceBoneParams</h4>
> () IKG3DModel:SetFaceBoneParams(boneParams)

Sets bone parameter array used for face configuration.

- `boneParams` must be a table indexed from `0` upwards; each entry must be a number.

* <h4 id="LuaModel_SetFaceDecals">SetFaceDecals</h4>
> () IKG3DModel:SetFaceDecals(nRoleType, decals)

Sets face decal data.

- `nRoleType` must be a number.
- `decals` is a table indexed from `0` upwards; each entry is a table containing `nShowID`, `nColorID` and optional `bUse` and `fValue1/fValue2/fValue3`.

* <h4 id="LuaModel_LoadFaceDefinitionINI">LoadFaceDefinitionINI</h4>
> () IKG3DModel:LoadFaceDefinitionINI(szFileName[, bCallBack])

Loads face definition from an INI file.

- Accepts 2 or 3 arguments (including `self`).
- `szFileName` must be a non-empty string.
- `bCallBack` is read via `lua_toboolean` when provided.

* <h4 id="LuaModel_SaveFaceDefinitionFileHD">SaveFaceDefinitionFileHD</h4>
> () IKG3DModel:SaveFaceDefinitionFileHD(szFileName[, bCallBack])

Saves face definition data (HD) to an INI file.

- Accepts 2 or 3 arguments (including `self`).
- `szFileName` must be a non-empty string.
- `bCallBack` is read via `lua_toboolean` when provided.

* <h4 id="LuaModel_SetFacePartID">SetFacePartID</h4>
> () IKG3DModel:SetFacePartID(nFacePartID)

Sets face part id.

* <h4 id="LuaModel_GetFacePartID">GetFacePartID</h4>
> (string, number[, string]) IKG3DModel:GetFacePartID()

Posts an async query for face part id.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaModel_SetForceRealInterpolate">SetForceRealInterpolate</h4>
> () IKG3DModel:SetForceRealInterpolate(bForceRealInterpolate)

Sets whether to force real interpolation.

* <h4 id="LuaModel_HideMeshPointOutsideCloak">HideMeshPointOutsideCloak</h4>
> () IKG3DModel:HideMeshPointOutsideCloak(modelCloak)

Requests to hide mesh points outside cloak.

Note: in the current implementation, the cloak id is read from argument 1 instead of argument 2, so `modelCloak` is effectively ignored.

* <h4 id="LuaModel_ClearHideMeshPointOutsideCloak">ClearHideMeshPointOutsideCloak</h4>
> () IKG3DModel:ClearHideMeshPointOutsideCloak()

Clears the “hide mesh point outside cloak” state.

* <h4 id="LuaModel_Find">Find</h4>
> (string, number[, string]) IKG3DModel:Find(pcszName)

Posts an async find request.

On success, returns `"_call_id", callID`. On failure, returns `"_error0"`.

* <h4 id="LuaModel_Equal">__eq</h4>
> (bool) IKG3DModel:__eq(other)

Compares two model userdata values.

* <h4 id="LuaModel_GC">__gc</h4>
> () IKG3DModel:__gc()

Garbage-collection handler (only available when `KGUI_MODEL_GC_API` is enabled).

Note: the implementation deliberately does not post a `Release` on GC due to Lua-side lifetime issues.
