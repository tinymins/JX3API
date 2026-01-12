# 文件 IO 函数

文件读写和数据持久化函数。

---

## 同步文件操作

### LoadDataFromFile {#LoadDataFromFile}

```lua
data = LoadDataFromFile(szFilePath, bPak, szPassphrase)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szFilePath | `string` | 文件路径（必须在 interface 目录内） |
| bPak | `boolean` | 可选：从 pak 文件加载 |
| szPassphrase | `string` | 可选：解密密码 |

**返回:** `any` - 加载的数据（Lua 表或其他序列化数据）

同步从文件加载数据。

---

### SaveDataToFile {#SaveDataToFile}

```lua
bSuccess = SaveDataToFile(data, szFilePath, szPassphrase, bCRCCheck, bCompress)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| data | `any` | 要保存的数据 |
| szFilePath | `string` | 文件路径（必须在 interface 目录内） |
| szPassphrase | `string` | 可选：加密密码 |
| bCRCCheck | `boolean` | 可选：添加 CRC 校验 |
| bCompress | `boolean` | 可选：压缩数据 |

**返回:** `boolean` - 成功返回 true

同步保存数据到文件。

---

## 异步文件操作

### AsyncLoadDataFromFile {#AsyncLoadDataFromFile}

```lua
AsyncLoadDataFromFile(szFilePath, fnCallback, bPak, szPassphrase)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szFilePath | `string` | 文件路径（必须在 interface 目录内） |
| fnCallback | `function` | 回调函数 `function(bSuccess, data)` |
| bPak | `boolean` | 可选：从 pak 文件加载 |
| szPassphrase | `string` | 可选：解密密码 |

**返回:** `void`

异步从文件加载数据。

---

### AsyncSaveDataToFile {#AsyncSaveDataToFile}

```lua
AsyncSaveDataToFile(data, szFilePath, fnCallback, szPassphrase, bCRCCheck, bCompress)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| data | `any` | 要保存的数据 |
| szFilePath | `string` | 文件路径（必须在 interface 目录内） |
| fnCallback | `function` | 回调函数 `function(bSuccess)` |
| szPassphrase | `string` | 可选：加密密码 |
| bCRCCheck | `boolean` | 可选：添加 CRC 校验 |
| bCompress | `boolean` | 可选：压缩数据 |

**返回:** `void`

异步保存数据到文件。

---

## LUA 数据持久化

### SaveLUAData {#SaveLUAData}

```lua
bSuccess = SaveLUAData(szFilePath, tData, bIndent)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szFilePath | `string` | 文件路径 |
| tData | `table` | 要保存的 Lua 表 |
| bIndent | `boolean` | 可选：使用缩进格式化输出 |

**返回:** `boolean` - 成功返回 true

将 Lua 表以 Lua 格式保存到文件。

---

### LoadLUAData {#LoadLUAData}

```lua
tData = LoadLUAData(szFilePath)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szFilePath | `string` | 文件路径 |

**返回:** `table` - 加载的 Lua 表

从文件加载 Lua 表。

---

### AsyncSaveLuaData {#AsyncSaveLuaData}

```lua
AsyncSaveLuaData(szFilePath, tData, bIndent, fnCallback)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szFilePath | `string` | 文件路径 |
| tData | `table` | 要保存的 Lua 表 |
| bIndent | `boolean` | 可选：使用缩进格式化输出 |
| fnCallback | `function` | 可选：回调函数 `function(bSuccess)` |

**返回:** `void`

异步将 Lua 表保存到文件。

---

### AsyncLoadLUAData {#AsyncLoadLUAData}

```lua
AsyncLoadLUAData(szFilePath, fnCallback)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szFilePath | `string` | 文件路径 |
| fnCallback | `function` | 回调函数 `function(bSuccess, tData)` |

**返回:** `void`

异步从文件加载 Lua 表。

---

## 用户数据

### GetUserDataFolder {#GetUserDataFolder}

```lua
szPath = GetUserDataFolder()
```

**返回:** `string` - 用户数据文件夹路径

获取用户数据文件夹的路径。

---

## 剪贴板

### SetDataToClip {#SetDataToClip}

```lua
SetDataToClip(szText)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szText | `string` | 要复制的文本（最多 128 字符） |

**返回:** `void`

将文本复制到系统剪贴板。仅当账号已激活时有效。

---

## 文件对话框

### GetOpenFileName {#GetOpenFileName}

```lua
szFilePath = GetOpenFileName(szFilter, szTitle)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szFilter | `string` | 文件过滤器（如 "Lua 文件\|*.lua\|所有文件\|*.*"） |
| szTitle | `string` | 对话框标题 |

**返回:** `string` - 选择的文件路径，取消则返回 nil

打开文件选择对话框。
