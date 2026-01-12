# 系统函数

系统信息和实用工具函数。

---

## 版本与客户端信息

### GetVersion {#GetVersion}

```lua
nMajor, nMinor, szVersion = GetVersion()
```

**返回:**
- `number` - 主版本号
- `number` - 次版本号
- `string` - 版本字符串（如 "zhcn"、"vivn"）

获取游戏客户端版本信息。

---

### IsDebugClient {#IsDebugClient}

```lua
bDebug = IsDebugClient()
```

**返回:** `boolean` - 如果是调试客户端返回 true

检查当前客户端是否为调试版本。

---

### GetCurrentProcessID {#GetCurrentProcessID}

```lua
nPID = GetCurrentProcessID()
```

**返回:** `number` - 进程 ID

获取当前进程 ID。

---

### GetMachineConfig {#GetMachineConfig}

```lua
tConfig = GetMachineConfig()
```

**返回:** `table` - 机器配置信息

获取机器硬件配置。

---

## 用户与服务器信息

### GetUserServer {#GetUserServer}

```lua
szServer = GetUserServer()
```

**返回:** `string` - 服务器名称

获取当前服务器名称。

---

### GetUserRoleName {#GetUserRoleName}

```lua
szName = GetUserRoleName()
```

**返回:** `string` - 角色名称

获取当前角色名称。

---

### GetUserAccount {#GetUserAccount}

```lua
szAccount = GetUserAccount()
```

**返回:** `string` - 账号名称

获取用户账号名称。

---

### Login_GetAccount {#Login_GetAccount}

```lua
szAccount = Login_GetAccount()
```

**返回:** `string` - 登录账号

获取登录账号名称。

---

### GetGatewayServer {#GetGatewayServer}

```lua
tServer = GetGatewayServer()
```

**返回:** `table` - 网关服务器信息

获取合服的网关服务器信息。

---

### GetInterworkingServers {#GetInterworkingServers}

```lua
tServers = GetInterworkingServers()
```

**返回:** `table` - 互通服务器列表

获取互通服务器列表。

---

## 线程与调试

### IsMultiThread {#IsMultiThread}

```lua
bMultiThread = IsMultiThread()
```

**返回:** `boolean` - 如果在多线程模式返回 true

检查当前上下文是否在多线程模式。

---

### ReloadUIAddon {#ReloadUIAddon}

```lua
ReloadUIAddon()
```

**返回:** `void`

重新加载 UI 插件。

---

### EnableDebugEnv {#EnableDebugEnv}

```lua
EnableDebugEnv(bEnable)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| bEnable | `boolean` | 启用或禁用 |

**返回:** `void`

启用或禁用调试环境。

别名：`OpenDebug`

---

## 位运算

### BitwiseAnd {#BitwiseAnd}

```lua
nResult = BitwiseAnd(nA, nB)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nA | `number` | 第一个操作数 |
| nB | `number` | 第二个操作数 |

**返回:** `number` - 按位与结果

执行按位与运算。

---

### BitwiseOr {#BitwiseOr}

```lua
nResult = BitwiseOr(nA, nB)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nA | `number` | 第一个操作数 |
| nB | `number` | 第二个操作数 |

**返回:** `number` - 按位或结果

执行按位或运算。

---

### BitwiseXor {#BitwiseXor}

```lua
nResult = BitwiseXor(nA, nB)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nA | `number` | 第一个操作数 |
| nB | `number` | 第二个操作数 |

**返回:** `number` - 按位异或结果

执行按位异或运算。

---

### GetNumberBit {#GetNumberBit}

```lua
nBit = GetNumberBit(nValue, nBitIndex)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nValue | `number` | 数值 |
| nBitIndex | `number` | 位索引（从 0 开始） |

**返回:** `number` - 位值（0 或 1）

获取数字的特定位。

---

### SetNumberBit {#SetNumberBit}

```lua
nResult = SetNumberBit(nValue, nBitIndex, nBit)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| nValue | `number` | 原始数值 |
| nBitIndex | `number` | 位索引（从 0 开始） |
| nBit | `number` | 位值（0 或 1） |

**返回:** `number` - 修改后的数值

设置数字的特定位。

---

## 命令执行

### rlcmd {#rlcmd}

```lua
rlcmd(szCommand)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szCommand | `string` | 命令字符串 |

**返回:** `void`

执行 RL 命令。

---

### k3dcmd {#k3dcmd}

```lua
k3dcmd(szCommand)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szCommand | `string` | 命令字符串 |

**返回:** `void`

执行 K3D 命令。

---

## 移动串流

### SM_IsEnable {#SM_IsEnable}

```lua
bEnabled = SM_IsEnable()
```

**返回:** `boolean` - 如果串流模式启用返回 true

检查串流模式是否启用。

---

### IsMobileStreamingEnable {#IsMobileStreamingEnable}

```lua
bEnabled = IsMobileStreamingEnable()
```

**返回:** `boolean` - 如果移动串流启用返回 true

检查移动串流是否启用。

---

## 插件接口

### PluginInterface {#PluginInterface}

```lua
PluginInterface(szMethod, ...)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szMethod | `string` | 方法名称 |
| ... | `any` | 方法参数 |

**返回:** `any` - 方法返回值

调用插件接口方法。
