[English](./WndWebPage.md) | 中文

# WndWebPage（网页）

说明：

- `WndWebPage` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。

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

 > (`void`) WndWebPage:Navigate(`string` szURL[, `string` szURL2[, `string` szURL3]])

说明：

- 至少需要提供一个 URL 字符串参数。
- 当前绑定实现中，如果额外传入第 2/3 个字符串参数（`szURL2`/`szURL3`），它们也会被当作 URL 使用（后传入者会覆盖前者）。

* <h4 id="LuaWebPage_NavigateBindCard">NavigateBindCard</h4>

 > (`void`) WndWebPage:NavigateBindCard(`string` szConst, `string` szAccount, `string` szPasswordTreePath, `string` szOfficialWeb)

说明：

- 参数数量必须严格为 4 个（不含 self）。
- `szPasswordTreePath` 会用于查找一个 `WndEdit`，并从中读取密码（MD5），再拼出最终 URL 并导航。

* <h4 id="LuaWebPage_CanGoBack">CanGoBack</h4>

检查是否可以后退。

 > (`bool` bOk) WndWebPage:CanGoBack()

* <h4 id="LuaWebPage_CanGoForward">CanGoForward</h4>

检查是否可以前进。

 > (`bool` bOk) WndWebPage:CanGoForward()

* <h4 id="LuaWebPage_GoBack">GoBack</h4>

浏览器后退。

 > (`void`) WndWebPage:GoBack()

* <h4 id="LuaWebPage_GoForward">GoForward</h4>

浏览器前进。

 > (`void`) WndWebPage:GoForward()

* <h4 id="LuaWebPage_Refresh">Refresh</h4>

刷新/重新加载当前页面。

 > (`void`) WndWebPage:Refresh()

* <h4 id="LuaWebPage_GetLocationName">GetLocationName</h4>

获取当前页面/位置名称。

 > (`string` szName) WndWebPage:GetLocationName()

* <h4 id="LuaWebPage_GetLocationURL">GetLocationURL</h4>

获取当前页面/位置 URL。

 > (`string` szURL) WndWebPage:GetLocationURL()

* <h4 id="LuaWebPage_GetDocument">GetDocument</h4>

 > (`string` szDocument) WndWebPage:GetDocument()

说明：

- 返回当前文档内容字符串（底层为宽字符串，绑定会做编码转换）。

* <h4 id="LuaWebPage_EnableUpdate">EnableUpdate</h4>

启用/禁用网页控件的更新。

 > (`void`) WndWebPage:EnableUpdate(`bool|number` bEnable)
