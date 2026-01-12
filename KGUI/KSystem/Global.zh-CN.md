[English](./Global.md) | 中文

# Global

## 函数

* <h4 id="LuaFormatTime">FormatTime</h4>
> FormatTime(pcszFormat, nTime) -> szText

按 `pcszFormat` 将 `nTime`（Unix 时间戳，秒）格式化为字符串。

* <h4 id="LuaMoneyToGoldSilverAndCopper">MoneyToGoldSilverAndCopper</h4>
> MoneyToGoldSilverAndCopper(nMoney) -> nGold, nSilver, nCopper

将金钱值转换为金/银/铜。

* <h4 id="LuaGoldSilverAndCopperToMoney">GoldSilverAndCopperToMoney</h4>
> GoldSilverAndCopperToMoney(nGold, nSilver, nCopper) -> nMoney

将金/银/铜转换为金钱值。

* <h4 id="LuaFormatString">FormatString</h4>
> FormatString(szFormat, ...) -> szText

使用自定义格式与参数格式化字符串。

* <h4 id="LuaGetTime">GetTime</h4>
> GetTime() -> dwTick

返回 tick 计数。

* <h4 id="LuaGetTickCount">GetTickCount</h4>
> GetTickCount() -> dwTick

返回 tick 计数。

* <h4 id="LuaGetFPS">GetFPS</h4>
> GetFPS() -> nFPS

返回当前 FPS。

* <h4 id="LuaGetUserAccount">GetUserAccount</h4>
> GetUserAccount() -> pcszAccount

获取当前账号。

* <h4 id="LuaGetUserServer">GetUserServer</h4>
> GetUserServer() -> pcszDisplayRegion, pcszDisplayServer, pcszRegion, pcszServer, pcszRealRegion, pcszRealServer, pcszServerIP, nServerPort

获取当前服务器选择，以及服务器 IP/端口。

* <h4 id="LuaGetUserRoleName">GetUserRoleName</h4>
> GetUserRoleName() -> pcszRoleName

获取当前角色名。

* <h4 id="LuaGetUserDataFolder">GetUserDataFolder</h4>
> GetUserDataFolder() -> pcszFolder

返回用户数据文件夹名。

* <h4 id="LuaEncodeData">EncodeData</h4>
> EncodeData(bin[, bCRCCheck[, bCompress]]) -> encoded

对二进制数据进行封装编码。

- `bCRCCheck`（可选）：boolean。
- `bCompress`（可选）：boolean。

* <h4 id="LuaDecodeData">DecodeData</h4>
> DecodeData(encoded) -> bin

解码 `EncodeData` 生成的数据。

失败时无返回。

* <h4 id="LuaIsEncodedData">IsEncodedData</h4>
> IsEncodedData(encoded) -> bIsEncoded

判断输入是否像是由 `EncodeData` 产生的数据。

* <h4 id="LuaLoadDataFromFile">LoadDataFromFile</h4>
> LoadDataFromFile(pcszFile[, bPak[, pszPassphrase]]) -> bin

读取文件内容并返回二进制 string。

- `bPak`（可选）：boolean。
- `pszPassphrase`（可选）：string。提供时会尝试解密。

失败时无返回。

* <h4 id="LuaAsyncLoadDataFromFile">AsyncLoadDataFromFile</h4>
> AsyncLoadDataFromFile(pcszFile, fnCallback[, bPak[, pszPassphrase]])

异步读取文件数据。

- `fnCallback(dataOrNil)`：成功传入二进制 string，失败传 `nil`。

* <h4 id="LuaSaveDataToFile">SaveDataToFile</h4>
> SaveDataToFile(bin, pcszFile[, pszPassphrase])

把二进制数据写入文件。

- `pszPassphrase`（可选）：string。提供时会先加密再写入。

* <h4 id="LuaAsyncSaveDataToFile">AsyncSaveDataToFile</h4>
> AsyncSaveDataToFile(bin, pcszFile, fnCallbackOrNil[, pszPassphrase[, bCRCCheck[, bCompress]]])

异步写入文件。

- `fnCallbackOrNil(bOk)`：完成后可能被调用。
- 按当前实现，如果在回调之后继续追加可选参数，回调可能会被忽略。

* <h4 id="LuaGetOpenFileName">GetOpenFileName</h4>
> GetOpenFileName([pcszTitle[, pcszFilter[, pcszInitialDir]]]) -> pcszFile

弹出"打开文件"对话框并返回选中文件路径。

* <h4 id="LuaIsMultiThread">IsMultiThread</h4>
> IsMultiThread() -> bMultiThread

返回是否启用多线程。

* <h4 id="LuaSetDataToClip">SetDataToClip</h4>
> SetDataToClip(szText)

把 `szText` 写入剪贴板。

* <h4 id="LuaGetCurrentProcessID">GetCurrentProcessID</h4>
> GetCurrentProcessID() -> nPID

返回当前进程 ID。

* <h4 id="LuaGetSystemCScreen">GetSystemCScreen</h4>
> GetSystemCScreen() -> nScreenX, nScreenY

返回屏幕分辨率（像素）。

* <h4 id="LuaMD5Encrypt">KGUIEncrypt</h4>
> KGUIEncrypt(pcszValue) -> pcszMD5

返回基于 `pcszValue` 与内部 key 计算得到的 MD5 字符串。
