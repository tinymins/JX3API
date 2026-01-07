# IKG3DResourceManager

Methods:
- `NewModel`
- `Preload`
- `Postload`

* <h4 id="LuaModelMgr_NewModel">NewModel</h4>
> (IKG3DModel) IKG3DResourceManager:NewModel(szFilePath[, bLowTextureLOD[, bReLoad[, bAdjustByAnimation[, bMainPlayer[, nLodLevel[, parentModel]]]]]])

Creates (or reuses) a model instance from `szFilePath`.

- `szFilePath` must be a non-empty string.
- Optional flags are read via `lua_toboolean` and therefore accept any Lua value (truthy/falsy).
- If `nLodLevel` is provided and not `nil`, it is converted with `lua_tonumber` and applied to the model load options.
- If `parentModel` is provided, it is converted via `ToIKG3DObjID` and used as the parent model id.

Returns a new `IKG3DModel` userdata on success. Returns nothing on failure.

* <h4 id="LuaModelMgr_Preload">Preload</h4>
> () IKG3DResourceManager:Preload(files)

Preloads model resources listed in `files`.

- `files` must be a Lua table; the implementation iterates it with `lua_next` and reads each value as a non-empty string.
- If an entry ends with `.tani`, it is queued into an internal wait list; otherwise it is inserted into the model preload set.

This call schedules preload work and returns no values.

* <h4 id="LuaModelMgr_Postload">Postload</h4>
> () IKG3DResourceManager:Postload()

Releases resources that were preloaded by `Preload`.

The current implementation does not validate the Lua argument count; it simply triggers the underlying release operation.
