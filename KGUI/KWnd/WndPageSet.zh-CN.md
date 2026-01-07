[English](./WndPageSet.md) | 中文

# WndPageSet（分页容器）

说明：

- `WndPageSet` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

[`ActivePage`](#LuaPageSet_ActivePage)
[`GetActivePageIndex`](#LuaPageSet_GetActivePageIndex)
[`GetLastActivePageIndex`](#LuaPageSet_GetLastActivePageIndex)
[`AddPage`](#LuaPageSet_AddPage)
[`GetActivePage`](#LuaPageSet_GetActivePage)
[`GetActiveCheckBox`](#LuaPageSet_GetActiveCheckBox)

* <h4 id="LuaPageSet_ActivePage">ActivePage</h4>

 > (`void`) WndPageSet:ActivePage(`number|string` nPageIndexOrWndName)

说明：

- 传 `number` 时按页索引激活。
- 传 `string` 时，会把它当作子窗口路径，在当前 `WndPageSet` 下查找对应 `WndCheckBox` 或 `WndWindow` 并激活。

* <h4 id="LuaPageSet_GetActivePageIndex">GetActivePageIndex</h4>

获取当前激活页的索引。

 > (`number` nIndex) WndPageSet:GetActivePageIndex()

* <h4 id="LuaPageSet_GetLastActivePageIndex">GetLastActivePageIndex</h4>

获取上一次激活页的索引。

 > (`number` nIndex) WndPageSet:GetLastActivePageIndex()

* <h4 id="LuaPageSet_AddPage">AddPage</h4>

 > (`void`) WndPageSet:AddPage(`WndPage|string` Page, `WndCheckBox|string` CheckBox[, `string` pcszNewPageName[, `string` pcszNewCheckBoxName]])

说明：

- `Page` / `CheckBox` 可以直接传窗口对象（userdata/table），也可以传窗口名（string）。
- 可选 `pcszNewPageName`、`pcszNewCheckBoxName` 非空时会重命名对应窗口。

* <h4 id="LuaPageSet_GetActivePage">GetActivePage</h4>

获取当前激活的页面窗口对象。

 > (`WndPage` Page) WndPageSet:GetActivePage()

* <h4 id="LuaPageSet_GetActiveCheckBox">GetActiveCheckBox</h4>

获取当前激活页对应的 CheckBox。

 > (`WndCheckBox` CheckBox) WndPageSet:GetActiveCheckBox()
