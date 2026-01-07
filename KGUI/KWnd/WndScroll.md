# WndScroll

Notes:

- `WndScroll` inherits all methods from `WndWindow`; only additional methods are listed here.

[`GetScrollVerStepSize`](#LuaScroll_GetScrollVerStepSize)
[`SetScrollVerStepSize`](#LuaScroll_SetScrollVerStepSize)
[`GetScrollHorStepSize`](#LuaScroll_GetScrollHorStepSize)
[`SetScrollHorStepSize`](#LuaScroll_SetScrollHorStepSize)
[`GetEntryScrollPos`](#LuaScroll_GetEntryScrollPos)
[`ScrollToEntry`](#LuaScroll_ScrollToEntry)

* <h4 id="LuaScroll_GetScrollVerStepSize">GetScrollVerStepSize</h4>

Gets vertical scroll step size. Return value is scaled back by `UIScale`.

 > (`number` fStep) WndScroll:GetScrollVerStepSize()

* <h4 id="LuaScroll_SetScrollVerStepSize">SetScrollVerStepSize</h4>

Sets vertical scroll step size. Input is multiplied by `UIScale`; optional `bDontFormat` controls whether to reformat.

 > (`void`) WndScroll:SetScrollVerStepSize(`number` fStep[, `bool|number` bDontFormat = false])

* <h4 id="LuaScroll_GetScrollHorStepSize">GetScrollHorStepSize</h4>

Gets horizontal scroll step size. Return value is scaled back by `UIScale`.

 > (`number` fStep) WndScroll:GetScrollHorStepSize()

* <h4 id="LuaScroll_SetScrollHorStepSize">SetScrollHorStepSize</h4>

Sets horizontal scroll step size. Input is multiplied by `UIScale`; optional `bDontFormat` controls whether to reformat.

 > (`void`) WndScroll:SetScrollHorStepSize(`number` fStep[, `bool|number` bDontFormat = false])

* <h4 id="LuaScroll_GetEntryScrollPos">GetEntryScrollPos</h4>

Gets the scroll position for a specific entry window/item; optional `bVertical` chooses vertical or horizontal behavior.

 > (`number` nPos) WndScroll:GetEntryScrollPos(`WndWindow|ItemNull` entry[, `bool|number` bVertical = true])

* <h4 id="LuaScroll_ScrollToEntry">ScrollToEntry</h4>

Scrolls to a specific entry (by index or userdata). Optional `bVertical` chooses vertical or horizontal behavior.

 > (`void`) WndScroll:ScrollToEntry(`number|table` entryOrIndex, `bool|number` bMinimalMoving[, `bool|number` bVertical = true])
