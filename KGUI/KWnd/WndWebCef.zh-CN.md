[English](./WndWebCef.md) | 中文

# WndWebCef（网页(CEF)）

说明：

- `WndWebCef` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

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

导航到指定 URL。

 > (`void`) WndWebCef:Navigate(`string` szURL)

* <h4 id="LuaWndWebCef_NavigateBindCard">NavigateBindCard</h4>

 > (`void`) WndWebCef:NavigateBindCard(`string` szConst, `string` szAccount, `string` szPasswordTreePath, `string` szOfficialWeb, `number` nAccountType)

说明：

- 参数数量必须严格为 5 个（不含 self）。
- 当 `nAccountType == 0` 时，会通过 `szPasswordTreePath` 查找 `WndEdit` 并读取密码（MD5）；否则不读取密码，按空串参与拼接。

* <h4 id="LuaWndWebCef_CanGoBack">CanGoBack</h4>

检查是否可以后退。

 > (`bool` bOk) WndWebCef:CanGoBack()

* <h4 id="LuaWndWebCef_CanGoForward">CanGoForward</h4>

检查是否可以前进。

 > (`bool` bOk) WndWebCef:CanGoForward()

* <h4 id="LuaWndWebCef_GoBack">GoBack</h4>

浏览器后退。

 > (`void`) WndWebCef:GoBack()

* <h4 id="LuaWndWebCef_GoForward">GoForward</h4>

浏览器前进。

 > (`void`) WndWebCef:GoForward()

* <h4 id="LuaWndWebCef_Refresh">Refresh</h4>

刷新/重新加载当前页面。

 > (`void`) WndWebCef:Refresh()

* <h4 id="LuaWndWebCef_GetLocationName">GetLocationName</h4>

获取当前页面/位置名称。

 > (`string` szName) WndWebCef:GetLocationName()

* <h4 id="LuaWndWebCef_GetLocationURL">GetLocationURL</h4>

获取当前页面/位置 URL。

 > (`string` szURL) WndWebCef:GetLocationURL()

* <h4 id="LuaWndWebCef_EnabelUpdate">EnableUpdate</h4>

启用/禁用网页控件的更新。

 > (`void`) WndWebCef:EnableUpdate(`bool|number` bEnable)
