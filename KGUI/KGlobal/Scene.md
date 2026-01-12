English | [中文](./Scene.zh-CN.md)

# Scene Coordinate Functions

> ⚠️ **Note:** These functions are provided by the **SO3UI** module, not KGUI.
>
> See [SO3UI Scene Documentation](../../SO3UI/Scene.md) for the authoritative documentation with correct source references.

This file is preserved for backward compatibility. All Scene_* functions are defined in `Source/Client/SO3UI/krepresentscripttable.cpp`.

---

## Quick Reference

| Function | Description |
|----------|-------------|
| [`Scene_GetCharacterTopScreenPos`](../../SO3UI/Scene.md#Scene_GetCharacterTopScreenPos) | Get character head screen position |
| [`Scene_GetCharacterTop`](../../SO3UI/Scene.md#Scene_GetCharacterTop) | Get character head scene position |
| [`Scene_ScenePointToScreenPoint`](../../SO3UI/Scene.md#Scene_ScenePointToScreenPoint) | Convert scene to screen coords |
| [`Scene_GameWorldPositionToScenePosition`](../../SO3UI/Scene.md#Scene_GameWorldPositionToScenePosition) | Convert game world to scene |
| [`Scene_ScenePositionToGameWorldPosition`](../../SO3UI/Scene.md#Scene_ScenePositionToGameWorldPosition) | Convert scene to game world |
| [`Scene_GameWorldPositionToScreenPoint`](../../SO3UI/Scene.md#Scene_GameWorldPositionToScreenPoint) | Convert game world to screen |
| [`Scene_PlaneGameWorldPosToScene`](../../SO3UI/Scene.md#Scene_PlaneGameWorldPosToScene) | Convert 2D game world to scene |
| [`Scene_SelectObject`](../../SO3UI/Scene.md#Scene_SelectObject) | Select scene object |
| [`SceneObject_SetBrightness`](../../SO3UI/Scene.md#SceneObject_SetBrightness) | Set object brightness |
| [`SceneObject_SetTitleEffect`](../../SO3UI/Scene.md#SceneObject_SetTitleEffect) | Set title effect |
| [`SetGlobalTopHeadFlag`](../../SO3UI/Scene.md#SetGlobalTopHeadFlag) | Set top head flag |
| [`GetGlobalTopHeadFlag`](../../SO3UI/Scene.md#GetGlobalTopHeadFlag) | Get top head flag |
| [`TargetSelection_AttachSceneObject`](../../SO3UI/Scene.md#TargetSelection_AttachSceneObject) | Attach selection visual |
| [`TargetSelection_DetachSceneObject`](../../SO3UI/Scene.md#TargetSelection_DetachSceneObject) | Detach selection visual |
| [`Global_SetCaptionParams`](../../SO3UI/Scene.md#Global_SetCaptionParams) | Set caption params |
| [`Global_GetCaptionFontConfig`](../../SO3UI/Scene.md#Global_GetCaptionFontConfig) | Get caption font config |

```lua
-- Commented out
-- Global_UpdateHeadTopPosition(dwID, nTargetType)
```
