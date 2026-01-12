English | [中文](./index.zh-CN.md)

# SO3UI

Game client UI integration module. Provides APIs for integrating the UI framework with the 3D game engine.

Source: `Source/Client/SO3UI/`

## Categories

| Category | Description | Source File |
|----------|-------------|-------------|
| [Network](./Network.md) | HTTP network request functions (CURL) | `kschemescripttable.cpp` |
| [Scene](./Scene.md) | Scene rendering and coordinate transformation | `krepresentscripttable.cpp` |
| [Camera](./Camera.md) | Camera control functions | `krepresentscripttable.cpp` |
| [Represent](./Represent.md) | Character and NPC representation | `krepresentscripttable.cpp` |

## Module Architecture

```
SO3UI (Game Client UI Integration)
├── Network Functions
│   ├── CURL_HttpPostEx, CURL_DownloadFile, CURL_Close
│   └── OpenBrowser
├── Scene Functions
│   ├── Scene_* coordinate transformation
│   ├── SceneObject_* manipulation
│   └── TopHead and Target Selection
├── Camera Functions
│   └── Camera_GetRTParams, Camera_GetParams
└── Represent Functions
    ├── Player_Get* resource functions
    ├── NPC_Get* resource functions
    └── Character_* model functions
```

## Notes

- **SO3UI** is the game client UI module that integrates with the 3D engine
- **KGUI** is the base UI framework; SO3UI extends it with game-specific functionality
- For game world logic APIs (KPlayer, KNpc, etc.), see [SO3World](../SO3World/index.md)
- For base UI framework APIs, see [KGUI](../KGUI/index.md)
