[English](./KCurl.md) | 中文

# KCurl

说明：

- 该模块注册了一个全局函数 `Curl_Create`，并导出了一个 userdata 元表 `KCurl`。
- `KCurl:Perform()` 会显式关闭 TLS 校验（`CURLOPT_SSL_VERIFYPEER = 0`、`CURLOPT_SSL_VERIFYHOST = 0`）。
- `KCurlScriptTable::Load()` 还会调用 `luaopen_webclient(L)`；该模块额外导出的 API 不在本文档范围内。

[`Curl_Create`](#LuaCurl_Create)

[`SetMethod`](#LuaKCurl_SetMethod)
[`SetTimeout`](#LuaKCurl_SetTimeout)
[`SetConnTimeout`](#LuaKCurl_SetConnTimeout)
[`AddHeader`](#LuaKCurl_AddHeader)
[`AddPostData`](#LuaKCurl_AddPostData)
[`AddPostFile`](#LuaKCurl_AddPostFile)
[`AddPostRawData`](#LuaKCurl_AddPostRawData)
[`OnProgress`](#LuaKCurl_OnProgress)
[`OnSuccess`](#LuaKCurl_OnSuccess)
[`OnError`](#LuaKCurl_OnError)
[`OnComplete`](#LuaKCurl_OnComplete)
[`Perform`](#LuaKCurl_Perform)

* <h4 id="LuaCurl_Create">Curl_Create</h4>
> (KCurl) Curl_Create(pcszUrl)

创建一个绑定到 `pcszUrl` 的 `KCurl` 请求对象。

- 必须且只能传 1 个参数。
- `pcszUrl` 通过 `lua_tostring` 读取，不能为 `nil`。

成功时返回一个 `KCurl` userdata；失败时不返回值。

* <h4 id="LuaKCurl_SetMethod">SetMethod</h4>
> () KCurl:SetMethod(pcszMethod)

设置 HTTP 方法。

- 必须且只能传 2 个参数（`self`、`pcszMethod`）。
- 识别的字符串：`"POST"`、`"PUT"`、`"DELETE"`。
- 其他值会按 GET 处理（回退为 `CURLOPT_HTTPGET`）。

* <h4 id="LuaKCurl_SetTimeout">SetTimeout</h4>
> () KCurl:SetTimeout(nTimeout)

设置 `CURLOPT_TIMEOUT`。

- `nTimeout` 用 `lua_tonumber` 读取并转换为 `int`。

* <h4 id="LuaKCurl_SetConnTimeout">SetConnTimeout</h4>
> () KCurl:SetConnTimeout(nTimeout)

设置 `CURLOPT_CONNECTTIMEOUT`。

- `nTimeout` 用 `lua_tonumber` 读取并转换为 `int`。

* <h4 id="LuaKCurl_AddHeader">AddHeader</h4>
> () KCurl:AddHeader(pcszHeader)

添加一条原始 HTTP Header 行。

- `pcszHeader` 必须是非 `nil` 字符串。

* <h4 id="LuaKCurl_AddPostData">AddPostData</h4>
> () KCurl:AddPostData(pcszKey, pcszData)

添加一个 multipart/form-data 字段。

- 必须且只能传 3 个参数（`self`、`pcszKey`、`pcszData`）。
- `pcszData` 使用 `lua_tolstring` 读取，因此可以包含二进制数据，并会保留字节长度。

* <h4 id="LuaKCurl_AddPostFile">AddPostFile</h4>
> () KCurl:AddPostFile(pcszKey, pcszConentType, pcszFile, pcszFileName)

添加一个 multipart/form-data 文件字段。

- 必须且只能传 5 个参数（`self`、`pcszKey`、`pcszConentType`、`pcszFile`、`pcszFileName`）。

注意：当前实现里疑似存在多处问题（例如 `pcszKey` 未初始化、以及传递指针大小等），因此该接口行为可能不正确或不稳定。

* <h4 id="LuaKCurl_AddPostRawData">AddPostRawData</h4>
> () KCurl:AddPostRawData(pcszData)

添加原始 POST 数据。

- `pcszData` 用 `lua_tolstring` 读取（会做长度校验），随后传给 `AddRawPost(pcszData)`。

* <h4 id="LuaKCurl_OnProgress">OnProgress</h4>
> () KCurl:OnProgress(fn)

设置进度回调。

- 必须且只能传 2 个参数（`self`、`fn`）。
- `fn` 必须是 Lua function。

* <h4 id="LuaKCurl_OnSuccess">OnSuccess</h4>
> () KCurl:OnSuccess(fn)

设置成功回调。

- 必须且只能传 2 个参数（`self`、`fn`）。
- `fn` 必须是 Lua function。

* <h4 id="LuaKCurl_OnError">OnError</h4>
> () KCurl:OnError(fn)

设置失败回调。

- 必须且只能传 2 个参数（`self`、`fn`）。
- `fn` 必须是 Lua function。

* <h4 id="LuaKCurl_OnComplete">OnComplete</h4>
> () KCurl:OnComplete(fn)

设置完成回调（无论成功或失败）。

- 必须且只能传 2 个参数（`self`、`fn`）。
- `fn` 必须是 Lua function。

* <h4 id="LuaKCurl_Perform">Perform</h4>
> () KCurl:Perform()

开始执行请求。

- 必须且只能传 1 个参数（`self`）。
- 执行前会关闭 TLS 证书/主机校验。
