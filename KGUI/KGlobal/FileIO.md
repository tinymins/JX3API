# File IO Functions

File reading, writing, and data persistence functions.

---

## Synchronous File Operations

### LoadDataFromFile {#LoadDataFromFile}

```lua
data = LoadDataFromFile(szFilePath, bPak, szPassphrase)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szFilePath | `string` | File path (must be in interface directory) |
| bPak | `boolean` | Optional: Load from pak file |
| szPassphrase | `string` | Optional: Decryption passphrase |

**Returns:** `any` - Loaded data (Lua table or other serialized data)

Load data from a file synchronously.

---

### SaveDataToFile {#SaveDataToFile}

```lua
bSuccess = SaveDataToFile(data, szFilePath, szPassphrase, bCRCCheck, bCompress)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| data | `any` | Data to save |
| szFilePath | `string` | File path (must be in interface directory) |
| szPassphrase | `string` | Optional: Encryption passphrase |
| bCRCCheck | `boolean` | Optional: Add CRC check |
| bCompress | `boolean` | Optional: Compress data |

**Returns:** `boolean` - true if successful

Save data to a file synchronously.

---

## Asynchronous File Operations

### AsyncLoadDataFromFile {#AsyncLoadDataFromFile}

```lua
AsyncLoadDataFromFile(szFilePath, fnCallback, bPak, szPassphrase)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szFilePath | `string` | File path (must be in interface directory) |
| fnCallback | `function` | Callback function `function(bSuccess, data)` |
| bPak | `boolean` | Optional: Load from pak file |
| szPassphrase | `string` | Optional: Decryption passphrase |

**Returns:** `void`

Load data from a file asynchronously.

---

### AsyncSaveDataToFile {#AsyncSaveDataToFile}

```lua
AsyncSaveDataToFile(data, szFilePath, fnCallback, szPassphrase, bCRCCheck, bCompress)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| data | `any` | Data to save |
| szFilePath | `string` | File path (must be in interface directory) |
| fnCallback | `function` | Callback function `function(bSuccess)` |
| szPassphrase | `string` | Optional: Encryption passphrase |
| bCRCCheck | `boolean` | Optional: Add CRC check |
| bCompress | `boolean` | Optional: Compress data |

**Returns:** `void`

Save data to a file asynchronously.

---

## LUA Data Persistence

### SaveLUAData {#SaveLUAData}

```lua
bSuccess = SaveLUAData(szFilePath, tData, bIndent)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szFilePath | `string` | File path |
| tData | `table` | Lua table to save |
| bIndent | `boolean` | Optional: Pretty print with indentation |

**Returns:** `boolean` - true if successful

Save a Lua table to a file in Lua format.

---

### LoadLUAData {#LoadLUAData}

```lua
tData = LoadLUAData(szFilePath)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szFilePath | `string` | File path |

**Returns:** `table` - Loaded Lua table

Load a Lua table from a file.

---

### AsyncSaveLuaData {#AsyncSaveLuaData}

```lua
AsyncSaveLuaData(szFilePath, tData, bIndent, fnCallback)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szFilePath | `string` | File path |
| tData | `table` | Lua table to save |
| bIndent | `boolean` | Optional: Pretty print with indentation |
| fnCallback | `function` | Optional: Callback function `function(bSuccess)` |

**Returns:** `void`

Save a Lua table to a file asynchronously.

---

### AsyncLoadLUAData {#AsyncLoadLUAData}

```lua
AsyncLoadLUAData(szFilePath, fnCallback)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szFilePath | `string` | File path |
| fnCallback | `function` | Callback function `function(bSuccess, tData)` |

**Returns:** `void`

Load a Lua table from a file asynchronously.

---

## User Data

### GetUserDataFolder {#GetUserDataFolder}

```lua
szPath = GetUserDataFolder()
```

**Returns:** `string` - User data folder path

Get the path to the user data folder.

---

## Clipboard

### SetDataToClip {#SetDataToClip}

```lua
SetDataToClip(szText)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szText | `string` | Text to copy (max 128 characters) |

**Returns:** `void`

Copy text to the system clipboard. Only works when account is activated.

---

## File Dialog

### GetOpenFileName {#GetOpenFileName}

```lua
szFilePath = GetOpenFileName(szFilter, szTitle)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szFilter | `string` | File filter (e.g., "Lua Files\|*.lua\|All Files\|*.*") |
| szTitle | `string` | Dialog title |

**Returns:** `string` - Selected file path, or nil if cancelled

Open a file selection dialog.
