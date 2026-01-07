[English](./WndNewScrollBar.md) | 中文

# WndNewScrollBar（滚动条）

说明：

- `WndNewScrollBar` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

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

 > (`void`) WndNewScrollBar:Enable(`bool|number` bEnable)

说明：

- 参数个数必须为 2。
- 实现使用 `lua_toboolean` 读取 `bEnable`（Lua 传 `number` 也会按布尔语义处理）。
- 调用底层 `Enable(bEnable)`。

* <h4 id="LuaNewScrollBar_EnableScroll">EnableScroll</h4>

 > (`void`) WndNewScrollBar:EnableScroll(`bool|number` bEnable)

说明：

- 参数个数必须为 2。
- 实现使用 `lua_toboolean` 读取 `bEnable`。
- 调用底层 `EnableScroll(bEnable)`。

* <h4 id="LuaNewScrollBar_SetScrollPos">SetScrollPos</h4>

 > (`void`) WndNewScrollBar:SetScrollPos(`number` nPos[, `number` eFireType])

说明：

- 参数个数必须为 2 或 3。
- `nPos` 以整数形式传入。
- 可选 `eFireType` 会传给底层 `SetScrollPos(nPos, eFireType)`。

* <h4 id="LuaNewScrollBar_GetScrollPos">GetScrollPos</h4>

 > (`number` nPos) WndNewScrollBar:GetScrollPos()

说明：

- 只接受 `self` 一个参数。
- 返回当前滚动位置。

* <h4 id="LuaNewScrollBar_SetStepCount">SetStepCount</h4>

 > (`void`) WndNewScrollBar:SetStepCount(`number` nCount[, `number` eFireType])

说明：

- 参数个数必须为 2 或 3。
- `nCount` 会被 `ceil()` 向上取整后作为 step 数。
- 可选 `eFireType` 会传给底层 `SetStepCount(nStepCount, eFireType)`。

* <h4 id="LuaNewScrollBar_GetStepCount">GetStepCount</h4>

 > (`number` nCount) WndNewScrollBar:GetStepCount()

说明：

- 只接受 `self` 一个参数。
- 返回 step 数。

* <h4 id="LuaNewScrollBar_SetPageStepCount">SetPageStepCount</h4>

 > (`void`) WndNewScrollBar:SetPageStepCount(`number` nCount)

说明：

- 参数个数必须为 2。
- 调用底层 `SetPageStepCount(nStepCount)`。

* <h4 id="LuaNewScrollBar_GetPageStepCount">GetPageStepCount</h4>

 > (`number` nCount) WndNewScrollBar:GetPageStepCount()

说明：

- 只接受 `self` 一个参数。
- 返回 page step 数。

* <h4 id="LuaNewScrollBar_ScrollPrev">ScrollPrev</h4>

 > (`void`) WndNewScrollBar:ScrollPrev([`number` nStepCount = 1])

说明：

- 参数个数至少为 1（实现允许只传 `self`）。
- 可选 `nStepCount` 默认为 1；传入时按整数读取。
- 调用底层 `ScrollPrev(nStepCount)`。

* <h4 id="LuaNewScrollBar_ScrollNext">ScrollNext</h4>

 > (`void`) WndNewScrollBar:ScrollNext([`number` nStepCount = 1])

说明：

- 参数个数至少为 1（实现允许只传 `self`）。
- 可选 `nStepCount` 默认为 1；传入时按整数读取。
- 调用底层 `ScrollNext(nStepCount)`。

* <h4 id="LuaNewScrollBar_ScrollPagePrev">ScrollPagePrev</h4>

 > (`void`) WndNewScrollBar:ScrollPagePrev()

说明：

- 只接受 `self` 一个参数。
- 调用底层 `ScrollPagePrev()`。

* <h4 id="LuaNewScrollBar_ScrollPageNext">ScrollPageNext</h4>

 > (`void`) WndNewScrollBar:ScrollPageNext()

说明：

- 只接受 `self` 一个参数。
- 调用底层 `ScrollPageNext()`。

* <h4 id="LuaNewScrollBar_ScrollHome">ScrollHome</h4>

 > (`void`) WndNewScrollBar:ScrollHome()

说明：

- 只接受 `self` 一个参数。
- 调用底层 `ScrollHome()`。

* <h4 id="LuaNewScrollBar_ScrollEnd">ScrollEnd</h4>

 > (`void`) WndNewScrollBar:ScrollEnd()

说明：

- 只接受 `self` 一个参数。
- 调用底层 `ScrollEnd()`。

* <h4 id="LuaNewScrollBar_SetDragStep">SetDragStep</h4>

 > (`void`) WndNewScrollBar:SetDragStep(`bool` bDragStep)

说明：

- 参数个数必须为 2。
- `bDragStep` 在实现中要求必须为 `boolean`（会 `lua_isboolean` 校验）。
- 调用底层 `SetDragStep(bDragStep)`。

* <h4 id="LuaNewScrollBar_EnableFreeOpt">EnableFreeOpt</h4>

 > (`void`) WndNewScrollBar:EnableFreeOpt(`bool` bEnable)

说明：

- 参数个数必须为 2。
- `bEnable` 在实现中要求必须为 `boolean`（会 `lua_isboolean` 校验）。
- 底层通过设置状态位 `WNDNEWSCROLL_FREE_OPT` 实现。
