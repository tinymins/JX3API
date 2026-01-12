English | [中文](./String.zh-CN.md)

# String Functions

Functions for string manipulation.

## Functions

[`StringFindW`](#StringFindW)
[`StringSubW`](#StringSubW)
[`StringLenW`](#StringLenW)
[`StringReplaceW`](#StringReplaceW)
[`StringLowerW`](#StringLowerW)
[`StringUpperW`](#StringUpperW)
[`wstring.len`](#wstring_len)
[`wstring.sub`](#wstring_sub)
[`wstring.find`](#wstring_find)
[`wstring.byte`](#wstring_byte)
[`wstring.format`](#wstring_format)
[`FormatMoney`](#FormatMoney)

---

* <h4 id="StringFindW">StringFindW</h4>

Finds a substring in a wide string.

 > (`number` nPos) StringFindW(`string` szString, `string` szPattern, `number` nStart)

* <h4 id="StringSubW">StringSubW</h4>

Gets a substring from a wide string.

 > (`string` szSubString) StringSubW(`string` szString, `number` nStart, `number` nEnd)

* <h4 id="StringLenW">StringLenW</h4>

Gets the length of a wide string.

 > (`number` nLen) StringLenW(`string` szString)

* <h4 id="StringReplaceW">StringReplaceW</h4>

Replaces a pattern in a wide string.

 > (`string` szResult) StringReplaceW(`string` szString, `string` szPattern, `string` szReplace)

* <h4 id="StringLowerW">StringLowerW</h4>

Converts a wide string to lowercase.

 > (`string` szResult) StringLowerW(`string` szString)

* <h4 id="StringUpperW">StringUpperW</h4>

Converts a wide string to uppercase.

 > (`string` szResult) StringUpperW(`string` szString)

* <h4 id="wstring_len">wstring.len</h4>

Gets the length of a wide string.

 > (`number` nLen) wstring.len(`string` szString)

* <h4 id="wstring_sub">wstring.sub</h4>

Gets a substring from a wide string.

 > (`string` szSubString) wstring.sub(`string` szString, `number` nStart, `number` nEnd)

* <h4 id="wstring_find">wstring.find</h4>

Finds a pattern in a wide string.

 > (`number` nStart, `number` nEnd) wstring.find(`string` szString, `string` szPattern)

* <h4 id="wstring_byte">wstring.byte</h4>

Gets the byte value at a position in a wide string.

 > (`number` nByte) wstring.byte(`string` szString, `number` nPos)

* <h4 id="wstring_format">wstring.format</h4>

Formats a wide string.

 > (`string` szResult) wstring.format(`string` szFormat, ...)

* <h4 id="FormatMoney">FormatMoney</h4>

Formats a money amount to string.

 > (`string` szMoney) FormatMoney(`number` nMoney)
