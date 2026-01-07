[English](./WndTexture.md) | 中文

# WndTexture（纹理）

说明：

- `WndTexture` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

[`SetTexture`](#LuaTexture_SetTexture)

* <h4 id="LuaTexture_SetTexture">SetTexture</h4>

 > (`void`) WndTexture:SetTexture(`userdata` pp3DModel)

说明：

- 这里的参数不是文件路径；绑定实现会把 `pp3DModel` 当作 `IKG3DModel**` 来解引用并设置到纹理窗口。
