# WndNewScrollBar

Notes:

- `WndNewScrollBar` inherits all methods from `WndWindow`; only additional methods are listed here.

[`Enable`](#LuaNewScrollBar_Enable)
[`EnableScroll`](#LuaNewScrollBar_EnableScroll)
[`SetScrollPos`](#LuaNewScrollBar_SetScrollPos)
[`GetScrollPos`](#LuaNewScrollBar_GetScrollPos)
[`SetStepCount`](#LuaNewScrollBar_SetStepCount)
[`GetStepCount`](#LuaNewScrollBar_GetStepCount)
[`SetPageStepCount`](#LuaNewScrollBar_SetPageStepCount)
[`GetPageStepCount`](#LuaNewScrollBar_GetPageStepCount)
[`ScrollPrev`](#LuaNewScrollBar_ScrollPrev)
[`ScrollNext`](#LuaNewScrollBar_ScrollNext)
[`ScrollPagePrev`](#LuaNewScrollBar_ScrollPagePrev)
[`ScrollPageNext`](#LuaNewScrollBar_ScrollPageNext)
[`ScrollHome`](#LuaNewScrollBar_ScrollHome)
[`ScrollEnd`](#LuaNewScrollBar_ScrollEnd)
[`SetDragStep`](#LuaNewScrollBar_SetDragStep)
[`EnableFreeOpt`](#LuaNewScrollBar_EnableFreeOpt)

* <h4 id="LuaNewScrollBar_Enable">Enable</h4>

Enables or disables the scrollbar control.

 > (`void`) WndNewScrollBar:Enable(`bool|number` bEnable)

* <h4 id="LuaNewScrollBar_EnableScroll">EnableScroll</h4>

Enables or disables scrolling behavior.

 > (`void`) WndNewScrollBar:EnableScroll(`bool|number` bEnable)

* <h4 id="LuaNewScrollBar_SetScrollPos">SetScrollPos</h4>

Sets current scroll position. Optional `eFireType` controls event firing behavior.

 > (`void`) WndNewScrollBar:SetScrollPos(`number` nPos[, `number` eFireType])

* <h4 id="LuaNewScrollBar_GetScrollPos">GetScrollPos</h4>

Gets current scroll position.

 > (`number` nPos) WndNewScrollBar:GetScrollPos()

* <h4 id="LuaNewScrollBar_SetStepCount">SetStepCount</h4>

Sets total step count. Optional `eFireType` controls event firing behavior.

 > (`void`) WndNewScrollBar:SetStepCount(`number` nCount[, `number` eFireType])

* <h4 id="LuaNewScrollBar_GetStepCount">GetStepCount</h4>

Gets current step count.

 > (`number` nCount) WndNewScrollBar:GetStepCount()

* <h4 id="LuaNewScrollBar_SetPageStepCount">SetPageStepCount</h4>

Sets page step count (how much to scroll per page action).

 > (`void`) WndNewScrollBar:SetPageStepCount(`number` nCount)

* <h4 id="LuaNewScrollBar_GetPageStepCount">GetPageStepCount</h4>

Gets page step count.

 > (`number` nCount) WndNewScrollBar:GetPageStepCount()

* <h4 id="LuaNewScrollBar_ScrollPrev">ScrollPrev</h4>

Scrolls towards previous direction by `nStepCount` steps.

 > (`void`) WndNewScrollBar:ScrollPrev([`number` nStepCount = 1])

* <h4 id="LuaNewScrollBar_ScrollNext">ScrollNext</h4>

Scrolls towards next direction by `nStepCount` steps.

 > (`void`) WndNewScrollBar:ScrollNext([`number` nStepCount = 1])

* <h4 id="LuaNewScrollBar_ScrollPagePrev">ScrollPagePrev</h4>

Scrolls one page towards previous direction.

 > (`void`) WndNewScrollBar:ScrollPagePrev()

* <h4 id="LuaNewScrollBar_ScrollPageNext">ScrollPageNext</h4>

Scrolls one page towards next direction.

 > (`void`) WndNewScrollBar:ScrollPageNext()

* <h4 id="LuaNewScrollBar_ScrollHome">ScrollHome</h4>

Scrolls to the home (start) position.

 > (`void`) WndNewScrollBar:ScrollHome()

* <h4 id="LuaNewScrollBar_ScrollEnd">ScrollEnd</h4>

Scrolls to the end position.

 > (`void`) WndNewScrollBar:ScrollEnd()

* <h4 id="LuaNewScrollBar_SetDragStep">SetDragStep</h4>

Sets whether dragging snaps by step.

 > (`void`) WndNewScrollBar:SetDragStep(`bool` bDragStep)

* <h4 id="LuaNewScrollBar_EnableFreeOpt">EnableFreeOpt</h4>

Enables or disables free operation mode.

 > (`void`) WndNewScrollBar:EnableFreeOpt(`bool` bEnable)
