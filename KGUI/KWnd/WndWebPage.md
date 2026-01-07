# WndWebPage

Notes:

- `WndWebPage` inherits all methods from `WndWindow`; only additional methods are listed here.

[`Navigate`](#LuaWebPage_Navigate)
[`NavigateBindCard`](#LuaWebPage_NavigateBindCard)
[`CanGoBack`](#LuaWebPage_CanGoBack)
[`CanGoForward`](#LuaWebPage_CanGoForward)
[`GoBack`](#LuaWebPage_GoBack)
[`GoForward`](#LuaWebPage_GoForward)
[`Refresh`](#LuaWebPage_Refresh)
[`GetLocationName`](#LuaWebPage_GetLocationName)
[`GetLocationURL`](#LuaWebPage_GetLocationURL)
[`GetDocument`](#LuaWebPage_GetDocument)
[`EnableUpdate`](#LuaWebPage_EnableUpdate)

* <h4 id="LuaWebPage_Navigate">Navigate</h4>

Navigates the embedded browser to a URL. If multiple URL strings are provided, later ones override earlier ones in the current binding.

 > (`void`) WndWebPage:Navigate(`string` szURL[, `string` szURL2[, `string` szURL3]])

* <h4 id="LuaWebPage_NavigateBindCard">NavigateBindCard</h4>

Builds a bind-card URL (including password read from a `WndEdit` by tree path) and navigates to it.

 > (`void`) WndWebPage:NavigateBindCard(`string` szConst, `string` szAccount, `string` szPasswordTreePath, `string` szOfficialWeb)

* <h4 id="LuaWebPage_CanGoBack">CanGoBack</h4>

Returns whether the browser can navigate back.

 > (`bool` bOk) WndWebPage:CanGoBack()

* <h4 id="LuaWebPage_CanGoForward">CanGoForward</h4>

Returns whether the browser can navigate forward.

 > (`bool` bOk) WndWebPage:CanGoForward()

* <h4 id="LuaWebPage_GoBack">GoBack</h4>

Navigates back.

 > (`void`) WndWebPage:GoBack()

* <h4 id="LuaWebPage_GoForward">GoForward</h4>

Navigates forward.

 > (`void`) WndWebPage:GoForward()

* <h4 id="LuaWebPage_Refresh">Refresh</h4>

Refreshes/reloads the current page.

 > (`void`) WndWebPage:Refresh()

* <h4 id="LuaWebPage_GetLocationName">GetLocationName</h4>

Gets the current page/location name.

 > (`string` szName) WndWebPage:GetLocationName()

* <h4 id="LuaWebPage_GetLocationURL">GetLocationURL</h4>

Gets the current page/location URL.

 > (`string` szURL) WndWebPage:GetLocationURL()

* <h4 id="LuaWebPage_GetDocument">GetDocument</h4>

Gets the current document content as a string (binding converts from wide string).

 > (`string` szDocument) WndWebPage:GetDocument()

* <h4 id="LuaWebPage_EnableUpdate">EnableUpdate</h4>

Enables or disables browser update.

 > (`void`) WndWebPage:EnableUpdate(`bool|number` bEnable)
