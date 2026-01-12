# KCurl

Notes:

- The module registers a global function `Curl_Create` and a userdata metatable `KCurl`.
- `KCurl:Perform()` explicitly disables TLS verification (`CURLOPT_SSL_VERIFYPEER = 0`, `CURLOPT_SSL_VERIFYHOST = 0`).
- `KCurlScriptTable::Load()` also calls `luaopen_webclient(L)`; any extra APIs exported by that module are not covered here.

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

Creates a `KCurl` request object bound to `pcszUrl`.

- Requires exactly 1 argument.
- `pcszUrl` is read using `lua_tostring` and must not be `nil`.

On success it returns a `KCurl` userdata. On failure it returns nothing.

* <h4 id="LuaKCurl_SetMethod">SetMethod</h4>
> () KCurl:SetMethod(pcszMethod)

Sets the HTTP method.

- Requires exactly 2 arguments (`self`, `pcszMethod`).
- Recognized method strings: `"POST"`, `"PUT"`, `"DELETE"`.
- Any other value is treated as GET (falls back to `CURLOPT_HTTPGET`).

* <h4 id="LuaKCurl_SetTimeout">SetTimeout</h4>
> () KCurl:SetTimeout(nTimeout)

Sets `CURLOPT_TIMEOUT`.

- `nTimeout` is read via `lua_tonumber` and cast to `int`.

* <h4 id="LuaKCurl_SetConnTimeout">SetConnTimeout</h4>
> () KCurl:SetConnTimeout(nTimeout)

Sets `CURLOPT_CONNECTTIMEOUT`.

- `nTimeout` is read via `lua_tonumber` and cast to `int`.

* <h4 id="LuaKCurl_AddHeader">AddHeader</h4>
> () KCurl:AddHeader(pcszHeader)

Adds a raw HTTP header line.

- `pcszHeader` must be a non-nil string.

* <h4 id="LuaKCurl_AddPostData">AddPostData</h4>
> () KCurl:AddPostData(pcszKey, pcszData)

Adds a multipart/form-data field.

- Requires exactly 3 arguments (`self`, `pcszKey`, `pcszData`).
- `pcszData` is read via `lua_tolstring`, so it can contain binary data and its byte length is preserved.

* <h4 id="LuaKCurl_AddPostFile">AddPostFile</h4>
> () KCurl:AddPostFile(pcszKey, pcszConentType, pcszFile, pcszFileName)

Adds a multipart/form-data file part.

- Requires exactly 5 arguments (`self`, `pcszKey`, `pcszConentType`, `pcszFile`, `pcszFileName`).

Note: the current implementation appears to have multiple issues (e.g. an uninitialized `pcszKey` variable and passing pointer sizes), so behavior may be incorrect or unstable.

* <h4 id="LuaKCurl_AddPostRawData">AddPostRawData</h4>
> () KCurl:AddPostRawData(pcszData)

Adds raw POST data.

- `pcszData` is read via `lua_tolstring` (length is validated), then passed to `AddRawPost(pcszData)`.

* <h4 id="LuaKCurl_OnProgress">OnProgress</h4>
> () KCurl:OnProgress(fn)

Sets a Lua callback invoked for progress updates.

- Requires exactly 2 arguments (`self`, `fn`).
- `fn` must be a Lua function.

* <h4 id="LuaKCurl_OnSuccess">OnSuccess</h4>
> () KCurl:OnSuccess(fn)

Sets a Lua callback invoked when the request succeeds.

- Requires exactly 2 arguments (`self`, `fn`).
- `fn` must be a Lua function.

* <h4 id="LuaKCurl_OnError">OnError</h4>
> () KCurl:OnError(fn)

Sets a Lua callback invoked when the request fails.

- Requires exactly 2 arguments (`self`, `fn`).
- `fn` must be a Lua function.

* <h4 id="LuaKCurl_OnComplete">OnComplete</h4>
> () KCurl:OnComplete(fn)

Sets a Lua callback invoked when the request completes (success or error).

- Requires exactly 2 arguments (`self`, `fn`).
- `fn` must be a Lua function.

* <h4 id="LuaKCurl_Perform">Perform</h4>
> () KCurl:Perform()

Starts the request.

- Requires exactly 1 argument (`self`).
- Disables TLS certificate/host verification before performing the request.
