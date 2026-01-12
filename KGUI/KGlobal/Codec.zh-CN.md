# 编解码函数

编码、解码和转换函数。

---

## 字符串编码

### AnsiToUTF8 {#AnsiToUTF8}

```lua
szUTF8 = AnsiToUTF8(szAnsi)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szAnsi | `string` | ANSI/游戏代码页字符串 |

**返回:** `string` - UTF-8 编码字符串

将字符串从游戏代码页（ANSI）转换为 UTF-8。

---

### UTF8ToAnsi {#UTF8ToAnsi}

```lua
szAnsi = UTF8ToAnsi(szUTF8)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szUTF8 | `string` | UTF-8 编码字符串 |

**返回:** `string` - ANSI/游戏代码页字符串

将字符串从 UTF-8 转换为游戏代码页（ANSI）。

---

### ConvertCodePage {#ConvertCodePage}

```lua
szResult = ConvertCodePage(szText, nFromCodePage, nToCodePage)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szText | `string` | 源字符串 |
| nFromCodePage | `number` | 源代码页 |
| nToCodePage | `number` | 目标代码页 |

**返回:** `string` - 转换后的字符串

在不同代码页之间转换字符串。

---

### GetGameCodePage {#GetGameCodePage}

```lua
nCodePage = GetGameCodePage()
```

**返回:** `number` - 游戏代码页编号（如简体中文为 936）

获取游戏内部使用的代码页。

---

### GetAnsiCodePage {#GetAnsiCodePage}

```lua
nCodePage = GetAnsiCodePage()
```

**返回:** `number` - 系统 ANSI 代码页编号

获取系统 ANSI 代码页。

---

## URL 编码

### UrlEncode {#UrlEncode}

```lua
szEncoded = UrlEncode(szText)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szText | `string` | 原始字符串 |

**返回:** `string` - URL 编码后的字符串

对字符串进行 URL 编码（百分号编码）。

---

### UrlDecode {#UrlDecode}

```lua
szDecoded = UrlDecode(szText)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szText | `string` | URL 编码的字符串 |

**返回:** `string` - 解码后的字符串

解码 URL 编码的字符串。

---

## JSON

### JsonEncode {#JsonEncode}

```lua
szJson = JsonEncode(tData)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| tData | `table` | 要编码的 Lua 表 |

**返回:** `string` - JSON 字符串

将 Lua 表转换为 JSON 字符串。

---

### JsonDecode {#JsonDecode}

```lua
tData = JsonDecode(szJson)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szJson | `string` | JSON 字符串 |

**返回:** `table` - Lua 表

将 JSON 字符串解析为 Lua 表。

---

## 二进制数据编码

### IsEncodedData {#IsEncodedData}

```lua
bEncoded = IsEncodedData(szData)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szData | `string` | 要检查的数据 |

**返回:** `boolean` - 如果数据已编码则返回 true

检查数据是否已编码。

---

### EncodeData {#EncodeData}

```lua
szEncoded = EncodeData(szData)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szData | `string` | 要编码的数据 |

**返回:** `string` - 编码后的数据

编码数据（类似 Base64 编码）。

---

### DecodeData {#DecodeData}

```lua
szDecoded = DecodeData(szEncoded)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szEncoded | `string` | 编码后的数据 |

**返回:** `string` - 解码后的数据

解码已编码的数据。

---

### EncodeByteData {#EncodeByteData}

```lua
szEncoded = EncodeByteData(szData)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szData | `string` | 要编码的字节数据 |

**返回:** `string` - 编码后的字节数据

编码字节数据。

---

### DecodeByteData {#DecodeByteData}

```lua
szDecoded = DecodeByteData(szEncoded)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szEncoded | `string` | 编码后的字节数据 |

**返回:** `string` - 解码后的字节数据

解码已编码的字节数据。

---

## 加密

### EncryptAES {#EncryptAES}

```lua
szEncrypted = EncryptAES(szData, szKey)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szData | `string` | 要加密的数据 |
| szKey | `string` | 加密密钥 |

**返回:** `string` - AES 加密后的数据

使用 AES 算法加密数据。

---

### DecryptAES {#DecryptAES}

```lua
szDecrypted = DecryptAES(szEncrypted, szKey)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szEncrypted | `string` | AES 加密的数据 |
| szKey | `string` | 解密密钥 |

**返回:** `string` - 解密后的数据

解密 AES 加密的数据。

---

### KGUIEncrypt {#KGUIEncrypt}

```lua
szEncrypted = KGUIEncrypt(szData)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szData | `string` | 要加密的数据 |

**返回:** `string` - 加密后的数据

使用 KGUI 内置加密方法加密数据。

---

## 哈希/CRC

### GetFileCRC {#GetFileCRC}

```lua
nCRC = GetFileCRC(szFilePath)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szFilePath | `string` | 文件路径 |

**返回:** `number` - 文件的 CRC32 校验和

计算文件的 CRC32 校验和。

---

### GetStringCRC {#GetStringCRC}

```lua
nCRC = GetStringCRC(szText)
```

| 参数 | 类型 | 描述 |
|------|------|------|
| szText | `string` | 输入字符串 |

**返回:** `number` - 字符串的 CRC32 校验和

计算字符串的 CRC32 校验和。

---

## 已禁用的函数

以下函数在源码中存在但已被注释，无法使用：

### ~~DecodeComponentsString~~ {#DecodeComponentsString}

⚠️ **已禁用** - 此函数已被注释。

```lua
-- 已注释
-- local tComponents = DecodeComponentsString(szData)
```
