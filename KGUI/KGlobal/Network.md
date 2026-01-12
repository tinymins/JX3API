English | [中文](./Network.zh-CN.md)

# Network Functions (KGUI)

Network-related functions provided by KGUI module.

> **Note:** Most HTTP request functions (CURL_HttpPostEx, CURL_HttpRqst, CURL_HttpPost, CURL_DownloadFile, CURL_Close) are provided by SO3UI module. See [SO3UI Network](../../SO3UI/Network.md) for those APIs.

---

## OpenBrowser {#OpenBrowser}

```lua
OpenBrowser(szUrl)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szUrl | `string` | URL to open |

**Returns:** `void`

Open a URL in the system default browser.

Source: `SO3UI/kschemescripttable.cpp` (exported as alias of `OpenExplorer`)

---

## KCurl Module

For low-level HTTP operations, see [KGUI KCurl Module](../KCurl/KCurl.md).

Source: `KGUI/script/kcurlscripttable.cpp`

---

## Disabled Functions

The following functions exist in source but are commented out and cannot be used:

### ~~Curl_Create~~ {#Curl_Create}

⚠️ **Disabled** - Low-level CURL interface disabled for addons.

```lua
-- Commented out in addonapi.lua
-- local curl = Curl_Create()
```

See [KCurl Documentation](../KCurl/KCurl.md) for the full API reference.

Source: `KGUI/script/kcurlscripttable.cpp`

---

### ~~OpenInternetExplorer~~ {#OpenInternetExplorer}

⚠️ **Disabled** - Use `OpenBrowser` instead.

```lua
-- Commented out in addonapi.lua
-- OpenInternetExplorer(url)
```

Source: `SO3UI/kschemescripttable.cpp`
