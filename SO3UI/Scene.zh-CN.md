[English](./Scene.md) | 中文

# 场景坐标函数（SO3UI）

SO3UI 模块提供的场景和坐标变换函数。

源码：`Source/Client/SO3UI/krepresentscripttable.cpp`

---

## 坐标变换

### Scene_GetCharacterTopScreenPos {#Scene_GetCharacterTopScreenPos}

```lua
nX, nY = Scene_GetCharacterTopScreenPos(dwID, nTargetType)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwID | `number` | 角色 ID |
| nTargetType | `number` | 目标类型常量（`TARGET.*`） |

**返回：** `number, number` - 屏幕 X 和 Y 坐标

获取角色头顶的屏幕位置。

> ⚠️ **线程安全：** 必须在主线程调用或通过 `PostThreadCall` 调用。

---

### Scene_GetCharacterTop {#Scene_GetCharacterTop}

```lua
fX, fY, fZ = Scene_GetCharacterTop(dwID, nTargetType)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwID | `number` | 角色 ID |
| nTargetType | `number` | 目标类型常量 |

**返回：** `number, number, number` - 角色头顶的场景 X, Y, Z 坐标

获取角色头顶的场景位置。

> ⚠️ **线程安全：** 必须在主线程调用或通过 `PostThreadCall` 调用。

---

### Scene_ScenePointToScreenPoint {#Scene_ScenePointToScreenPoint}

```lua
nX, nY = Scene_ScenePointToScreenPoint(fSceneX, fSceneY, fSceneZ)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| fSceneX | `number` | 场景 X 坐标 |
| fSceneY | `number` | 场景 Y 坐标 |
| fSceneZ | `number` | 场景 Z 坐标 |

**返回：** `number, number` - 屏幕 X 和 Y 坐标

将场景坐标转换为屏幕坐标。

> ⚠️ **线程安全：** 必须在主线程调用或通过 `PostThreadCall` 调用。

---

### Scene_GameWorldPositionToScenePosition {#Scene_GameWorldPositionToScenePosition}

```lua
fSceneX, fSceneY, fSceneZ = Scene_GameWorldPositionToScenePosition(nGameX, nGameY, nGameZ)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| nGameX | `number` | 游戏世界 X 坐标 |
| nGameY | `number` | 游戏世界 Y 坐标 |
| nGameZ | `number` | 游戏世界 Z 坐标 |

**返回：** `number, number, number` - 场景 X, Y, Z 坐标

将游戏世界位置转换为场景位置。

---

### Scene_ScenePositionToGameWorldPosition {#Scene_ScenePositionToGameWorldPosition}

```lua
nGameX, nGameY, nGameZ = Scene_ScenePositionToGameWorldPosition(fSceneX, fSceneY, fSceneZ)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| fSceneX | `number` | 场景 X 坐标 |
| fSceneY | `number` | 场景 Y 坐标 |
| fSceneZ | `number` | 场景 Z 坐标 |

**返回：** `number, number, number` - 游戏世界 X, Y, Z 坐标

将场景位置转换为游戏世界位置。

---

### Scene_GameWorldPositionToScreenPoint {#Scene_GameWorldPositionToScreenPoint}

```lua
nX, nY = Scene_GameWorldPositionToScreenPoint(nGameX, nGameY, nGameZ)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| nGameX | `number` | 游戏世界 X 坐标 |
| nGameY | `number` | 游戏世界 Y 坐标 |
| nGameZ | `number` | 游戏世界 Z 坐标 |

**返回：** `number, number` - 屏幕 X 和 Y 坐标

将游戏世界位置直接转换为屏幕坐标。

> ⚠️ **线程安全：** 必须在主线程调用或通过 `PostThreadCall` 调用。

---

### Scene_PlaneGameWorldPosToScene {#Scene_PlaneGameWorldPosToScene}

```lua
fX, fY = Scene_PlaneGameWorldPosToScene(nGameX, nGameY)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| nGameX | `number` | 游戏世界 X 坐标 |
| nGameY | `number` | 游戏世界 Y 坐标 |

**返回：** `number, number` - 场景平面 X 和 Y

将游戏世界平面位置转换为场景位置（2D）。

---

## 场景对象操作

### Scene_SelectObject {#Scene_SelectObject}

```lua
Scene_SelectObject(dwID, nTargetType)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwID | `number` | 对象 ID |
| nTargetType | `number` | 目标类型常量 |

**返回：** `void`

选择场景对象。

---

### SceneObject_SetBrightness {#SceneObject_SetBrightness}

```lua
SceneObject_SetBrightness(dwID, nTargetType, fBrightness)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwID | `number` | 对象 ID |
| nTargetType | `number` | 目标类型常量 |
| fBrightness | `number` | 亮度值（0.0-1.0） |

**返回：** `void`

设置场景对象的亮度。

---

### SceneObject_SetTitleEffect {#SceneObject_SetTitleEffect}

```lua
SceneObject_SetTitleEffect(dwID, nTargetType, szEffect)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwID | `number` | 对象 ID |
| nTargetType | `number` | 目标类型常量 |
| szEffect | `string` | 特效名称 |

**返回：** `void`

设置场景对象的称号特效。

---

## 头顶显示

### SetGlobalTopHeadFlag {#SetGlobalTopHeadFlag}

```lua
SetGlobalTopHeadFlag(nFlag)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| nFlag | `number` | 标志值 |

**返回：** `void`

设置全局头顶显示标志。

---

### GetGlobalTopHeadFlag {#GetGlobalTopHeadFlag}

```lua
nFlag = GetGlobalTopHeadFlag()
```

**返回：** `number` - 当前头顶标志

获取全局头顶显示标志。

---

### SetGlobalTopIntelligenceLife {#SetGlobalTopIntelligenceLife}

```lua
SetGlobalTopIntelligenceLife(bShow)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| bShow | `boolean` | 是否显示灵兽头顶 |

**返回：** `void`

设置是否显示灵兽（宠物）头顶显示。

> **注意：** 这是 addonapi.lua 中定义的 Lua 封装函数

---

### GetGlobalTopIntelligenceLife {#GetGlobalTopIntelligenceLife}

```lua
bShow = GetGlobalTopIntelligenceLife()
```

**返回：** `boolean` - 灵兽头顶是否显示

获取灵兽头顶是否显示。

> **注意：** 这是 addonapi.lua 中定义的 Lua 封装函数

---

## 目标选择

### TargetSelection_AttachSceneObject {#TargetSelection_AttachSceneObject}

```lua
TargetSelection_AttachSceneObject(dwID, nTargetType)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwID | `number` | 对象 ID |
| nTargetType | `number` | 目标类型常量 |

**返回：** `void`

为场景对象附加目标选择视觉效果。

---

### TargetSelection_DetachSceneObject {#TargetSelection_DetachSceneObject}

```lua
TargetSelection_DetachSceneObject(dwID, nTargetType)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| dwID | `number` | 对象 ID |
| nTargetType | `number` | 目标类型常量 |

**返回：** `void`

从场景对象移除目标选择视觉效果。

---

## 标题字幕

### Global_SetCaptionParams {#Global_SetCaptionParams}

```lua
Global_SetCaptionParams(tParams)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| tParams | `table` | 标题参数 |

**返回：** `void`

设置全局标题显示参数。

---

### Global_GetCaptionFontConfig {#Global_GetCaptionFontConfig}

```lua
tConfig = Global_GetCaptionFontConfig()
```

**返回：** `table` - 标题字体配置

获取全局标题字体配置。

---

## 已禁用函数

以下函数存在于源码中，但在 addon API 中被注释掉，无法使用：

### ~~Global_UpdateHeadTopPosition~~ {#Global_UpdateHeadTopPosition}

⚠️ **已禁用** - 此函数已被注释。

```lua
-- 在 addonapi.lua 中被注释
-- Global_UpdateHeadTopPosition(dwID, nTargetType)
```
