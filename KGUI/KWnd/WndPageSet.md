# WndPageSet

Notes:

- `WndPageSet` inherits all methods from `WndWindow`; only additional methods are listed here.

[`ActivePage`](#LuaPageSet_ActivePage)
[`GetActivePageIndex`](#LuaPageSet_GetActivePageIndex)
[`GetLastActivePageIndex`](#LuaPageSet_GetLastActivePageIndex)
[`AddPage`](#LuaPageSet_AddPage)
[`GetActivePage`](#LuaPageSet_GetActivePage)
[`GetActiveCheckBox`](#LuaPageSet_GetActiveCheckBox)

* <h4 id="LuaPageSet_ActivePage">ActivePage</h4>

Activates a page by index, or by a child window path/name.

 > (`void`) WndPageSet:ActivePage(`number|string` nPageIndexOrWndName)

* <h4 id="LuaPageSet_GetActivePageIndex">GetActivePageIndex</h4>

Gets the currently active page index.

 > (`number` nIndex) WndPageSet:GetActivePageIndex()

* <h4 id="LuaPageSet_GetLastActivePageIndex">GetLastActivePageIndex</h4>

Gets the previously active page index.

 > (`number` nIndex) WndPageSet:GetLastActivePageIndex()

* <h4 id="LuaPageSet_AddPage">AddPage</h4>

Adds a page and its associated checkbox. Optional name parameters can rename the windows.

 > (`void`) WndPageSet:AddPage(`WndPage|string` Page, `WndCheckBox|string` CheckBox[, `string` pcszNewPageName[, `string` pcszNewCheckBoxName]])

* <h4 id="LuaPageSet_GetActivePage">GetActivePage</h4>

Gets the currently active page window.

 > (`WndPage` Page) WndPageSet:GetActivePage()

* <h4 id="LuaPageSet_GetActiveCheckBox">GetActiveCheckBox</h4>

Gets the checkbox corresponding to the currently active page.

 > (`WndCheckBox` CheckBox) WndPageSet:GetActiveCheckBox()
