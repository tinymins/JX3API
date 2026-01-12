English | [中文](./Global.zh-CN.md)

# Global

## Functions

* <h4 id="LuaFormatTime">FormatTime</h4>
> FormatTime(pcszFormat, nTime) -> szText

Formats `nTime` (Unix timestamp, seconds) into a string using `pcszFormat`.

* <h4 id="LuaMoneyToGoldSilverAndCopper">MoneyToGoldSilverAndCopper</h4>
> MoneyToGoldSilverAndCopper(nMoney) -> nGold, nSilver, nCopper

Converts money value to gold/silver/copper.

* <h4 id="LuaGoldSilverAndCopperToMoney">GoldSilverAndCopperToMoney</h4>
> GoldSilverAndCopperToMoney(nGold, nSilver, nCopper) -> nMoney

Converts gold/silver/copper to a money value.

* <h4 id="LuaFormatString">FormatString</h4>
> FormatString(szFormat, ...) -> szText

Formats a string using a custom format with parameters.

* <h4 id="LuaGetTime">GetTime</h4>
> GetTime() -> dwTick

Returns a tick count.

* <h4 id="LuaGetTickCount">GetTickCount</h4>
> GetTickCount() -> dwTick

Returns a tick count.

* <h4 id="LuaGetFPS">GetFPS</h4>
> GetFPS() -> nFPS

Returns current FPS.

* <h4 id="LuaGetUserAccount">GetUserAccount</h4>
> GetUserAccount() -> pcszAccount

Gets current user account.

* <h4 id="LuaGetUserServer">GetUserServer</h4>
> GetUserServer() -> pcszDisplayRegion, pcszDisplayServer, pcszRegion, pcszServer, pcszRealRegion, pcszRealServer, pcszServerIP, nServerPort

Gets current server selection and server IP/port.

* <h4 id="LuaGetUserRoleName">GetUserRoleName</h4>
> GetUserRoleName() -> pcszRoleName

Gets current role name.

* <h4 id="LuaGetUserDataFolder">GetUserDataFolder</h4>
> GetUserDataFolder() -> pcszFolder

Returns the user data folder name.

* <h4 id="LuaEncodeData">EncodeData</h4>
> EncodeData(bin[, bCRCCheck[, bCompress]]) -> encoded

Encodes binary data.

- `bCRCCheck` (optional): boolean.
- `bCompress` (optional): boolean.

* <h4 id="LuaDecodeData">DecodeData</h4>
> DecodeData(encoded) -> bin

Decodes data encoded by `EncodeData`.

On failure, it returns nothing.

* <h4 id="LuaIsEncodedData">IsEncodedData</h4>
> IsEncodedData(encoded) -> bIsEncoded

Checks whether the input looks like data produced by `EncodeData`.

* <h4 id="LuaLoadDataFromFile">LoadDataFromFile</h4>
> LoadDataFromFile(pcszFile[, bPak[, pszPassphrase]]) -> bin

Loads file content as a binary string.

- `bPak` (optional): boolean.
- `pszPassphrase` (optional): string. If provided, decrypts the data.

On failure, it returns nothing.

* <h4 id="LuaAsyncLoadDataFromFile">AsyncLoadDataFromFile</h4>
> AsyncLoadDataFromFile(pcszFile, fnCallback[, bPak[, pszPassphrase]])

Asynchronously loads file data.

- `fnCallback(dataOrNil)` will be called with the binary string, or `nil` on failure.

* <h4 id="LuaSaveDataToFile">SaveDataToFile</h4>
> SaveDataToFile(bin, pcszFile[, pszPassphrase])

Writes binary data to a file.

- `pszPassphrase` (optional): string. If provided, encrypts the data before writing.

* <h4 id="LuaAsyncSaveDataToFile">AsyncSaveDataToFile</h4>
> AsyncSaveDataToFile(bin, pcszFile, fnCallbackOrNil[, pszPassphrase[, bCRCCheck[, bCompress]]])

Asynchronously writes data to a file.

- `fnCallbackOrNil(bOk)` may be called when finished.
- As implemented, the callback may be ignored when extra optional parameters are appended after it.

* <h4 id="LuaGetOpenFileName">GetOpenFileName</h4>
> GetOpenFileName([pcszTitle[, pcszFilter[, pcszInitialDir]]]) -> pcszFile

Shows a file open dialog and returns the selected file path.

* <h4 id="LuaIsMultiThread">IsMultiThread</h4>
> IsMultiThread() -> bMultiThread

Returns whether multithreading is enabled.

* <h4 id="LuaSetDataToClip">SetDataToClip</h4>
> SetDataToClip(szText)

Copies `szText` into the clipboard.

* <h4 id="LuaGetCurrentProcessID">GetCurrentProcessID</h4>
> GetCurrentProcessID() -> nPID

Returns current process ID.

* <h4 id="LuaGetSystemCScreen">GetSystemCScreen</h4>
> GetSystemCScreen() -> nScreenX, nScreenY

Returns screen size in pixels.

* <h4 id="LuaMD5Encrypt">KGUIEncrypt</h4>
> KGUIEncrypt(pcszValue) -> pcszMD5

Returns an MD5 string derived from `pcszValue` and internal keys.
