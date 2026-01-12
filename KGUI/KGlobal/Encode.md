English | [中文](./Encode.zh-CN.md)

# Encode Functions

Functions for data encoding and decoding.

## Base64 Functions

[`Base64Encode`](#Base64Encode)
[`Base64Decode`](#Base64Decode)

## JSON Functions

[`JsonEncode`](#JsonEncode)
[`JsonDecode`](#JsonDecode)

## URL Functions

[`UrlEncode`](#UrlEncode)
[`UrlDecode`](#UrlDecode)

## Hash Functions

[`GetStringMD5`](#GetStringMD5)
[`GetStringCRC32`](#GetStringCRC32)

---

* <h4 id="Base64Encode">Base64Encode</h4>

Encodes a string to Base64.

 > (`string` szEncoded) Base64Encode(`string` szInput)

* <h4 id="Base64Decode">Base64Decode</h4>

Decodes a Base64 string.

 > (`string` szDecoded) Base64Decode(`string` szInput)

* <h4 id="JsonEncode">JsonEncode</h4>

Encodes a Lua table to JSON string.

 > (`string` szJson) JsonEncode(`table` tData)

* <h4 id="JsonDecode">JsonDecode</h4>

Decodes a JSON string to Lua table.

 > (`table` tData) JsonDecode(`string` szJson)

* <h4 id="UrlEncode">UrlEncode</h4>

Encodes a string for URL use.

 > (`string` szEncoded) UrlEncode(`string` szInput)

* <h4 id="UrlDecode">UrlDecode</h4>

Decodes a URL-encoded string.

 > (`string` szDecoded) UrlDecode(`string` szInput)

* <h4 id="GetStringMD5">GetStringMD5</h4>

Gets the MD5 hash of a string.

 > (`string` szMD5) GetStringMD5(`string` szInput)

* <h4 id="GetStringCRC32">GetStringCRC32</h4>

Gets the CRC32 hash of a string.

 > (`number` nCRC32) GetStringCRC32(`string` szInput)
