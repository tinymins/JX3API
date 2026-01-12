English | [中文](./Misc.zh-CN.md)

# Miscellaneous Functions

Miscellaneous utility functions.

## System Functions

[`Log`](#Log)
[`Trace`](#Trace)
[`IsEmpty`](#IsEmpty)
[`IsTable`](#IsTable)
[`IsNumber`](#IsNumber)
[`IsString`](#IsString)
[`IsFunction`](#IsFunction)
[`IsNil`](#IsNil)
[`Random`](#Random)

## Frame Functions

[`GetLogicFrameCount`](#GetLogicFrameCount)
[`DelayCall`](#DelayCall)

## Path Functions

[`GetFormatPath`](#GetFormatPath)
[`GetUserDataPath`](#GetUserDataPath)
[`GetRootPath`](#GetRootPath)

## Clipboard Functions

[`GetClipboardText`](#GetClipboardText)
[`SetClipboardText`](#SetClipboardText)

---

* <h4 id="Log">Log</h4>

Outputs a log message.

 > (`void`) Log(`string` szMessage)

* <h4 id="Trace">Trace</h4>

Outputs a trace message.

 > (`void`) Trace(`string` szMessage)

* <h4 id="IsEmpty">IsEmpty</h4>

Checks if a value is empty (nil, empty string, or empty table).

 > (`boolean` bEmpty) IsEmpty(`any` value)

* <h4 id="IsTable">IsTable</h4>

Checks if a value is a table.

 > (`boolean` bIsTable) IsTable(`any` value)

* <h4 id="IsNumber">IsNumber</h4>

Checks if a value is a number.

 > (`boolean` bIsNumber) IsNumber(`any` value)

* <h4 id="IsString">IsString</h4>

Checks if a value is a string.

 > (`boolean` bIsString) IsString(`any` value)

* <h4 id="IsFunction">IsFunction</h4>

Checks if a value is a function.

 > (`boolean` bIsFunction) IsFunction(`any` value)

* <h4 id="IsNil">IsNil</h4>

Checks if a value is nil.

 > (`boolean` bIsNil) IsNil(`any` value)

* <h4 id="Random">Random</h4>

Generates a random number.

 > (`number` nRandom) Random(`number` nMin, `number` nMax)

* <h4 id="GetLogicFrameCount">GetLogicFrameCount</h4>

Gets the current logic frame count.

 > (`number` nFrame) GetLogicFrameCount()

* <h4 id="DelayCall">DelayCall</h4>

Calls a function after a delay.

 > (`void`) DelayCall(`number` nDelay, `function` fnCallback)

* <h4 id="GetFormatPath">GetFormatPath</h4>

Formats a path string.

 > (`string` szPath) GetFormatPath(`string` szPath)

* <h4 id="GetUserDataPath">GetUserDataPath</h4>

Gets the user data path.

 > (`string` szPath) GetUserDataPath()

* <h4 id="GetRootPath">GetRootPath</h4>

Gets the root path.

 > (`string` szPath) GetRootPath()

* <h4 id="GetClipboardText">GetClipboardText</h4>

Gets text from the clipboard.

 > (`string` szText) GetClipboardText()

* <h4 id="SetClipboardText">SetClipboardText</h4>

Sets text to the clipboard.

 > (`void`) SetClipboardText(`string` szText)
