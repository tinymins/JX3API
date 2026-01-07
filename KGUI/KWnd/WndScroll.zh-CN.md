[English](./WndScroll.md) | 中文

# WndScroll（滚动区域）

说明：

- `WndScroll` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

[`GetScrollVerStepSize`](#LuaScroll_GetScrollVerStepSize)
[`SetScrollVerStepSize`](#LuaScroll_SetScrollVerStepSize)
[`GetScrollHorStepSize`](#LuaScroll_GetScrollHorStepSize)
[`SetScrollHorStepSize`](#LuaScroll_SetScrollHorStepSize)
[`GetEntryScrollPos`](#LuaScroll_GetEntryScrollPos)
[`ScrollToEntry`](#LuaScroll_ScrollToEntry)

* <h4 id="LuaScroll_GetScrollVerStepSize">GetScrollVerStepSize</h4>

获取垂直滚动步长。

返回值会在 Lua 层按 `UIScale` 还原（内部值 / `Station.GetUIScale()`）。

 > (`number` fStep) WndScroll:GetScrollVerStepSize()

* <h4 id="LuaScroll_SetScrollVerStepSize">SetScrollVerStepSize</h4>

设置垂直滚动步长。

Lua 侧传入的步长会先乘以 `Station.GetUIScale()` 再写入。

实现支持可选第 3 个参数 `bDontFormat`（bool），用于控制是否自动重新排版（内部实际传入 `!bDontFormat`）。

 > (`void`) WndScroll:SetScrollVerStepSize(`number` fStep[, `bool|number` bDontFormat = false])

* <h4 id="LuaScroll_GetScrollHorStepSize">GetScrollHorStepSize</h4>

获取水平滚动步长。

返回值会在 Lua 层按 `UIScale` 还原（内部值 / `Station.GetUIScale()`）。

 > (`number` fStep) WndScroll:GetScrollHorStepSize()

* <h4 id="LuaScroll_SetScrollHorStepSize">SetScrollHorStepSize</h4>

设置水平滚动步长。

Lua 侧传入的步长会先乘以 `Station.GetUIScale()` 再写入。

实现支持可选第 3 个参数 `bDontFormat`（bool），用于控制是否自动重新排版（内部实际传入 `!bDontFormat`）。

 > (`void`) WndScroll:SetScrollHorStepSize(`number` fStep[, `bool|number` bDontFormat = false])

* <h4 id="LuaScroll_GetEntryScrollPos">GetEntryScrollPos</h4>

获取指定 entry 对应的滚动位置。

参数个数必须为 2 或 3。

- 第 2 个参数支持传入 `WndWindow` userdata，或 HostWndItem（例如 `ItemNull`）userdata。
- 可选第 3 个参数 `bVertical`（bool，默认 true）用于指定按垂直/水平滚动计算。

 > (`number` nPos) WndScroll:GetEntryScrollPos(`WndWindow|ItemNull` entry[, `bool|number` bVertical = true])

* <h4 id="LuaScroll_ScrollToEntry">ScrollToEntry</h4>

滚动到指定 entry。

参数个数必须为 3 或 4。

- 第 2 个参数支持：
	- `number`：entry index
	- `table`：entry userdata（可为 HostWndItem 的 table，或 `WndWindow` userdata）
- 第 3 个参数 `bMinimalMoving`（bool）：是否尽量最小移动。
- 可选第 4 个参数 `bVertical`（bool，默认 true）：按垂直/水平滚动。

内部会根据是否存在 ScrollHandle / ScrollContainer，分别调用 `ScrollToEntryItem` 或 `ScrollToEntryWnd`。

 > (`void`) WndScroll:ScrollToEntry(`number|table` entryOrIndex, `bool|number` bMinimalMoving[, `bool|number` bVertical = true])
