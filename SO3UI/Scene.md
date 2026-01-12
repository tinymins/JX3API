English | [中文](./Scene.zh-CN.md)

# Scene Coordinate Functions (SO3UI)

Scene and coordinate transformation functions provided by SO3UI module.

Source: `Source/Client/SO3UI/krepresentscripttable.cpp`

---

## Coordinate Transformation

### Scene_GetCharacterTopScreenPos {#Scene_GetCharacterTopScreenPos}

```lua
nX, nY = Scene_GetCharacterTopScreenPos(dwID, nTargetType)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwID | `number` | Character ID |
| nTargetType | `number` | Target type constant (`TARGET.*`) |

**Returns:** `number, number` - Screen X and Y coordinates

Get the screen position of a character's head top.

> ⚠️ **Thread Safety:** Must be called from main thread or via `PostThreadCall`.

---

### Scene_GetCharacterTop {#Scene_GetCharacterTop}

```lua
fX, fY, fZ = Scene_GetCharacterTop(dwID, nTargetType)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwID | `number` | Character ID |
| nTargetType | `number` | Target type constant |

**Returns:** `number, number, number` - Scene X, Y, Z coordinates of character head top

Get the scene position of a character's head top.

> ⚠️ **Thread Safety:** Must be called from main thread or via `PostThreadCall`.

---

### Scene_ScenePointToScreenPoint {#Scene_ScenePointToScreenPoint}

```lua
nX, nY = Scene_ScenePointToScreenPoint(fSceneX, fSceneY, fSceneZ)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| fSceneX | `number` | Scene X coordinate |
| fSceneY | `number` | Scene Y coordinate |
| fSceneZ | `number` | Scene Z coordinate |

**Returns:** `number, number` - Screen X and Y coordinates

Convert scene coordinates to screen coordinates.

> ⚠️ **Thread Safety:** Must be called from main thread or via `PostThreadCall`.

---

### Scene_GameWorldPositionToScenePosition {#Scene_GameWorldPositionToScenePosition}

```lua
fSceneX, fSceneY, fSceneZ = Scene_GameWorldPositionToScenePosition(nGameX, nGameY, nGameZ)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nGameX | `number` | Game world X coordinate |
| nGameY | `number` | Game world Y coordinate |
| nGameZ | `number` | Game world Z coordinate |

**Returns:** `number, number, number` - Scene X, Y, Z coordinates

Convert game world position to scene position.

---

### Scene_ScenePositionToGameWorldPosition {#Scene_ScenePositionToGameWorldPosition}

```lua
nGameX, nGameY, nGameZ = Scene_ScenePositionToGameWorldPosition(fSceneX, fSceneY, fSceneZ)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| fSceneX | `number` | Scene X coordinate |
| fSceneY | `number` | Scene Y coordinate |
| fSceneZ | `number` | Scene Z coordinate |

**Returns:** `number, number, number` - Game world X, Y, Z coordinates

Convert scene position to game world position.

---

### Scene_GameWorldPositionToScreenPoint {#Scene_GameWorldPositionToScreenPoint}

```lua
nX, nY = Scene_GameWorldPositionToScreenPoint(nGameX, nGameY, nGameZ)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nGameX | `number` | Game world X coordinate |
| nGameY | `number` | Game world Y coordinate |
| nGameZ | `number` | Game world Z coordinate |

**Returns:** `number, number` - Screen X and Y coordinates

Convert game world position directly to screen point.

> ⚠️ **Thread Safety:** Must be called from main thread or via `PostThreadCall`.

---

### Scene_PlaneGameWorldPosToScene {#Scene_PlaneGameWorldPosToScene}

```lua
fX, fY = Scene_PlaneGameWorldPosToScene(nGameX, nGameY)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nGameX | `number` | Game world X coordinate |
| nGameY | `number` | Game world Y coordinate |

**Returns:** `number, number` - Scene plane X and Y

Convert game world plane position to scene position (2D).

---

## Scene Object Operations

### Scene_SelectObject {#Scene_SelectObject}

```lua
Scene_SelectObject(dwID, nTargetType)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwID | `number` | Object ID |
| nTargetType | `number` | Target type constant |

**Returns:** `void`

Select a scene object.

---

### SceneObject_SetBrightness {#SceneObject_SetBrightness}

```lua
SceneObject_SetBrightness(dwID, nTargetType, fBrightness)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwID | `number` | Object ID |
| nTargetType | `number` | Target type constant |
| fBrightness | `number` | Brightness value (0.0-1.0) |

**Returns:** `void`

Set the brightness of a scene object.

---

### SceneObject_SetTitleEffect {#SceneObject_SetTitleEffect}

```lua
SceneObject_SetTitleEffect(dwID, nTargetType, szEffect)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwID | `number` | Object ID |
| nTargetType | `number` | Target type constant |
| szEffect | `string` | Effect name |

**Returns:** `void`

Set the title effect of a scene object.

---

## Top Head Display

### SetGlobalTopHeadFlag {#SetGlobalTopHeadFlag}

```lua
SetGlobalTopHeadFlag(nFlag)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nFlag | `number` | Flag value |

**Returns:** `void`

Set the global top head display flag.

---

### GetGlobalTopHeadFlag {#GetGlobalTopHeadFlag}

```lua
nFlag = GetGlobalTopHeadFlag()
```

**Returns:** `number` - Current top head flag

Get the global top head display flag.

---

### SetGlobalTopIntelligenceLife {#SetGlobalTopIntelligenceLife}

```lua
SetGlobalTopIntelligenceLife(bShow)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| bShow | `boolean` | Whether to show intelligence life top head |

**Returns:** `void`

Set whether to show intelligence life (pet) top head display.

> **Note:** This is a Lua wrapper function defined in addonapi.lua

---

### GetGlobalTopIntelligenceLife {#GetGlobalTopIntelligenceLife}

```lua
bShow = GetGlobalTopIntelligenceLife()
```

**Returns:** `boolean` - Whether intelligence life top head is shown

Get whether intelligence life top head is shown.

> **Note:** This is a Lua wrapper function defined in addonapi.lua

---

## Target Selection

### TargetSelection_AttachSceneObject {#TargetSelection_AttachSceneObject}

```lua
TargetSelection_AttachSceneObject(dwID, nTargetType)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwID | `number` | Object ID |
| nTargetType | `number` | Target type constant |

**Returns:** `void`

Attach target selection visual to a scene object.

---

### TargetSelection_DetachSceneObject {#TargetSelection_DetachSceneObject}

```lua
TargetSelection_DetachSceneObject(dwID, nTargetType)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| dwID | `number` | Object ID |
| nTargetType | `number` | Target type constant |

**Returns:** `void`

Detach target selection visual from a scene object.

---

## Caption

### Global_SetCaptionParams {#Global_SetCaptionParams}

```lua
Global_SetCaptionParams(tParams)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| tParams | `table` | Caption parameters |

**Returns:** `void`

Set global caption display parameters.

---

### Global_GetCaptionFontConfig {#Global_GetCaptionFontConfig}

```lua
tConfig = Global_GetCaptionFontConfig()
```

**Returns:** `table` - Caption font configuration

Get global caption font configuration.

---

## Disabled Functions

The following functions exist in source but are commented out and cannot be used:

### ~~Global_UpdateHeadTopPosition~~ {#Global_UpdateHeadTopPosition}

⚠️ **Disabled** - This function is commented out.

```lua
-- Commented out in addonapi.lua
-- Global_UpdateHeadTopPosition(dwID, nTargetType)
```
