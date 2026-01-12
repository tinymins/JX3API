# System Functions

System information and utility functions.

---

## Version & Client Info

### GetVersion {#GetVersion}

```lua
nMajor, nMinor, szVersion = GetVersion()
```

**Returns:**
- `number` - Major version number
- `number` - Minor version number
- `string` - Version string (e.g., "zhcn", "vivn")

Get the game client version information.

---

### IsDebugClient {#IsDebugClient}

```lua
bDebug = IsDebugClient()
```

**Returns:** `boolean` - true if running debug client

Check if the current client is a debug build.

---

### GetCurrentProcessID {#GetCurrentProcessID}

```lua
nPID = GetCurrentProcessID()
```

**Returns:** `number` - Process ID

Get the current process ID.

---

### GetMachineConfig {#GetMachineConfig}

```lua
tConfig = GetMachineConfig()
```

**Returns:** `table` - Machine configuration info

Get the machine hardware configuration.

---

## User & Server Info

### GetUserServer {#GetUserServer}

```lua
szServer = GetUserServer()
```

**Returns:** `string` - Server name

Get the current server name.

---

### GetUserRoleName {#GetUserRoleName}

```lua
szName = GetUserRoleName()
```

**Returns:** `string` - Character name

Get the current character name.

---

### GetUserAccount {#GetUserAccount}

```lua
szAccount = GetUserAccount()
```

**Returns:** `string` - Account name

Get the user account name.

---

### Login_GetAccount {#Login_GetAccount}

```lua
szAccount = Login_GetAccount()
```

**Returns:** `string` - Login account

Get the login account name.

---

### GetGatewayServer {#GetGatewayServer}

```lua
tServer = GetGatewayServer()
```

**Returns:** `table` - Gateway server info

Get the gateway server information for merged servers.

---

### GetInterworkingServers {#GetInterworkingServers}

```lua
tServers = GetInterworkingServers()
```

**Returns:** `table` - List of interworking servers

Get the list of interworking servers.

---

## Thread & Debug

### IsMultiThread {#IsMultiThread}

```lua
bMultiThread = IsMultiThread()
```

**Returns:** `boolean` - true if in multi-thread mode

Check if the current context is in multi-thread mode.

---

### ReloadUIAddon {#ReloadUIAddon}

```lua
ReloadUIAddon()
```

**Returns:** `void`

Reload UI addons.

---

### EnableDebugEnv {#EnableDebugEnv}

```lua
EnableDebugEnv(bEnable)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| bEnable | `boolean` | Enable or disable |

**Returns:** `void`

Enable or disable the debug environment.

Alias: `OpenDebug`

---

## Bitwise Operations

### BitwiseAnd {#BitwiseAnd}

```lua
nResult = BitwiseAnd(nA, nB)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nA | `number` | First operand |
| nB | `number` | Second operand |

**Returns:** `number` - Bitwise AND result

Perform bitwise AND operation.

---

### BitwiseOr {#BitwiseOr}

```lua
nResult = BitwiseOr(nA, nB)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nA | `number` | First operand |
| nB | `number` | Second operand |

**Returns:** `number` - Bitwise OR result

Perform bitwise OR operation.

---

### BitwiseXor {#BitwiseXor}

```lua
nResult = BitwiseXor(nA, nB)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nA | `number` | First operand |
| nB | `number` | Second operand |

**Returns:** `number` - Bitwise XOR result

Perform bitwise XOR operation.

---

### GetNumberBit {#GetNumberBit}

```lua
nBit = GetNumberBit(nValue, nBitIndex)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nValue | `number` | Number value |
| nBitIndex | `number` | Bit index (0-based) |

**Returns:** `number` - Bit value (0 or 1)

Get a specific bit from a number.

---

### SetNumberBit {#SetNumberBit}

```lua
nResult = SetNumberBit(nValue, nBitIndex, nBit)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| nValue | `number` | Original number |
| nBitIndex | `number` | Bit index (0-based) |
| nBit | `number` | Bit value (0 or 1) |

**Returns:** `number` - Modified number

Set a specific bit in a number.

---

## Command Execution

### rlcmd {#rlcmd}

```lua
rlcmd(szCommand)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szCommand | `string` | Command string |

**Returns:** `void`

Execute an RL command.

---

### k3dcmd {#k3dcmd}

```lua
k3dcmd(szCommand)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szCommand | `string` | Command string |

**Returns:** `void`

Execute a K3D command.

---

## Mobile Streaming

### SM_IsEnable {#SM_IsEnable}

```lua
bEnabled = SM_IsEnable()
```

**Returns:** `boolean` - true if streaming mode enabled

Check if streaming mode is enabled.

---

### IsMobileStreamingEnable {#IsMobileStreamingEnable}

```lua
bEnabled = IsMobileStreamingEnable()
```

**Returns:** `boolean` - true if mobile streaming enabled

Check if mobile streaming is enabled.

---

## Plugin Interface

### PluginInterface {#PluginInterface}

```lua
PluginInterface(szMethod, ...)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szMethod | `string` | Method name |
| ... | `any` | Method arguments |

**Returns:** `any` - Method result

Call a plugin interface method.
