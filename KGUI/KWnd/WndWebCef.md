# WndWebCef

Notes:

- `WndWebCef` inherits all methods from `WndWindow`; only additional methods are listed here.

[`Navigate`](#LuaWndWebCef_Navigate)
[`NavigateBindCard`](#LuaWndWebCef_NavigateBindCard)
[`CanGoBack`](#LuaWndWebCef_CanGoBack)
[`CanGoForward`](#LuaWndWebCef_CanGoForward)
[`GoBack`](#LuaWndWebCef_GoBack)
[`GoForward`](#LuaWndWebCef_GoForward)
[`Refresh`](#LuaWndWebCef_Refresh)
[`GetLocationName`](#LuaWndWebCef_GetLocationName)
[`GetLocationURL`](#LuaWndWebCef_GetLocationURL)
[`EnableUpdate`](#LuaWndWebCef_EnabelUpdate)

* <h4 id="LuaWndWebCef_Navigate">Navigate</h4>

Navigates the embedded CEF browser to a URL.

 > (`void`) WndWebCef:Navigate(`string` szURL)

* <h4 id="LuaWndWebCef_NavigateBindCard">NavigateBindCard</h4>

Builds a bind-card URL (optionally reading password from a `WndEdit` depending on `nAccountType`) and navigates to it.

 > (`void`) WndWebCef:NavigateBindCard(`string` szConst, `string` szAccount, `string` szPasswordTreePath, `string` szOfficialWeb, `number` nAccountType)

* <h4 id="LuaWndWebCef_CanGoBack">CanGoBack</h4>

Returns whether the browser can navigate back.

 > (`bool` bOk) WndWebCef:CanGoBack()

* <h4 id="LuaWndWebCef_CanGoForward">CanGoForward</h4>

Returns whether the browser can navigate forward.

 > (`bool` bOk) WndWebCef:CanGoForward()

* <h4 id="LuaWndWebCef_GoBack">GoBack</h4>

Navigates back.

 > (`void`) WndWebCef:GoBack()

* <h4 id="LuaWndWebCef_GoForward">GoForward</h4>

Navigates forward.

 > (`void`) WndWebCef:GoForward()

* <h4 id="LuaWndWebCef_Refresh">Refresh</h4>

Refreshes/reloads the current page.

 > (`void`) WndWebCef:Refresh()

* <h4 id="LuaWndWebCef_GetLocationName">GetLocationName</h4>

Gets the current page/location name.

 > (`string` szName) WndWebCef:GetLocationName()

* <h4 id="LuaWndWebCef_GetLocationURL">GetLocationURL</h4>

Gets the current page/location URL.

 > (`string` szURL) WndWebCef:GetLocationURL()

* <h4 id="LuaWndWebCef_EnabelUpdate">EnableUpdate</h4>

Enables or disables browser update.

 > (`void`) WndWebCef:EnableUpdate(`bool|number` bEnable)
