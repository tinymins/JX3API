[English](./Misc.md) | 中文

# 杂项函数

杂项工具函数。

## 系统函数

[`Log`](#Log)
[`Trace`](#Trace)
[`IsEmpty`](#IsEmpty)
[`IsTable`](#IsTable)
[`IsNumber`](#IsNumber)
[`IsString`](#IsString)
[`IsFunction`](#IsFunction)
[`IsNil`](#IsNil)
[`Random`](#Random)

## 帧函数

[`GetLogicFrameCount`](#GetLogicFrameCount)
[`DelayCall`](#DelayCall)

## 路径函数

[`GetFormatPath`](#GetFormatPath)
[`GetUserDataPath`](#GetUserDataPath)
[`GetRootPath`](#GetRootPath)

## 剪贴板函数

[`GetClipboardText`](#GetClipboardText)
[`SetClipboardText`](#SetClipboardText)

---

* <h4 id="Log">Log</h4>

输出日志消息。

 > (`void`) Log(`string` szMessage)

* <h4 id="Trace">Trace</h4>

输出跟踪消息。

 > (`void`) Trace(`string` szMessage)

* <h4 id="IsEmpty">IsEmpty</h4>

检查值是否为空（nil、空字符串或空表）。

 > (`boolean` bEmpty) IsEmpty(`any` value)

* <h4 id="IsTable">IsTable</h4>

检查值是否为表。

 > (`boolean` bIsTable) IsTable(`any` value)

* <h4 id="IsNumber">IsNumber</h4>

检查值是否为数字。

 > (`boolean` bIsNumber) IsNumber(`any` value)

* <h4 id="IsString">IsString</h4>

检查值是否为字符串。

 > (`boolean` bIsString) IsString(`any` value)

* <h4 id="IsFunction">IsFunction</h4>

检查值是否为函数。

 > (`boolean` bIsFunction) IsFunction(`any` value)

* <h4 id="IsNil">IsNil</h4>

检查值是否为 nil。

 > (`boolean` bIsNil) IsNil(`any` value)

* <h4 id="Random">Random</h4>

生成随机数。

 > (`number` nRandom) Random(`number` nMin, `number` nMax)

* <h4 id="GetLogicFrameCount">GetLogicFrameCount</h4>

获取当前逻辑帧计数。

 > (`number` nFrame) GetLogicFrameCount()

* <h4 id="DelayCall">DelayCall</h4>

延迟调用函数。

 > (`void`) DelayCall(`number` nDelay, `function` fnCallback)

* <h4 id="GetFormatPath">GetFormatPath</h4>

格式化路径字符串。

 > (`string` szPath) GetFormatPath(`string` szPath)

* <h4 id="GetUserDataPath">GetUserDataPath</h4>

获取用户数据路径。

 > (`string` szPath) GetUserDataPath()

* <h4 id="GetRootPath">GetRootPath</h4>

获取根路径。

 > (`string` szPath) GetRootPath()

* <h4 id="GetClipboardText">GetClipboardText</h4>

从剪贴板获取文本。

 > (`string` szText) GetClipboardText()

* <h4 id="SetClipboardText">SetClipboardText</h4>

将文本设置到剪贴板。

 > (`void`) SetClipboardText(`string` szText)
