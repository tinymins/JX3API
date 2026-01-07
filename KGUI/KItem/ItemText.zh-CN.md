[English](./ItemText.md) | 中文

# ItemText

[`SetFontScheme`](#LuaItemText_SetFontScheme)
[`GetFontScheme`](#LuaItemText_GetFontScheme)
[`SetRange`](#LuaItemText_SetRange)
[`SetTime`](#LuaItemText_SetTime)
[`SetNumber`](#LuaItemText_SetNumber)
[`GetNumber`](#LuaItemText_GetNumber)
[`SprintfText`](#LuaItemText_SprintfText)
[`SetText`](#LuaItemText_SetText)
[`GetText`](#LuaItemText_GetText)
[`GetTextLen`](#LuaItemText_GetTextLen)
[`SetVAlign`](#LuaItemText_SetVAlign)
[`GetVAlign`](#LuaItemText_GetVAlign)
[`SetHAlign`](#LuaItemText_SetHAlign)
[`GetHAlign`](#LuaItemText_GetHAlign)
[`SetRowSpacing`](#LuaItemText_SetRowSpacing)
[`GetRowSpacing`](#LuaItemText_GetRowSpacing)
[`SetMultiLine`](#LuaItemText_SetMultiLine)
[`IsMultiLine`](#LuaItemText_IsMultiLine)
[`FormatTextForDraw`](#LuaItemText_FormatTextForDraw)
[`AutoSize`](#LuaItemText_AutoSize)
[`SetCenterEachLine`](#LuaItemText_SetCenterEachLine)
[`IsCenterEachLine`](#LuaItemText_IsCenterEachLine)
[`SetFontSpacing`](#LuaItemText_SetFontSpacing)
[`GetFontSpacing`](#LuaItemText_GetFontSpacing)
[`SetRichText`](#LuaItemText_SetRichText)
[`IsRichText`](#LuaItemText_IsRichText)
[`GetFontScale`](#LuaItemText_GetFontScale)
[`SetFontScale`](#LuaItemText_SetFontScale)
[`SetFontID`](#LuaItemText_SetFontID)
[`SetFontColor`](#LuaItemText_SetFontColor)
[`SetFontBorder`](#LuaItemText_SetFontBoder)
[`SetFontShadow`](#LuaItemText_SetFontShadow)
[`GetFontID`](#LuaItemText_GetFontID)
[`GetFontColor`](#LuaItemText_GetFontColor)
[`GetFontBoder`](#LuaItemText_GetFontBoder)
[`GetFontProjection`](#LuaItemText_GetFontProjection)
[`GetTextExtent`](#LuaItemText_GetTextExtent)
[`GetTextPosExtent`](#LuaItemText_GetTextPosExtent)
[`IsTextAutoTipEnabled`](#LuaItemText_IsTextAutoTipEnabled)
[`SetTextAutoTipEnabled`](#LuaItemText_SetTextAutoTipEnabled)

* <h4 id="LuaItemText_SetFontScheme">SetFontScheme</h4>
设置文本字体方案。<br>
此 API 会用 `nFontID` 加载 `pFontScheme`，然后依次调用：<br>
[`:SetFontID(pFontScheme->nFontID)`](#LuaItemText_SetFontID)<br>
[`:SetFontColor(pFontScheme->GetFontColor())`](#LuaItemText_SetFontColor)<br>
[`:SetFontBorder(pFontScheme->nBorderSize, pFontScheme->GetBoderColor())`](#LuaItemText_SetFontBoder)<br>
[`:SetFontShadow(pFontScheme->nShadowOffset, pFontScheme->GetShadowColor())`](#LuaItemText_SetFontShadow)<br>
[`:SetFontScale(pFontScheme->fScale)`](#LuaItemText_SetFontScale)<br>

 > (`void`) ItemText:SetFontScheme(`number` nFont)

 ````lua
 ItemText:SetFontScheme(192)
 ````


* <h4 id="LuaItemText_GetFontScheme">GetFontScheme</h4>
获取文本字体方案。

 > (`number` nFont) ItemText:GetFontScheme()

 ````lua
 local nFont = ItemText:GetFontScheme()
 ````

* <h4 id="LuaItemText_SetRange">SetRange</h4>
将文本设置为“区间”格式。

注意：此 API 的效果等同于 [`:SetText(nValue1 .. szDelimiter .. nVlaue2)`](#LuaItemText_SetText)。但此 API 比 `:SetText` 性能更高，因为在拼接字符串时不会产生中间字符串。

实现细节：

- `szDelimiter` 必须为非空字符串。
- 双参数形式下，`szDelimiter` 为单字符 `%` 时会显示百分号（例如 `5%`）。
- 双参数形式下，`szDelimiter` 为单字符 `M` 时会显示 `M`（例如 `5M`）。
- 三参数形式下，`szDelimiter` 为单字符 `/` 时会按 `"%d/%d"` 格式输出。

> * (`void`) ItemText:SetRange(`number` nValue, `string` szDelimiter)
> * (`void`) ItemText:SetRange(`number` nValue1, `string` szDelimiter, `number` nValue2)

 ````lua
 ItemText:SetRange(5, "%")
 ItemText:SetRange(5, "/", 100)
 ````

* <h4 id="LuaItemText_SetTime">SetTime</h4>
将文本设置为时间格式。

注意：此 API 的效果等同于 [`:SetText(("%02d:%02d:%02d"):format(TimeToHMS(nTime)))`](#LuaItemText_SetText)。但此 API 比 `:SetText` 性能更高，因为在拼接字符串时不会产生中间字符串。

注意：绑定层使用 `localtime` 将时间戳转换为本地时间。

 > (`void`) ItemText:SetTime(`number` nTimeStamp)

 ````lua
 ItemText:SetTime(GetCurrentTime())
 ````

* <h4 id="LuaItemText_SetNumber">SetNumber</h4>
将文本设置为纯数字。

注意：此 API 的效果等同于 [`:SetText(tostring(nNumber))`](#LuaItemText_SetText)。但此 API 比 `:SetText` 性能更高，因为在拼接字符串时不会产生中间字符串。

注意：实现会读取 Lua 数字的字符串形式，内部缓冲区长度有限（过长会报错）。建议传入非负整数以避免异常显示。

 > (`void`) ItemText:SetNumber(`number` nNumber)

 ````lua
 ItemText:SetNumber(213928)
 ````

* <h4 id="LuaItemText_GetNumber">GetNumber</h4>
将当前文本按数字解析。

内部使用简单扫描（`%lf`）。如果文本不是合法数字，则返回 `0`。

 > (`number` nNumber) ItemText:GetNumber()

 ````lua
 local nNumber = ItemText:GetNumber()
 ````

* <h4 id="LuaItemText_SetText">SetText</h4>
设置显示文本。

 > (`void`) ItemText:SetText(`string` szText[, `bool` bKey])

如果 `bKey` 为 `true`，则 `szText` 会被当作**全局字符串 key**，实际显示文本会从全局字符串表中加载（key 不存在会报错）。

`szText` 会按当前代码页转换后再传入引擎；当 `szText` 为 `nil` 时会清空为 `""`。

 ````lua
 ItemText:SetText("This is a text.")
 ItemText:SetText("UI_TEXT_KEY", true)
 ````

* <h4 id="LuaItemText_SprintfText">SprintfText</h4>
使用类似 printf 的格式串来格式化并设置文本。

支持的转换说明符：

- `%s`（字符串）
- `%d`（整数）、`%x`/`%X`（十六进制）
- `%f`（数值）
- `%%`（字面量 `%`）

格式串中可以在 `%` 与说明符之间包含宽度/精度部分（数字与 `.`）。

注意：绑定层会校验参数类型（例如 `%s` 需要字符串、`%d/%x/%X/%f` 需要数值）；如果格式串解析失败或参数类型不匹配，会报错并且不返回值。

每个转换说明符会从 `...` 中消耗 1 个参数；未被格式串消耗到的多余参数会被忽略。

 > (`void`) ItemText:SprintfText(`string` szFormat, ...)

 ````lua
 ItemText:SprintfText("%d/%d", 5, 100)
 ItemText:SprintfText("HP:%d%%", 80)
 ItemText:SprintfText("Name:%s  Score:%.2f", "Bob", 98.25)
 ````

* <h4 id="LuaItemText_GetText">GetText</h4>
获取显示文本。

 > (`string` szText) ItemText:GetText()

 ````lua
 local szText = ItemText:GetText()
 ````

* <h4 id="LuaItemText_GetTextLen">GetTextLen</h4>
获取显示文本的长度。

 > (`number` nLen) ItemText:GetTextLen()

 ````lua
 local nLen = ItemText:GetTextLen()
 ````

* <h4 id="LuaItemText_SetVAlign">SetVAlign</h4>
设置文本垂直对齐。枚举：`0-top`、`1-center`、`2-bottom`。

注意：你可能需要调用 [`:FormatTextForDraw()`](#LuaItemText_FormatTextForDraw) 才能立即应用更改并重绘文本。

 > (`void`) ItemText:SetVAlign(`number` nAlign)

 ````lua
 ItemText:SetVAlign(1)
 ````

* <h4 id="LuaItemText_GetVAlign">GetVAlign</h4>
获取文本垂直对齐。

 > (`number` nAlign) ItemText:GetVAlign()

 ````lua
 local nAlign = ItemText:GetVAlign()
 ````

* <h4 id="LuaItemText_SetHAlign">SetHAlign</h4>
设置文本水平对齐。枚举：`0-left`、`1-middle`、`2-right`。

注意：你可能需要调用 [`:FormatTextForDraw()`](#LuaItemText_FormatTextForDraw) 才能立即应用更改并重绘文本。

 > (`void`) ItemText:SetHAlign(`number` nAlign)

 ````lua
 ItemText:SetHAlign(1)
 ````

* <h4 id="LuaItemText_GetHAlign">GetHAlign</h4>
获取文本水平对齐。

 > (`number` nAlign) ItemText:GetHAlign()

 ````lua
 local nAlign = ItemText:GetHAlign()
 ````

* <h4 id="LuaItemText_SetRowSpacing">SetRowSpacing</h4>
设置两行之间的行距。

注意：内部会乘以 `Station.GetUIScale()`。

 > (`void`) ItemText:SetRowSpacing(`number` nSpacing)

 ````lua
 ItemText:SetRowSpacing(3)
 ````

* <h4 id="LuaItemText_GetRowSpacing">GetRowSpacing</h4>
获取两行之间的行距。

注意：返回前内部会先除以 `Station.GetUIScale()`。

 > (`number` nSpacing) ItemText:GetRowSpacing()

 ````lua
 local nSpacing = ItemText:GetRowSpacing()
 ````

* <h4 id="LuaItemText_SetMultiLine">SetMultiLine</h4>
设置该文本控件是否支持多行显示。支持多行显示意味着：当内部文本宽度达到控件宽度时，会自动换行。

 > (`void`) ItemText:SetMultiLine(`bool` bMultiline)

 ````lua
 ItemText:SetMultiLine(true)
 ````

* <h4 id="LuaItemText_IsMultiLine">IsMultiLine</h4>
获取是否支持多行显示。

 > (`bool` bMultiline) ItemText:IsMultiLine()

 ````lua
 local bMultiline = ItemText:IsMultiLine()
 ````

* <h4 id="LuaItemText_FormatTextForDraw">FormatTextForDraw</h4>
格式化并重绘文本。当你修改了文本样式（如对齐方式、行距等）时，需要调用此 API 来立即应用样式。

 > (`void`) ItemText:FormatTextForDraw()

 ````lua
 ItemText:FormatTextForDraw()
 ````

* <h4 id="LuaItemText_AutoSize">AutoSize</h4>
根据内部文本自动设置自身宽高。

 > (`void`) ItemText:AutoSize()

 ````lua
 ItemText:AutoSize()
 ````

* <h4 id="LuaItemText_SetCenterEachLine">SetCenterEachLine</h4>
设置绘制时是否保持每一行居中。

 > (`void`) ItemText:SetCenterEachLine(`bool` bCenter)

 ````lua
 ItemText:SetCenterEachLine(true)
 ````

* <h4 id="LuaItemText_IsCenterEachLine">IsCenterEachLine</h4>
获取绘制时是否保持每一行居中。

 > (`bool` bCenter) ItemText:IsCenterEachLine()

 ````lua
 local bCenter = ItemText:IsCenterEachLine()
 ````

* <h4 id="LuaItemText_SetFontSpacing">SetFontSpacing</h4>
设置字符间距。

注意：内部会乘以 `Station.GetUIScale()`。

 > (`void`) ItemText:SetFontSpacing(`number` nSpacing)

 ````lua
 ItemText:SetFontSpacing(5)
 ````

* <h4 id="LuaItemText_GetFontSpacing">GetFontSpacing</h4>
获取字符间距。

注意：返回前内部会先除以 `Station.GetUIScale()`。

 > (`number` nSpacing) ItemText:GetFontSpacing()

 ````lua
 local nSpacing = ItemText:GetFontSpacing()
 ````

* <h4 id="LuaItemText_SetRichText">SetRichText</h4>
设置该 Text 是否支持富文本。

 > (`void`) ItemText:SetRichText(`bool` bRichText)

 ````lua
 ItemText:SetRichText(true)
 ````

* <h4 id="LuaItemText_IsRichText">IsRichText</h4>
获取该 Text 是否支持富文本。

 > (`number` nRichText) ItemText:IsRichText()

 ````lua
 local nRichText = ItemText:IsRichText() -- 0/1
 ````

* <h4 id="LuaItemText_GetFontScale">GetFontScale</h4>
获取缩放。

 > (`number` fScale) ItemText:GetFontScale()

 ````lua
 local fScale = ItemText:GetFontScale()
 ````

* <h4 id="LuaItemText_SetFontScale">SetFontScale</h4>
设置缩放。

注意：Text 控件无法使用 [`:Scale`](#LuaItemNull_Scale)，因为字体绘制方式与其他控件不同。

 > (`void`) ItemText:SetFontScale(`number` fScale)

 ````lua
 ItemText:SetFontScale(2.0)
 ````

* <h4 id="LuaItemText_SetFontID">SetFontID</h4>
设置字体 id。

 > (`void`) ItemText:SetFontID(`number` nFontID)

 ````lua
 ItemText:SetFontID(1)
 ````

* <h4 id="LuaItemText_SetFontColor">SetFontColor</h4>
设置字体颜色。

重载：

> * (`void`) ItemText:SetFontColor(`number` dwARGB)
> * (`void`) ItemText:SetFontColor(`string` szColorSchemeName)
> * (`void`) ItemText:SetFontColor(`number` nR, `number` nG, `number` nB)

 ````lua
 ItemText:SetFontColor(255, 255, 0)
 ItemText:SetFontColor(0xFFFF0000) -- ARGB
 ItemText:SetFontColor("WarningColor") -- from ColorScheme
 ````

* <h4 id="LuaItemText_SetFontBoder">SetFontBorder</h4>
设置字体描边。

 > (`void`) ItemText:SetFontBorder(`number` nBorderSize, `number` nR, `number` nG, `number` nB)

 ````lua
 ItemText:SetFontBorder(1, 255, 255, 0)
 ````

* <h4 id="LuaItemText_SetFontShadow">SetFontShadow</h4>
设置字体阴影。

 > (`void`) ItemText:SetFontShadow(`number` nShadowOffset, `number` nR, `number` nG, `number` nB)

 ````lua
 ItemText:SetFontShadow(1, 255, 255, 0)
 ````

* <h4 id="LuaItemText_GetFontID">GetFontID</h4>
获取字体 id。

 > (`number` nFontID) ItemText:GetFontID()

 ````lua
 local nFontID = ItemText:GetFontID()
 ````

* <h4 id="LuaItemText_GetFontColor">GetFontColor</h4>
获取字体颜色。

 > (`number` nR, `number` nG, `number` nB) ItemText:GetFontColor()

 ````lua
 local nR, nG, nB = ItemText:GetFontColor()
 ````

* <h4 id="LuaItemText_GetFontBoder">GetFontBoder</h4>
获取字体描边。

 > (`number` nBorderSize, `number` nR, `number` nG, `number` nB) ItemText:GetFontBoder()

 ````lua
 local nBorderSize, nR, nG, nB = ItemText:GetFontBoder()
 ````

* <h4 id="LuaItemText_GetFontProjection">GetFontProjection</h4>
获取字体阴影。（不确定为什么此 API 不命名为 `GetFontShadow`。）

 > (`number` nShadowOffset, `number` nR, `number` nG, `number` nB) ItemText:GetFontProjection()

 ````lua
 local nShadowOffset, nR, nG, nB = ItemText:GetFontProjection()
 ````

* <h4 id="LuaItemText_GetTextExtent">GetTextExtent</h4>
获取内部文本从偏移 0 到 `nOffset` 的宽高。

如果 `nOffset` 等于 -1，则返回全部文本的尺寸。

 > (`number` nW, `number` nH) ItemText:GetTextExtent([`number` nOffset])

 ````lua
 local nW, nH = ItemText:GetTextExtent() -- 获取全部文本尺寸
 local nW, nH = ItemText:GetTextExtent(3) -- 获取从偏移 0 到 3 的文本尺寸
 ````

* <h4 id="LuaItemText_GetTextPosExtent">GetTextPosExtent</h4>
获取给定 X 坐标位置对应的字符偏移。

如果省略 `nPosX`，则使用控件宽度。

 > (`number` nOffset) ItemText:GetTextPosExtent([`number` nPosX])

 ````lua
 local nCount = ItemText:GetTextPosExtent()     -- 获取全部文本的字符数
 local nOffset = ItemText:GetTextPosExtent(80)  -- 获取从偏移 0 到 80 像素范围内对应的字符偏移
 ````

* <h4 id="LuaItemText_IsTextAutoTipEnabled">IsTextAutoTipEnabled</h4>
获取是否启用了“文本被截断时自动提示”。

 > (`bool` bEnabled) ItemText:IsTextAutoTipEnabled()

 ````lua
 local bEnabled = ItemText:IsTextAutoTipEnabled()
 ````

* <h4 id="LuaItemText_SetTextAutoTipEnabled">SetTextAutoTipEnabled</h4>
启用/禁用“文本被截断时自动提示”。

重载：

> * (`void`) ItemText:SetTextAutoTipEnabled(`bool|number` bEnable)
> * (`void`) ItemText:SetTextAutoTipEnabled(`bool|number` bEnable, `bool|number` bFormatText)
> * (`void`) ItemText:SetTextAutoTipEnabled(`bool|number` bEnable, `bool|number` bFormatText, `bool|number` bClearMouseEnterEvent)

默认值：

- `bFormatText = true`
- `bClearMouseEnterEvent = false`（仅在禁用时有意义）

 ````lua
 ItemText:SetTextAutoTipEnabled(true)
 ItemText:SetTextAutoTipEnabled(true, true)
 ItemText:SetTextAutoTipEnabled(false, true, true)
 ````
