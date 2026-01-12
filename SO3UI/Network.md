English | [中文](./Network.zh-CN.md)

# Network Functions (SO3UI)

HTTP network request functions provided by SO3UI module.

Source: `Source/Client/SO3UI/kschemescripttable.cpp`

---

## CURL_HttpPostEx {#CURL_HttpPostEx}

Send an HTTP POST request asynchronously.

```lua
CURL_HttpPostEx(szKey, szUrl, szData, fnCallback, tHeaders)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szKey | `string` | Unique request identifier (automatically prefixed with `__addon_`) |
| szUrl | `string` | Target URL |
| szData | `string` | POST data body |
| fnCallback | `function` | Callback function `function(bSuccess, szContent)` |
| tHeaders | `table` | Optional: HTTP headers table `{["Content-Type"] = "application/json"}` |

**Returns:** `void`

**Event:** `CURL_REQUEST_RESULT` - Fired when request completes
- `arg0`: Request key
- `arg1`: Success boolean
- `arg2`: Response content
- `arg3`: Content size

**Example:**
```lua
CURL_HttpPostEx("myrequest", "https://api.example.com/data",
    JsonEncode({name = "test"}),
    function(bSuccess, szContent)
        if bSuccess then
            local data = JsonDecode(szContent)
            Output(data)
        end
    end,
    {["Content-Type"] = "application/json"}
)
```

---

## CURL_DownloadFile {#CURL_DownloadFile}

Download a file from URL.

```lua
CURL_DownloadFile(szKey, szUrl, szFilePath, bSSL, nConnTimeout, nTimeout)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szKey | `string` | Unique request identifier |
| szUrl | `string` | File URL |
| szFilePath | `string` | Local file path to save |
| bSSL | `boolean` | Optional: Use SSL verification (default: false) |
| nConnTimeout | `number` | Optional: Connection timeout in seconds (default: 10) |
| nTimeout | `number` | Optional: Total timeout in seconds (default: -1, no limit) |

**Returns:** `void`

**Events:**
- `CURL_PROGRESS_UPDATE` - Fired during download progress
  - `arg0`: Request key
  - `arg1`: Total download size
  - `arg2`: Downloaded size
  - `arg3`: Total upload size
  - `arg4`: Uploaded size
- `CURL_DOWNLOAD_RESULT` - Fired when download completes
  - `arg0`: Request key
  - `arg1`: Success boolean
  - `arg2`: File path
  - `arg3`: File size

---

## CURL_Close {#CURL_Close}

Close/cancel a CURL request.

```lua
CURL_Close(szKey)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szKey | `string` | Request identifier to close |

**Returns:** `void`

---

## Disabled Functions

The following functions exist in source but are commented out in addon API and cannot be used:

### ~~CURL_HttpRqst~~ {#CURL_HttpRqst}

⚠️ **Disabled** - Use `CURL_HttpPostEx` instead.

```lua
-- Commented out in addonapi.lua
-- CURL_HttpRqst(szKey, szUrl, bSSL, nTimeout)
```

Source signature:
```cpp
// LuaCURL_HttpRqst(Lua_State *L)
// Parameters: szKey, szUrl, bSSL (optional), nTimeout (optional)
```

---

### ~~CURL_HttpPost~~ {#CURL_HttpPost}

⚠️ **Disabled** - Use `CURL_HttpPostEx` instead.

```lua
-- Commented out in addonapi.lua
-- CURL_HttpPost(szKey, szUrl, szData/tData, bSSL, nConnTimeout, nTimeout, tHeaders)
```

Source signature:
```cpp
// LuaCURL_HttpPost(Lua_State *L)
// Parameters: szKey, szUrl, szData or table, bSSL (optional), nConnTimeout (optional), nTimeout (optional), tHeaders (optional)
```
