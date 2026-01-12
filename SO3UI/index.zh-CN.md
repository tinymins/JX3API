[English](./index.md) | 中文

# SO3UI

游戏客户端 UI 集成模块。提供将 UI 框架与 3D 游戏引擎集成的 API。

源码：`Source/Client/SO3UI/`

## 分类

| 分类 | 说明 | 源文件 |
|------|------|--------|
| [Network](./Network.zh-CN.md) | HTTP 网络请求函数 (CURL) | `kschemescripttable.cpp` |
| [Scene](./Scene.zh-CN.md) | 场景渲染和坐标变换 | `krepresentscripttable.cpp` |
| [Camera](./Camera.zh-CN.md) | 摄像机控制函数 | `krepresentscripttable.cpp` |
| [Represent](./Represent.zh-CN.md) | 角色和 NPC 表现 | `krepresentscripttable.cpp` |

## 模块架构

```
SO3UI（游戏客户端 UI 集成）
├── 网络函数
│   ├── CURL_HttpPostEx, CURL_DownloadFile, CURL_Close
│   └── OpenBrowser
├── 场景函数
│   ├── Scene_* 坐标变换
│   ├── SceneObject_* 操作
│   └── 头顶显示和目标选择
├── 摄像机函数
│   └── Camera_GetRTParams, Camera_GetParams
└── 表现函数
    ├── Player_Get* 资源函数
    ├── NPC_Get* 资源函数
    └── Character_* 模型函数
```

## 说明

- **SO3UI** 是与 3D 引擎集成的游戏客户端 UI 模块
- **KGUI** 是基础 UI 框架；SO3UI 在其基础上扩展了游戏特定功能
- 游戏世界逻辑 API（KPlayer, KNpc 等），请参阅 [SO3World](../SO3World/index.zh-CN.md)
- 基础 UI 框架 API，请参阅 [KGUI](../KGUI/index.zh-CN.md)
