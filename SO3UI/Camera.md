English | [中文](./Camera.zh-CN.md)

# Camera Functions (SO3UI)

Camera control and parameter functions provided by SO3UI module.

Source: `Source/Client/SO3UI/krepresentscripttable.cpp`

---

## Camera Parameter Functions

### Camera_GetRTParams {#Camera_GetRTParams}

```lua
fLookAtX, fLookAtY, fLookAtZ, fAlpha, fBeta, fDistance = Camera_GetRTParams()
```

**Returns:**
- `fLookAtX` - Look-at point X coordinate
- `fLookAtY` - Look-at point Y coordinate
- `fLookAtZ` - Look-at point Z coordinate
- `fAlpha` - Alpha angle (horizontal rotation)
- `fBeta` - Beta angle (vertical rotation)
- `fDistance` - Camera distance from look-at point

Get the current camera real-time parameters.

> ⚠️ **Thread Safety:** Should be called from main thread.

---

### Camera_GetParams {#Camera_GetParams}

```lua
tParams = Camera_GetParams()
```

**Returns:** `table` - Camera parameters table containing:
- `fLookAtX`, `fLookAtY`, `fLookAtZ` - Look-at position
- `fAlpha`, `fBeta` - Rotation angles
- `fDistance` - Distance
- Additional camera state information

Get the camera parameters as a table.

---

## Related Camera APIs

For camera control via KScene objects, see:
- [SO3World Camera](../SO3World/Camera.md) - KScene:GetCamera, SetCamera, FreeLookAt etc.

---

## Disabled Functions

The following camera functions exist but are restricted:

### ~~Camera Direct Control~~ {#CameraDirectControl}

⚠️ **Not directly exported** - Camera manipulation is done through KScene object methods.

```lua
-- Use KScene methods instead:
-- local scene = Station.Lookup("Topmost/Scene").hScene
-- scene:GetCamera(...)
-- scene:SetCamera(...)
```
