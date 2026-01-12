[English](./String.md) | 中文

# 字符串函数

字符串操作相关函数。

## 函数

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

在宽字符串中查找子字符串。

 > (`number` nPos) StringFindW(`string` szString, `string` szPattern, `number` nStart)

* <h4 id="StringSubW">StringSubW</h4>

从宽字符串获取子字符串。

 > (`string` szSubString) StringSubW(`string` szString, `number` nStart, `number` nEnd)

* <h4 id="StringLenW">StringLenW</h4>

获取宽字符串的长度。

 > (`number` nLen) StringLenW(`string` szString)

* <h4 id="StringReplaceW">StringReplaceW</h4>

替换宽字符串中的模式。

 > (`string` szResult) StringReplaceW(`string` szString, `string` szPattern, `string` szReplace)

* <h4 id="StringLowerW">StringLowerW</h4>

将宽字符串转换为小写。

 > (`string` szResult) StringLowerW(`string` szString)

* <h4 id="StringUpperW">StringUpperW</h4>

将宽字符串转换为大写。

 > (`string` szResult) StringUpperW(`string` szString)

* <h4 id="wstring_len">wstring.len</h4>

获取宽字符串的长度。

 > (`number` nLen) wstring.len(`string` szString)

* <h4 id="wstring_sub">wstring.sub</h4>

从宽字符串获取子字符串。

 > (`string` szSubString) wstring.sub(`string` szString, `number` nStart, `number` nEnd)

* <h4 id="wstring_find">wstring.find</h4>

在宽字符串中查找模式。

 > (`number` nStart, `number` nEnd) wstring.find(`string` szString, `string` szPattern)

* <h4 id="wstring_byte">wstring.byte</h4>

获取宽字符串中指定位置的字节值。

 > (`number` nByte) wstring.byte(`string` szString, `number` nPos)

* <h4 id="wstring_format">wstring.format</h4>

格式化宽字符串。

 > (`string` szResult) wstring.format(`string` szFormat, ...)

* <h4 id="FormatMoney">FormatMoney</h4>

将金钱数量格式化为字符串。

 > (`string` szMoney) FormatMoney(`number` nMoney)
