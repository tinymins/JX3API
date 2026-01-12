[English](./Encode.md) | 中文

# 编码函数

数据编码和解码相关函数。

## Base64 函数

[`Base64Encode`](#Base64Encode)
[`Base64Decode`](#Base64Decode)

## JSON 函数

[`JsonEncode`](#JsonEncode)
[`JsonDecode`](#JsonDecode)

## URL 函数

[`UrlEncode`](#UrlEncode)
[`UrlDecode`](#UrlDecode)

## 哈希函数

[`GetStringMD5`](#GetStringMD5)
[`GetStringCRC32`](#GetStringCRC32)

---

* <h4 id="Base64Encode">Base64Encode</h4>

将字符串编码为 Base64。

 > (`string` szEncoded) Base64Encode(`string` szInput)

* <h4 id="Base64Decode">Base64Decode</h4>

解码 Base64 字符串。

 > (`string` szDecoded) Base64Decode(`string` szInput)

* <h4 id="JsonEncode">JsonEncode</h4>

将 Lua 表编码为 JSON 字符串。

 > (`string` szJson) JsonEncode(`table` tData)

* <h4 id="JsonDecode">JsonDecode</h4>

将 JSON 字符串解码为 Lua 表。

 > (`table` tData) JsonDecode(`string` szJson)

* <h4 id="UrlEncode">UrlEncode</h4>

将字符串编码为 URL 格式。

 > (`string` szEncoded) UrlEncode(`string` szInput)

* <h4 id="UrlDecode">UrlDecode</h4>

解码 URL 编码的字符串。

 > (`string` szDecoded) UrlDecode(`string` szInput)

* <h4 id="GetStringMD5">GetStringMD5</h4>

获取字符串的 MD5 哈希值。

 > (`string` szMD5) GetStringMD5(`string` szInput)

* <h4 id="GetStringCRC32">GetStringCRC32</h4>

获取字符串的 CRC32 哈希值。

 > (`number` nCRC32) GetStringCRC32(`string` szInput)
