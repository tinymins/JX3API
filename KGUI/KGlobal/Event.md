English | [中文](./Event.zh-CN.md)

# Event Functions

Functions for event registration and timer operations.

## Event Functions

[`RegisterEvent`](#RegisterEvent)
[`UnRegisterEvent`](#UnRegisterEvent)
[`FireUIEvent`](#FireUIEvent)

## Timer Functions

[`GetLogicFrameCount`](#GetLogicFrameCount)
[`GetTime`](#GetTime)
[`GetCurrentTime`](#GetCurrentTime)
[`GetTickCount`](#GetTickCount)

---

* <h4 id="RegisterEvent">RegisterEvent</h4>

Registers a callback function for an event.

 > (`void`) RegisterEvent(`string` szEvent, `function` fnCallback)

* <h4 id="UnRegisterEvent">UnRegisterEvent</h4>

Unregisters a callback function from an event.

 > (`void`) UnRegisterEvent(`string` szEvent, `function` fnCallback)

* <h4 id="FireUIEvent">FireUIEvent</h4>

Fires a UI event with optional parameters.

 > (`void`) FireUIEvent(`string` szEvent, ...)

* <h4 id="GetLogicFrameCount">GetLogicFrameCount</h4>

Gets the current logic frame count.

 > (`number` nFrame) GetLogicFrameCount()

* <h4 id="GetTime">GetTime</h4>

Gets the current game time in seconds.

 > (`number` nTime) GetTime()

* <h4 id="GetCurrentTime">GetCurrentTime</h4>

Gets the current system time.

 > (`number` nTime) GetCurrentTime()

* <h4 id="GetTickCount">GetTickCount</h4>

Gets the system tick count in milliseconds.

 > (`number` nTick) GetTickCount()
