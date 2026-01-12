[English](./Scene.md) | 中文

# 场景坐标函数

> ⚠️ **注意：** 这些函数由 **SO3UI** 模块提供，而非 KGUI。
>
> 请参阅 [SO3UI 场景文档](../../SO3UI/Scene.zh-CN.md) 获取包含正确源码引用的权威文档。

此文件保留用于向后兼容。所有 Scene_* 函数定义在 `Source/Client/SO3UI/krepresentscripttable.cpp` 中。

---

## 快速参考

| 函数 | 说明 |
|------|------|
| [`Scene_GetCharacterTopScreenPos`](../../SO3UI/Scene.zh-CN.md#Scene_GetCharacterTopScreenPos) | 获取角色头顶屏幕位置 |
| [`Scene_GetCharacterTop`](../../SO3UI/Scene.zh-CN.md#Scene_GetCharacterTop) | 获取角色头顶场景位置 |
| [`Scene_ScenePointToScreenPoint`](../../SO3UI/Scene.zh-CN.md#Scene_ScenePointToScreenPoint) | 场景坐标转屏幕坐标 |
| [`Scene_GameWorldPositionToScenePosition`](../../SO3UI/Scene.zh-CN.md#Scene_GameWorldPositionToScenePosition) | 游戏世界转场景 |
| [`Scene_ScenePositionToGameWorldPosition`](../../SO3UI/Scene.zh-CN.md#Scene_ScenePositionToGameWorldPosition) | 场景转游戏世界 |
| [`Scene_GameWorldPositionToScreenPoint`](../../SO3UI/Scene.zh-CN.md#Scene_GameWorldPositionToScreenPoint) | 游戏世界转屏幕 |
| [`Scene_PlaneGameWorldPosToScene`](../../SO3UI/Scene.zh-CN.md#Scene_PlaneGameWorldPosToScene) | 2D游戏世界转场景 |
| [`Scene_SelectObject`](../../SO3UI/Scene.zh-CN.md#Scene_SelectObject) | 选择场景对象 |
| [`SceneObject_SetBrightness`](../../SO3UI/Scene.zh-CN.md#SceneObject_SetBrightness) | 设置对象亮度 |
| [`SceneObject_SetTitleEffect`](../../SO3UI/Scene.zh-CN.md#SceneObject_SetTitleEffect) | 设置称号特效 |
| [`SetGlobalTopHeadFlag`](../../SO3UI/Scene.zh-CN.md#SetGlobalTopHeadFlag) | 设置头顶标志 |
| [`GetGlobalTopHeadFlag`](../../SO3UI/Scene.zh-CN.md#GetGlobalTopHeadFlag) | 获取头顶标志 |
| [`TargetSelection_AttachSceneObject`](../../SO3UI/Scene.zh-CN.md#TargetSelection_AttachSceneObject) | 附加选择视觉 |
| [`TargetSelection_DetachSceneObject`](../../SO3UI/Scene.zh-CN.md#TargetSelection_DetachSceneObject) | 移除选择视觉 |
| [`Global_SetCaptionParams`](../../SO3UI/Scene.zh-CN.md#Global_SetCaptionParams) | 设置标题参数 |
| [`Global_GetCaptionFontConfig`](../../SO3UI/Scene.zh-CN.md#Global_GetCaptionFontConfig) | 获取标题字体配置 |
