# IKG3DResourceManager

Methods:
- `NewModel`
- `Preload`
- `Postload`

* <h4 id="LuaModelMgr_NewModel">NewModel</h4>
> (IKG3DModel) IKG3DResourceManager:NewModel(szFilePath[, bLowTextureLOD[, bReLoad[, bAdjustByAnimation[, bMainPlayer[, nLodLevel[, parentModel]]]]]])

根据 `szFilePath` 创建（或复用）一个模型实例。

- `szFilePath` 必须是非空字符串。
- 这些可选布尔开关用 `lua_toboolean` 读取，因此 Lua 层传入任意值都会按“真/假”解释。
- 如果传入 `nLodLevel` 且不为 `nil`，会用 `lua_tonumber` 转换并写入加载选项。
- 如果传入 `parentModel`，会通过 `ToIKG3DObjID` 转成父模型 ID。

成功时返回一个新的 `IKG3DModel` userdata；失败时不返回值。

* <h4 id="LuaModelMgr_Preload">Preload</h4>
> () IKG3DResourceManager:Preload(files)

预加载 `files` 表中列出的模型资源。

- `files` 必须是 table；实现用 `lua_next` 遍历，读取每个 value 为非空字符串。
- 以 `.tani` 结尾的条目会进入内部等待队列；其他条目会被加入模型预加载集合。

该调用会提交预加载工作，不返回值。

* <h4 id="LuaModelMgr_Postload">Postload</h4>
> () IKG3DResourceManager:Postload()

释放 `Preload` 预加载的资源。

当前实现没有校验 Lua 传参个数，直接触发底层释放流程。
