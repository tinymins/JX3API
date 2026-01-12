[English](./Camera.md) | 中文

# 摄像机函数（SO3UI）

SO3UI 模块提供的摄像机控制和参数函数。

源码：`Source/Client/SO3UI/krepresentscripttable.cpp`

---

## 摄像机参数函数

### Camera_GetRTParams {#Camera_GetRTParams}

```lua
fLookAtX, fLookAtY, fLookAtZ, fAlpha, fBeta, fDistance = Camera_GetRTParams()
```

**返回：**
- `fLookAtX` - 观察点 X 坐标
- `fLookAtY` - 观察点 Y 坐标
- `fLookAtZ` - 观察点 Z 坐标
- `fAlpha` - Alpha 角度（水平旋转）
- `fBeta` - Beta 角度（垂直旋转）
- `fDistance` - 摄像机到观察点的距离

获取当前摄像机的实时参数。

> ⚠️ **线程安全：** 应在主线程调用。

---

### Camera_GetParams {#Camera_GetParams}

```lua
tParams = Camera_GetParams()
```

**返回：** `table` - 摄像机参数表，包含：
- `fLookAtX`, `fLookAtY`, `fLookAtZ` - 观察点位置
- `fAlpha`, `fBeta` - 旋转角度
- `fDistance` - 距离
- 其他摄像机状态信息

以表格形式获取摄像机参数。

---

## 相关摄像机 API

通过 KScene 对象控制摄像机，请参阅：
- [SO3World 摄像机](../SO3World/Camera.zh-CN.md) - KScene:GetCamera, SetCamera, FreeLookAt 等

---

## 已禁用函数

以下摄像机函数存在但受限：

### ~~摄像机直接控制~~ {#CameraDirectControl}

⚠️ **未直接导出** - 摄像机操作通过 KScene 对象方法完成。

```lua
-- 使用 KScene 方法代替：
-- local scene = Station.Lookup("Topmost/Scene").hScene
-- scene:GetCamera(...)
-- scene:SetCamera(...)
```
