[English](./Network.md) | 中文

# 网络函数（SO3UI）

SO3UI 模块提供的 HTTP 网络请求函数。

源码：`Source/Client/SO3UI/kschemescripttable.cpp`

---

## CURL_HttpPostEx {#CURL_HttpPostEx}

异步发送 HTTP POST 请求。

```lua
CURL_HttpPostEx(szKey, szUrl, szData, fnCallback, tHeaders)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| szKey | `string` | 唯一请求标识（会自动添加 `__addon_` 前缀） |
| szUrl | `string` | 目标 URL |
| szData | `string` | POST 数据体 |
| fnCallback | `function` | 回调函数 `function(bSuccess, szContent)` |
| tHeaders | `table` | 可选：HTTP 请求头表 `{["Content-Type"] = "application/json"}` |

**返回：** `void`

**事件：** `CURL_REQUEST_RESULT` - 请求完成时触发
- `arg0`: 请求标识
- `arg1`: 是否成功
- `arg2`: 响应内容
- `arg3`: 内容大小

**示例：**
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

从 URL 下载文件。

```lua
CURL_DownloadFile(szKey, szUrl, szFilePath, bSSL, nConnTimeout, nTimeout)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| szKey | `string` | 唯一请求标识 |
| szUrl | `string` | 文件 URL |
| szFilePath | `string` | 本地保存路径 |
| bSSL | `boolean` | 可选：使用 SSL 验证（默认：false） |
| nConnTimeout | `number` | 可选：连接超时秒数（默认：10） |
| nTimeout | `number` | 可选：总超时秒数（默认：-1，无限制） |

**返回：** `void`

**事件：**
- `CURL_PROGRESS_UPDATE` - 下载进度更新时触发
  - `arg0`: 请求标识
  - `arg1`: 总下载大小
  - `arg2`: 已下载大小
  - `arg3`: 总上传大小
  - `arg4`: 已上传大小
- `CURL_DOWNLOAD_RESULT` - 下载完成时触发
  - `arg0`: 请求标识
  - `arg1`: 是否成功
  - `arg2`: 文件路径
  - `arg3`: 文件大小

---

## CURL_Close {#CURL_Close}

关闭/取消 CURL 请求。

```lua
CURL_Close(szKey)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| szKey | `string` | 要关闭的请求标识 |

**返回：** `void`

---

## 已禁用函数

以下函数存在于源码中，但在 addon API 中被注释掉，无法使用：

### ~~CURL_HttpRqst~~ {#CURL_HttpRqst}

⚠️ **已禁用** - 请使用 `CURL_HttpPostEx` 代替。

```lua
-- 在 addonapi.lua 中被注释
-- CURL_HttpRqst(szKey, szUrl, bSSL, nTimeout)
```

源码签名：
```cpp
// LuaCURL_HttpRqst(Lua_State *L)
// 参数：szKey, szUrl, bSSL（可选）, nTimeout（可选）
```

---

### ~~CURL_HttpPost~~ {#CURL_HttpPost}

⚠️ **已禁用** - 请使用 `CURL_HttpPostEx` 代替。

```lua
-- 在 addonapi.lua 中被注释
-- CURL_HttpPost(szKey, szUrl, szData/tData, bSSL, nConnTimeout, nTimeout, tHeaders)
```

源码签名：
```cpp
// LuaCURL_HttpPost(Lua_State *L)
// 参数：szKey, szUrl, szData 或 table, bSSL（可选）, nConnTimeout（可选）, nTimeout（可选）, tHeaders（可选）
```
