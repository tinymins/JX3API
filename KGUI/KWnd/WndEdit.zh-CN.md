[English](./WndEdit.md) | 中文

# WndEdit（编辑框）

说明：

- `WndEdit` 继承 `WndWindow` 的全部方法；此处仅列出新增方法。
- 大多数文本相关 API 都支持可选参数 `eFireType`（事件触发类型，数值枚举），与实现保持一致。

[`SetPadding`](#LuaEdit_SetPadding)
[`GetPadding`](#LuaEdit_GetPadding)
[`GetContentSize`](#LuaEdit_GetContentSize)
[`SetText`](#LuaEdit_SetText)
[`GetText`](#LuaEdit_GetText)
[`GetTextLength`](#LuaEdit_GetTextLength)
[`GetImageCount`](#LuaEdit_GetImageCount)
[`ClearText`](#LuaEdit_ClearText)
[`InsertObj`](#LuaEdit_InsertObj)
[`GetTextStruct`](#LuaEdit_GetTextStruct)
[`SetType`](#LuaEdit_SetType)
[`SetLimit`](#LuaEdit_SetLimit)
[`GetLimit`](#LuaEdit_GetLimit)
[`SetLimitMultiByte`](#LuaEdit_SetLimitMultiByte)
[`IsLimitMultiByte`](#LuaEdit_IsLimitMultiByte)
[`SelectAll`](#LuaEdit_SelectAll)
[`CancelSelect`](#LuaEdit_CancelSelect)
[`SetFontScheme`](#LuaEdit_SetFontScheme)
[`GetFontScheme`](#LuaEdit_GetFontScheme)
[`SetFontColor`](#LuaEdit_SetFontColor)
[`InsertText`](#LuaEdit_InsertText)
[`Backspace`](#LuaEdit_Backspace)
[`SetMultiLine`](#LuaEdit_SetMultiLine)
[`IsMultiLine`](#LuaEdit_IsMultiLine)
[`SetFontSpacing`](#LuaEdit_SetFontSpacing)
[`SetRowSpacing`](#LuaEdit_SetRowSpacing)
[`SetFocusBgColor`](#LuaEdit_SetFocusBgColor)
[`SetSelectBgColor`](#LuaEdit_SetSelectBgColor)
[`SetSelectFontScheme`](#LuaEdit_SetSelectFontScheme)
[`SetCurSel`](#LuaEdit_SetCurSel)
[`SetCaretPos`](#LuaEdit_SetCaretPos)
[`GetCaretPos`](#LuaEdit_GetCaretPos)
[`SetPlaceholderRelX`](#LuaEdit_SetPlaceholderRelX)
[`GetPlaceholderRelX`](#LuaEdit_GetPlaceholderRelX)
[`SetPlaceholderRelY`](#LuaEdit_SetPlaceholderRelY)
[`GetPlaceholderRelY`](#LuaEdit_GetPlaceholderRelY)
[`SetPlaceholderText`](#LuaEdit_SetPlaceholderText)
[`GetPlaceholderText`](#LuaEdit_GetPlaceholderText)
[`SetPlaceholderFontScheme`](#LuaEdit_SetPlaceholderFontScheme)
[`GetPlaceholderFontScheme`](#LuaEdit_GetPlaceholderFontScheme)
[`SetPlaceholderFontColor`](#LuaEdit_SetPlaceholderFontColor)
[`GetPlaceholderFontColor`](#LuaEdit_GetPlaceholderFontColor)
[`SetPlaceholderVAlign`](#LuaEdit_SetPlaceholderVAlign)
[`GetPlaceholderVAlign`](#LuaEdit_GetPlaceholderVAlign)
[`SetPlaceholderHAlign`](#LuaEdit_SetPlaceholderHAlign)
[`GetPlaceholderHAlign`](#LuaEdit_GetPlaceholderHAlign)
[`SetPlaceholderAlpha`](#LuaEdit_SetPlaceholderAlpha)
[`GetPlaceholderAlpha`](#LuaEdit_GetPlaceholderAlpha)
[`SetStatus`](#LuaEdit_SetStatus)
[`IsStatus`](#LuaEdit_IsStatus)

* <h4 id="LuaEdit_SetPadding">SetPadding</h4>

 > (`void`) WndEdit:SetPadding(`number` all)

 > (`void`) WndEdit:SetPadding(`number` topBottom, `number` leftRight)

 > (`void`) WndEdit:SetPadding(`number` top, `number` right, `number` bottom, `number` left)

说明：

- 对应 C++ 绑定中允许 3 种参数形式（不含 `self`）：`all` / `topBottom + leftRight` / `top + right + bottom + left`。
- 传入的数值会直接作为 padding 使用（实现中未做 `UIScale` 换算）。
- 参数个数不匹配时会触发错误日志，但 Lua 层仍然返回 0 个值。

* <h4 id="LuaEdit_GetPadding">GetPadding</h4>

 > (`number` top, `number` right, `number` bottom, `number` left) WndEdit:GetPadding()

说明：

- 只接受 `self` 一个参数。
- 依次返回 `top`、`right`、`bottom`、`left`（共 4 个返回值）。

* <h4 id="LuaEdit_GetContentSize">GetContentSize</h4>

 > (`number` w, `number` h) WndEdit:GetContentSize([`bool|number` bIncludingPadding = true])

说明：

- 返回值会在 Lua 层按 `UIScale` 还原（内部值 / `Station.GetUIScale()`）。

* <h4 id="LuaEdit_SetText">SetText</h4>

 > (`void`) WndEdit:SetText(`string` szText[, `number` eFireType])

说明：

- 参数个数必须为 2 或 3。
- `szText` 会按当前代码页从多字节转换为宽字符串（`CA2WEX(..., GetCodePage())`）；传入 `nil` 时等价于设置为空字符串。
- 可选参数 `eFireType` 会传给底层 `SetText(..., eFireType)`，用于控制触发事件的方式。

* <h4 id="LuaEdit_GetText">GetText</h4>

 > (`string` szText) WndEdit:GetText()

说明：

- 只接受 `self` 一个参数。
- 底层返回 `NULL` 时会在 Lua 层转换为 `""`（空字符串）。
- 返回值会按当前代码页从宽字符串转换回多字节字符串（`CW2AEX(..., GetCodePage())`）。

* <h4 id="LuaEdit_GetTextLength">GetTextLength</h4>

 > (`number` nLen) WndEdit:GetTextLength([`bool|number` bMultiByte = true])

说明：

- `bMultiByte` 支持 `bool` 或 `number`（非 0 视为 true），默认 true。
- 即使参数校验失败（例如传入参数个数为 0），Lua 层仍会返回一个数值；失败路径下 `nLen` 为 0。

* <h4 id="LuaEdit_GetImageCount">GetImageCount</h4>

 > (`number` nCount) WndEdit:GetImageCount()

说明：

- 返回编辑框中插入对象（图片/动画等）的数量。
- 即使校验失败，Lua 层也会返回一个数值；失败路径下 `nCount` 为 0。

* <h4 id="LuaEdit_ClearText">ClearText</h4>

 > (`void`) WndEdit:ClearText([`number` eFireType])

说明：

- 参数个数必须为 1 或 2。
- 可选 `eFireType` 会传给底层 `ClearText(eFireType)`。

* <h4 id="LuaEdit_InsertObj">InsertObj</h4>

 > (`void`) WndEdit:InsertObj(`string` name, `table` tObj[, `number` eFireType])

说明：

- 参数个数必须为 3 或 4；`name` 必须为非空字符串；`tObj` 必须为 table。
- 可选 `eFireType` 会传给底层插入逻辑，用于控制触发事件的方式。
- `tObj` 支持的字段（取决于实现分支）：

- 若未设置 `imagetype`：会通过 `luaL_ref` 将整个 `tObj` 保存下来，供引擎回调用。
- `imagetype == "animate"`：
  - `path`（string）、`group`（number）
  - 可选：`width`/`height`（number）
- `imagetype == "image"`：
  - `path`（string）、`frame`（number）
  - 可选：`width`/`height`（number）

* <h4 id="LuaEdit_GetTextStruct">GetTextStruct</h4>

 > (`table` tStruct) WndEdit:GetTextStruct([`bool` bCursor = false])

说明：

- 由底层 `GetTextLuaStruct` 生成，并以 table 形式返回。

* <h4 id="LuaEdit_SetType">SetType</h4>

 > (`void`) WndEdit:SetType(`number` nType)

说明：

- 参数个数必须为 2。
- `nType` 直接传给底层 `SetType(nType)`。

* <h4 id="LuaEdit_SetLimit">SetLimit</h4>

 > (`void`) WndEdit:SetLimit(`number` nLimit)

说明：

- 参数个数必须为 2。
- `nLimit` 直接传给底层 `SetLimit(nLimit)`（是否允许 `-1` 等特殊值以底层实现为准）。

* <h4 id="LuaEdit_GetLimit">GetLimit</h4>

 > (`number` nLimit) WndEdit:GetLimit()

说明：

- 只接受 `self` 一个参数。
- 返回底层 `GetLimit()` 的结果。

* <h4 id="LuaEdit_SetLimitMultiByte">SetLimitMultiByte</h4>

 > (`void`) WndEdit:SetLimitMultiByte(`bool|number` bMultiByte)

说明：

- 参数个数必须为 2。
- `bMultiByte` 支持 `bool` 或 `number`（非 0 视为 true），并传给底层 `SetLimitMultiByte(...)`。

* <h4 id="LuaEdit_IsLimitMultiByte">IsLimitMultiByte</h4>

 > (`bool` bMultiByte) WndEdit:IsLimitMultiByte()

说明：

- 只接受 `self` 一个参数。
- 返回底层 `IsLimitMultiByte()` 的结果。

* <h4 id="LuaEdit_SelectAll">SelectAll</h4>

 > (`void`) WndEdit:SelectAll()

说明：

- 全选当前文本。

* <h4 id="LuaEdit_CancelSelect">CancelSelect</h4>

 > (`void`) WndEdit:CancelSelect()

说明：

- 取消当前选区。

* <h4 id="LuaEdit_SetFontScheme">SetFontScheme</h4>

 > (`void`) WndEdit:SetFontScheme(`number` nFontScheme)

说明：

- 参数个数必须为 2。
- `nFontScheme` 直接传给底层 `SetFontScheme(...)`。

* <h4 id="LuaEdit_GetFontScheme">GetFontScheme</h4>

 > (`number` nFontScheme) WndEdit:GetFontScheme()

说明：

- 只接受 `self` 一个参数。
- 返回底层字体方案编号。

* <h4 id="LuaEdit_SetFontColor">SetFontColor</h4>

 > (`void`) WndEdit:SetFontColor(`number` r, `number` g, `number` b)

说明：

- 参数个数必须为 4。
- `r`/`g`/`b` 会各自按 `0xFF` 取低 8 位，并组合为 `0xFFRRGGBB`（alpha 固定为 255）。

* <h4 id="LuaEdit_InsertText">InsertText</h4>

 > (`void`) WndEdit:InsertText(`string` szText[, `number` eFireType])

说明：

- 参数个数必须为 2 或 3；`szText` 必须为非空字符串。
- `szText` 会按当前代码页转换为宽字符串后插入/追加（`AppendString(CA2WEX(...))`）。
- 可选 `eFireType` 会透传给底层，用于控制触发事件的方式。

* <h4 id="LuaEdit_Backspace">Backspace</h4>

 > (`void`) WndEdit:Backspace()

说明：

- 执行一次退格删除。

* <h4 id="LuaEdit_SetMultiLine">SetMultiLine</h4>

 > (`void`) WndEdit:SetMultiLine(`bool|number` bMultiLine)

说明：

- 参数个数必须为 2。
- `bMultiLine` 支持 `bool` 或 `number`（非 0 视为 true）。
- 底层通过设置/清除 `WNDEDIT_ES_MULTI_LINE` 状态位实现。

* <h4 id="LuaEdit_IsMultiLine">IsMultiLine</h4>

 > (`bool` bMultiLine) WndEdit:IsMultiLine()

说明：

- 只接受 `self` 一个参数。
- 等价于检测 `WNDEDIT_ES_MULTI_LINE` 状态位。

* <h4 id="LuaEdit_SetFontSpacing">SetFontSpacing</h4>

 > (`void`) WndEdit:SetFontSpacing(`number` fSpacing)

说明：

- 参数个数必须为 2。
- `fSpacing` 以浮点数形式传入底层 `SetFontSpacing(...)`。

* <h4 id="LuaEdit_SetRowSpacing">SetRowSpacing</h4>

 > (`void`) WndEdit:SetRowSpacing(`number` fSpacing)

说明：

- 参数个数必须为 2。
- `fSpacing` 以浮点数形式传入底层 `SetRowSpacing(...)`。

* <h4 id="LuaEdit_SetFocusBgColor">SetFocusBgColor</h4>

 > (`void`) WndEdit:SetFocusBgColor(`number` r, `number` g, `number` b)

说明：

- 参数个数必须为 4。
- `r`/`g`/`b` 会各自按 `0xFF` 取低 8 位，并组合为 `0xFFRRGGBB`（alpha 固定为 255）。

* <h4 id="LuaEdit_SetSelectBgColor">SetSelectBgColor</h4>

 > (`void`) WndEdit:SetSelectBgColor(`number` r, `number` g, `number` b)

说明：

- 参数个数必须为 4。
- `r`/`g`/`b` 会各自按 `0xFF` 取低 8 位，并组合为 `0xFFRRGGBB`（alpha 固定为 255）。

* <h4 id="LuaEdit_SetSelectFontScheme">SetSelectFontScheme</h4>

 > (`void`) WndEdit:SetSelectFontScheme(`number` nFontScheme)

说明：

- 参数个数必须为 2。
- 设置选区文本使用的字体方案编号。

* <h4 id="LuaEdit_SetCurSel">SetCurSel</h4>

 > (`void`) WndEdit:SetCurSel(`number` nStart[, `number` nEnd = -1[, `bool|number` bMultiByte = true]])

说明：

- `nStart`/`nEnd` 为 1-based；负数表示从末尾向前计数。

* <h4 id="LuaEdit_SetCaretPos">SetCaretPos</h4>

 > (`void`) WndEdit:SetCaretPos(`number` dwPos[, `number` nAfterFlag = 0])

说明：

- 绑定实现对参数个数校验较宽松：内部会直接读取第 2 个参数作为 `dwPos`。
- 若未传 `dwPos`，实现会按 0 处理；建议始终显式传入 `dwPos`。
- 可选 `nAfterFlag` 为数值，直接传给底层 `SetCaretPos(dwPos, nAfterFlag)`。

* <h4 id="LuaEdit_GetCaretPos">GetCaretPos</h4>

 > (`number` dwPos) WndEdit:GetCaretPos()

说明：

- 只接受 `self` 一个参数。
- 返回 `GetCaretPos()` 的结果（以整数形式返回）。

* <h4 id="LuaEdit_SetPlaceholderRelX">SetPlaceholderRelX</h4>

 > (`void`) WndEdit:SetPlaceholderRelX(`number` x)

说明：

- 参数个数必须为 2。
- `x` 以浮点数形式传入底层 `SetPlaceholderRelX(...)`。

* <h4 id="LuaEdit_GetPlaceholderRelX">GetPlaceholderRelX</h4>

 > (`number` x) WndEdit:GetPlaceholderRelX()

说明：

- 只接受 `self` 一个参数。
- 返回占位符相对 X（浮点数）。

* <h4 id="LuaEdit_SetPlaceholderRelY">SetPlaceholderRelY</h4>

 > (`void`) WndEdit:SetPlaceholderRelY(`number` y)

说明：

- 参数个数必须为 2。
- `y` 以浮点数形式传入底层 `SetPlaceholderRelY(...)`。

* <h4 id="LuaEdit_GetPlaceholderRelY">GetPlaceholderRelY</h4>

 > (`number` y) WndEdit:GetPlaceholderRelY()

说明：

- 只接受 `self` 一个参数。
- 返回占位符相对 Y（浮点数）。

* <h4 id="LuaEdit_SetPlaceholderText">SetPlaceholderText</h4>

 > (`void`) WndEdit:SetPlaceholderText(`string` szText)

说明：

- 参数个数必须为 2；`szText` 必须为非空字符串。
- `szText` 会按当前代码页从多字节转换为宽字符串后设置（`CA2WEX(..., GetCodePage())`）。

* <h4 id="LuaEdit_GetPlaceholderText">GetPlaceholderText</h4>

 > (`string` szText) WndEdit:GetPlaceholderText()

说明：

- 只接受 `self` 一个参数。
- 返回值会按当前代码页从宽字符串转换回多字节字符串（`CW2AEX(..., GetCodePage())`）。

* <h4 id="LuaEdit_SetPlaceholderFontScheme">SetPlaceholderFontScheme</h4>

 > (`void`) WndEdit:SetPlaceholderFontScheme(`number` nFontScheme)

说明：

- 参数个数必须为 2。
- 设置占位符文本使用的字体方案编号。

* <h4 id="LuaEdit_GetPlaceholderFontScheme">GetPlaceholderFontScheme</h4>

 > (`number` nFontScheme) WndEdit:GetPlaceholderFontScheme()

说明：

- 只接受 `self` 一个参数。
- 返回占位符字体方案编号。

* <h4 id="LuaEdit_SetPlaceholderFontColor">SetPlaceholderFontColor</h4>

 > (`void`) WndEdit:SetPlaceholderFontColor(`number` r, `number` g, `number` b)

说明：

- 参数个数必须为 4。
- `r`/`g`/`b` 会各自按 `0xFF` 取低 8 位，并组合为 `0xFFRRGGBB`（alpha 固定为 255）。

* <h4 id="LuaEdit_GetPlaceholderFontColor">GetPlaceholderFontColor</h4>

 > (`number` r, `number` g, `number` b) WndEdit:GetPlaceholderFontColor()

说明：

- 只接受 `self` 一个参数。
- 依次返回 `r`、`g`、`b`（从颜色值中拆出，不包含 alpha）。

* <h4 id="LuaEdit_SetPlaceholderVAlign">SetPlaceholderVAlign</h4>

 > (`void`) WndEdit:SetPlaceholderVAlign(`number` nAlign)

说明：

- 参数个数必须为 2。
- `nAlign` 直接传给底层 `SetPlaceholderVAlign(nAlign)`。

* <h4 id="LuaEdit_GetPlaceholderVAlign">GetPlaceholderVAlign</h4>

 > (`number` nAlign) WndEdit:GetPlaceholderVAlign()

说明：

- 只接受 `self` 一个参数。
- 返回占位符的垂直对齐枚举值。

* <h4 id="LuaEdit_SetPlaceholderHAlign">SetPlaceholderHAlign</h4>

 > (`void`) WndEdit:SetPlaceholderHAlign(`number` nAlign)

说明：

- 参数个数必须为 2。
- `nAlign` 直接传给底层 `SetPlaceholderHAlign(nAlign)`。

* <h4 id="LuaEdit_GetPlaceholderHAlign">GetPlaceholderHAlign</h4>

 > (`number` nAlign) WndEdit:GetPlaceholderHAlign()

说明：

- 只接受 `self` 一个参数。
- 返回占位符的水平对齐枚举值。

* <h4 id="LuaEdit_SetPlaceholderAlpha">SetPlaceholderAlpha</h4>

 > (`void`) WndEdit:SetPlaceholderAlpha(`number` nAlpha)

说明：

- 参数个数必须为 2。
- `nAlpha` 直接传给底层 `SetPlaceholderAlpha(nAlpha)`；实现未在 Lua 层做范围裁剪。

* <h4 id="LuaEdit_GetPlaceholderAlpha">GetPlaceholderAlpha</h4>

 > (`number` nAlpha) WndEdit:GetPlaceholderAlpha()

说明：

- 只接受 `self` 一个参数。
- 返回占位符 alpha 值。

* <h4 id="LuaEdit_SetStatus">SetStatus</h4>

 > (`void`) WndEdit:SetStatus(`number` dwStatus, `bool` bEnable)

说明：

- 参数个数必须为 3。
- `dwStatus` 必须为 `number`。
- `bEnable` 在实现中要求必须为 `boolean`（不接受 `number` 充当布尔）。
- 校验失败时会调用 `LuaMsgError` 输出错误信息，并返回 0 个值。

* <h4 id="LuaEdit_IsStatus">IsStatus</h4>

 > (`bool` bEnable) WndEdit:IsStatus(`number` dwStatus)

说明：

- 参数个数必须为 2。
- `dwStatus` 必须为 `number`。
- 返回 `pWnd->IsStatus(dwStatus)` 的结果（Lua boolean）。
- 校验失败时会调用 `LuaMsgError` 输出错误信息，并不返回值。
