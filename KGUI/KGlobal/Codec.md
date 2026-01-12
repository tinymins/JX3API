# Codec Functions

Encoding, decoding, and conversion functions.

---

## String Encoding

### AnsiToUTF8 {#AnsiToUTF8}

```lua
szUTF8 = AnsiToUTF8(szAnsi)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szAnsi | `string` | ANSI/Game code page string |

**Returns:** `string` - UTF-8 encoded string

Convert a string from game code page (ANSI) to UTF-8.

---

### UTF8ToAnsi {#UTF8ToAnsi}

```lua
szAnsi = UTF8ToAnsi(szUTF8)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szUTF8 | `string` | UTF-8 encoded string |

**Returns:** `string` - ANSI/Game code page string

Convert a string from UTF-8 to game code page (ANSI).

---

### ConvertCodePage {#ConvertCodePage}

```lua
szResult = ConvertCodePage(szText, nFromCodePage, nToCodePage)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szText | `string` | Source string |
| nFromCodePage | `number` | Source code page |
| nToCodePage | `number` | Target code page |

**Returns:** `string` - Converted string

Convert a string between different code pages.

---

### GetGameCodePage {#GetGameCodePage}

```lua
nCodePage = GetGameCodePage()
```

**Returns:** `number` - Game code page number (e.g., 936 for Simplified Chinese)

Get the game's internal code page.

---

### GetAnsiCodePage {#GetAnsiCodePage}

```lua
nCodePage = GetAnsiCodePage()
```

**Returns:** `number` - System ANSI code page number

Get the system ANSI code page.

---

## URL Encoding

### UrlEncode {#UrlEncode}

```lua
szEncoded = UrlEncode(szText)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szText | `string` | Original string |

**Returns:** `string` - URL-encoded string

URL-encode a string (percent-encoding).

---

### UrlDecode {#UrlDecode}

```lua
szDecoded = UrlDecode(szText)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szText | `string` | URL-encoded string |

**Returns:** `string` - Decoded string

Decode a URL-encoded string.

---

## JSON

### JsonEncode {#JsonEncode}

```lua
szJson = JsonEncode(tData)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| tData | `table` | Lua table to encode |

**Returns:** `string` - JSON string

Convert a Lua table to a JSON string.

---

### JsonDecode {#JsonDecode}

```lua
tData = JsonDecode(szJson)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szJson | `string` | JSON string |

**Returns:** `table` - Lua table

Parse a JSON string into a Lua table.

---

## Binary Data Encoding

### IsEncodedData {#IsEncodedData}

```lua
bEncoded = IsEncodedData(szData)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szData | `string` | Data to check |

**Returns:** `boolean` - true if data is encoded

Check if data is encoded.

---

### EncodeData {#EncodeData}

```lua
szEncoded = EncodeData(szData)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szData | `string` | Data to encode |

**Returns:** `string` - Encoded data

Encode data (Base64-like encoding).

---

### DecodeData {#DecodeData}

```lua
szDecoded = DecodeData(szEncoded)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szEncoded | `string` | Encoded data |

**Returns:** `string` - Decoded data

Decode encoded data.

---

### EncodeByteData {#EncodeByteData}

```lua
szEncoded = EncodeByteData(szData)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szData | `string` | Byte data to encode |

**Returns:** `string` - Encoded byte data

Encode byte data.

---

### DecodeByteData {#DecodeByteData}

```lua
szDecoded = DecodeByteData(szEncoded)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szEncoded | `string` | Encoded byte data |

**Returns:** `string` - Decoded byte data

Decode encoded byte data.

---

## Encryption

### EncryptAES {#EncryptAES}

```lua
szEncrypted = EncryptAES(szData, szKey)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szData | `string` | Data to encrypt |
| szKey | `string` | Encryption key |

**Returns:** `string` - AES encrypted data

Encrypt data using AES algorithm.

---

### DecryptAES {#DecryptAES}

```lua
szDecrypted = DecryptAES(szEncrypted, szKey)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szEncrypted | `string` | AES encrypted data |
| szKey | `string` | Decryption key |

**Returns:** `string` - Decrypted data

Decrypt AES encrypted data.

---

### KGUIEncrypt {#KGUIEncrypt}

```lua
szEncrypted = KGUIEncrypt(szData)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szData | `string` | Data to encrypt |

**Returns:** `string` - Encrypted data

Encrypt data using KGUI's built-in encryption.

---

## Hash/CRC

### GetFileCRC {#GetFileCRC}

```lua
nCRC = GetFileCRC(szFilePath)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szFilePath | `string` | File path |

**Returns:** `number` - CRC32 checksum of the file

Calculate CRC32 checksum of a file.

---

### GetStringCRC {#GetStringCRC}

```lua
nCRC = GetStringCRC(szText)
```

| Parameter | Type | Description |
|-----------|------|-------------|
| szText | `string` | Input string |

**Returns:** `number` - CRC32 checksum of the string

Calculate CRC32 checksum of a string.

---

## Disabled Functions

The following functions exist in source but are commented out and cannot be used:

### ~~DecodeComponentsString~~ {#DecodeComponentsString}

⚠️ **Disabled** - This function is commented out.

```lua
-- Commented out
-- local tComponents = DecodeComponentsString(szData)
```
