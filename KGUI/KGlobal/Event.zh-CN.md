[English](./Event.md) | 中文

# 事件函数

事件注册和计时器操作相关函数。

## 事件函数

[`RegisterEvent`](#RegisterEvent)
[`UnRegisterEvent`](#UnRegisterEvent)
[`FireUIEvent`](#FireUIEvent)

## 计时器函数

[`GetLogicFrameCount`](#GetLogicFrameCount)
[`GetTime`](#GetTime)
[`GetCurrentTime`](#GetCurrentTime)
[`GetTickCount`](#GetTickCount)

---

* <h4 id="RegisterEvent">RegisterEvent</h4>

为事件注册回调函数。

 > (`void`) RegisterEvent(`string` szEvent, `function` fnCallback)

* <h4 id="UnRegisterEvent">UnRegisterEvent</h4>

从事件中注销回调函数。

 > (`void`) UnRegisterEvent(`string` szEvent, `function` fnCallback)

* <h4 id="FireUIEvent">FireUIEvent</h4>

触发 UI 事件，可带可选参数。

 > (`void`) FireUIEvent(`string` szEvent, ...)

* <h4 id="GetLogicFrameCount">GetLogicFrameCount</h4>

获取当前逻辑帧计数。

 > (`number` nFrame) GetLogicFrameCount()

* <h4 id="GetTime">GetTime</h4>

获取当前游戏时间（秒）。

 > (`number` nTime) GetTime()

* <h4 id="GetCurrentTime">GetCurrentTime</h4>

获取当前系统时间。

 > (`number` nTime) GetCurrentTime()

* <h4 id="GetTickCount">GetTickCount</h4>

获取系统滴答计数（毫秒）。

 > (`number` nTick) GetTickCount()
