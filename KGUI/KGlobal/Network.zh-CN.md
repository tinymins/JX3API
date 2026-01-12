[English](./Network.md) | 中文

# 网络函数（KGUI）

KGUI 模块提供的网络相关函数。

> **注意：** 大多数 HTTP 请求函数（CURL_HttpPostEx, CURL_HttpRqst, CURL_HttpPost, CURL_DownloadFile, CURL_Close）由 SO3UI 模块提供。请参阅 [SO3UI 网络](../../SO3UI/Network.zh-CN.md)。

---

## OpenBrowser {#OpenBrowser}

```lua
OpenBrowser(szUrl)
```

| 参数 | 类型 | 说明 |
|------|------|------|
| szUrl | `string` | 要打开的 URL |

**返回：** `void`

在系统默认浏览器中打开 URL。

源码：`SO3UI/kschemescripttable.cpp`（作为 `OpenExplorer` 的别名导出）

---

## KCurl 模块

底层 HTTP 操作，请参阅 [KGUI KCurl 模块](../KCurl/KCurl.zh-CN.md)。

源码：`KGUI/script/kcurlscripttable.cpp`

---

## 已禁用函数

以下函数存在于源码中，但在 addon API 中被注释掉，无法使用：

### ~~Curl_Create~~ {#Curl_Create}

⚠️ **已禁用** - 底层 CURL 接口对插件禁用。

```lua
-- 在 addonapi.lua 中被注释
-- local curl = Curl_Create()
```

参阅 [KCurl 文档](../KCurl/KCurl.zh-CN.md) 了解完整 API 参考。

源码：`KGUI/script/kcurlscripttable.cpp`

---

### ~~OpenInternetExplorer~~ {#OpenInternetExplorer}

⚠️ **已禁用** - 请使用 `OpenBrowser` 代替。

```lua
-- 在 addonapi.lua 中被注释
-- OpenInternetExplorer(url)
```

源码：`SO3UI/kschemescripttable.cpp`
