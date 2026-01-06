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
Set text font scheme.<br>
This api will load `pFontScheme` by `nFontID`, and then call this:<br>
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
Get text font scheme.

 > (`number` nFont) ItemText:GetFontScheme()

 ````lua
 local nFont = ItemText:GetFontScheme()
 ````

* <h4 id="LuaItemText_SetRange">SetRange</h4>
Set text as range format. Notice that this api is the same as [`:SetText(nValue1 .. szDelimiter .. nVlaue2)`](#LuaItemText_SetText). But this api is high performanced than `:SetText` cause there is no intermediate string when concat string.
> * (`void`) ItemText:SetRange(`number` nValue, `string` szDelimiter)
> * (`void`) ItemText:SetRange(`number` nValue1, `string` szDelimiter, `number` nValue2)

 ````lua
 ItemText:SetRange(5, "%")
 ItemText:SetRange(5, "/", 100)
 ````

* <h4 id="LuaItemText_SetTime">SetTime</h4>
Set text as time format. Notice that this api is the same as [`:SetText(("%02d:%02d:%02d"):format(TimeToHMS(nTime)))`](#LuaItemText_SetText). But this api is high performanced than `:SetText` cause there is no intermediate string when concat string.

 > (`void`) ItemText:SetTime(`number` nTimeStamp)

 ````lua
 ItemText:SetTime(GetCurrentTime())
 ````

* <h4 id="LuaItemText_SetNumber">SetNumber</h4>
Set text as pure number. Notice that this api is the same as [`:SetText(tostring(nNumber))`](#LuaItemText_SetText). But this api is high performanced than `:SetText` cause there is no intermediate string when concat string.

 > (`void`) ItemText:SetNumber(`number` nNumber)

 ````lua
 ItemText:SetNumber(213928)
 ````

* <h4 id="LuaItemText_GetNumber">GetNumber</h4>
Parse current text as a number.

This uses a simple scan (`%lf`). If the text is not a valid number, it returns `0`.

 > (`number` nNumber) ItemText:GetNumber()

 ````lua
 local nNumber = ItemText:GetNumber()
 ````

* <h4 id="LuaItemText_SetText">SetText</h4>
Set display text.

 > (`void`) ItemText:SetText(`string` szText[, `bool` bKey])

If `bKey` is `true`, `szText` is treated as a **global string key**, and the real text will be loaded from the global string table.

 ````lua
 ItemText:SetText("This is a text.")
 ItemText:SetText("UI_TEXT_KEY", true)
 ````

* <h4 id="LuaItemText_SprintfText">SprintfText</h4>
Format and set text using a printf-like format string.

Supported conversion specifiers:

- `%s` (string)
- `%d` (integer), `%x`/`%X` (hex)
- `%f` (number)
- `%%` (literal `%`)

The format string can contain width/precision parts (digits and `.`) between `%` and the specifier.

 > (`void`) ItemText:SprintfText(`string` szFormat, ...)

 ````lua
 ItemText:SprintfText("%d/%d", 5, 100)
 ItemText:SprintfText("HP:%d%%", 80)
 ItemText:SprintfText("Name:%s  Score:%.2f", "Bob", 98.25)
 ````

* <h4 id="LuaItemText_GetText">GetText</h4>
Get display text.

 > (`string` szText) ItemText:GetText()

 ````lua
 local szText = ItemText:GetText()
 ````

* <h4 id="LuaItemText_GetTextLen">GetTextLen</h4>
Get the length of display text.

 > (`number` nLen) ItemText:GetTextLen()

 ````lua
 local nLen = ItemText:GetTextLen()
 ````

* <h4 id="LuaItemText_SetVAlign">SetVAlign</h4>
Set text vertical alignment. Enum: `0-top`, `1-center`, `2-bottom`. Notice that you may need to call [`:FormatTextForDraw()`](#LuaItemText_FormatTextForDraw) for apply the change and redraw text immediately.

 > (`void`) ItemText:SetVAlign(`number` nAlign)

 ````lua
 ItemText:SetVAlign(1)
 ````

* <h4 id="LuaItemText_GetVAlign">GetVAlign</h4>
Get text vertical alignment.

 > (`number` nAlign) ItemText:GetVAlign()

 ````lua
 local nAlign = ItemText:GetVAlign()
 ````

* <h4 id="LuaItemText_SetHAlign">SetHAlign</h4>
Set text horizontal alignment. Enum: `0-left`, `1-middle`, `2-right`. Notice that you may need to call [`:FormatTextForDraw()`](#LuaItemText_FormatTextForDraw) for apply the change and redraw text immediately.

 > (`void`) ItemText:SetHAlign(`number` nAlign)

 ````lua
 ItemText:SetHAlign(1)
 ````

* <h4 id="LuaItemText_GetHAlign">GetHAlign</h4>
Get text horizontal alignment.

 > (`number` nAlign) ItemText:GetHAlign()

 ````lua
 local nAlign = ItemText:GetHAlign()
 ````

* <h4 id="LuaItemText_SetRowSpacing">SetRowSpacing</h4>
Set the spacing of two rows.

Note: internally it is multiplied by `Station.GetUIScale()`.

 > (`void`) ItemText:SetRowSpacing(`number` nSpacing)

 ````lua
 ItemText:SetRowSpacing(3)
 ````

* <h4 id="LuaItemText_GetRowSpacing">GetRowSpacing</h4>
Get the spacing of two rows.

Note: internally it is divided by `Station.GetUIScale()` before returning.

 > (`number` nSpacing) ItemText:GetRowSpacing()

 ````lua
 local nSpacing = ItemText:GetRowSpacing()
 ````

* <h4 id="LuaItemText_SetMultiLine">SetMultiLine</h4>
Set if this text control supports multiline display. Support multiline display means that when the width of the inner text reaches the width of the control, it will auto wrap.

 > (`void`) ItemText:SetMultiLine(`bool` bMultiline)

 ````lua
 ItemText:SetMultiLine(true)
 ````

* <h4 id="LuaItemText_IsMultiLine">IsMultiLine</h4>
Get if it supports multiline.

 > (`bool` bMultiline) ItemText:IsMultiLine()

 ````lua
 local bMultiline = ItemText:IsMultiLine()
 ````

* <h4 id="LuaItemText_FormatTextForDraw">FormatTextForDraw</h4>
Format and redraw the text. When you change the style of text (such as alignment and row spacing), you need to call this api to apply style immediately.

 > (`void`) ItemText:FormatTextForDraw()

 ````lua
 ItemText:FormatTextForDraw()
 ````

* <h4 id="LuaItemText_AutoSize">AutoSize</h4>
Auto set its width and height by its inner text.

 > (`void`) ItemText:AutoSize()

 ````lua
 ItemText:AutoSize()
 ````

* <h4 id="LuaItemText_SetCenterEachLine">SetCenterEachLine</h4>
Set whether to keep center of each line in this text while drawing.

 > (`void`) ItemText:SetCenterEachLine(`bool` bCenter)

 ````lua
 ItemText:SetCenterEachLine(true)
 ````

* <h4 id="LuaItemText_IsCenterEachLine">IsCenterEachLine</h4>
Get whether to keep center of each line in this text while drawing.

 > (`bool` bCenter) ItemText:IsCenterEachLine()

 ````lua
 local bCenter = ItemText:IsCenterEachLine()
 ````

* <h4 id="LuaItemText_SetFontSpacing">SetFontSpacing</h4>
Set the spacing between two characters.

Note: internally it is multiplied by `Station.GetUIScale()`.

 > (`void`) ItemText:SetFontSpacing(`number` nSpacing)

 ````lua
 ItemText:SetFontSpacing(5)
 ````

* <h4 id="LuaItemText_GetFontSpacing">GetFontSpacing</h4>
Get the spacing between two characters.

Note: internally it is divided by `Station.GetUIScale()` before returning.

 > (`number` nSpacing) ItemText:GetFontSpacing()

 ````lua
 local nSpacing = ItemText:GetFontSpacing()
 ````

* <h4 id="LuaItemText_SetRichText">SetRichText</h4>
Set whether this Text supports rich text.

 > (`void`) ItemText:SetRichText(`bool` bRichText)

 ````lua
 ItemText:SetRichText(true)
 ````

* <h4 id="LuaItemText_IsRichText">IsRichText</h4>
Get whether this Text supports rich text.

 > (`number` nRichText) ItemText:IsRichText()

 ````lua
 local nRichText = ItemText:IsRichText() -- 0/1
 ````

* <h4 id="LuaItemText_GetFontScale">GetFontScale</h4>
Get scale.

 > (`number` fScale) ItemText:GetFontScale()

 ````lua
 local fScale = ItemText:GetFontScale()
 ````

* <h4 id="LuaItemText_SetFontScale">SetFontScale</h4>
Set scale. Notice that [`:Scale`](#LuaItemNull_Scale) is unavailable on Text control because drawing font is in a different way with drawing other controls.

 > (`void`) ItemText:SetFontScale(`number` fScale)

 ````lua
 ItemText:SetFontScale(2.0)
 ````

* <h4 id="LuaItemText_SetFontID">SetFontID</h4>
Set font id.

 > (`void`) ItemText:SetFontID(`number` nFontID)

 ````lua
 ItemText:SetFontID(1)
 ````

* <h4 id="LuaItemText_SetFontColor">SetFontColor</h4>
Set font color.

Overloads:

> * (`void`) ItemText:SetFontColor(`number` dwARGB)
> * (`void`) ItemText:SetFontColor(`string` szColorSchemeName)
> * (`void`) ItemText:SetFontColor(`number` nR, `number` nG, `number` nB)

 ````lua
 ItemText:SetFontColor(255, 255, 0)
 ItemText:SetFontColor(0xFFFF0000) -- ARGB
 ItemText:SetFontColor("WarningColor") -- from ColorScheme
 ````

* <h4 id="LuaItemText_SetFontBoder">SetFontBorder</h4>
Set font border.

 > (`void`) ItemText:SetFontBorder(`number` nBorderSize, `number` nR, `number` nG, `number` nB)

 ````lua
 ItemText:SetFontBorder(1, 255, 255, 0)
 ````

* <h4 id="LuaItemText_SetFontShadow">SetFontShadow</h4>
Set font shadow.

 > (`void`) ItemText:SetFontShadow(`number` nShadowOffset, `number` nR, `number` nG, `number` nB)

 ````lua
 ItemText:SetFontShadow(1, 255, 255, 0)
 ````

* <h4 id="LuaItemText_GetFontID">GetFontID</h4>
Get font id.

 > (`number` nFontID) ItemText:GetFontID()

 ````lua
 local nFontID = ItemText:GetFontID()
 ````

* <h4 id="LuaItemText_GetFontColor">GetFontColor</h4>
Get font color.

 > (`number` nR, `number` nG, `number` nB) ItemText:GetFontColor()

 ````lua
 local nR, nG, nB = ItemText:GetFontColor()
 ````

* <h4 id="LuaItemText_GetFontBoder">GetFontBoder</h4>
Get font border.

 > (`number` nBorderSize, `number` nR, `number` nG, `number` nB) ItemText:GetFontBoder()

 ````lua
 local nBorderSize, nR, nG, nB = ItemText:GetFontBoder()
 ````

* <h4 id="LuaItemText_GetFontProjection">GetFontProjection</h4>
Get font shadow. (I don't know why this api is not named as `GetFontShadow`).

 > (`number` nShadowOffset, `number` nR, `number` nG, `number` nB) ItemText:GetFontProjection()

 ````lua
 local nShadowOffset, nR, nG, nB = ItemText:GetFontProjection()
 ````

* <h4 id="LuaItemText_GetTextExtent">GetTextExtent</h4>
Get the width and height of the inner text from offset 0 to `nOffset`. If `nOffset` equals with -1, the size of all text will be returned.

 > (`number` nW, `number` nH) ItemText:GetTextExtent([`number` nOffset])

 ````lua
 local nW, nH = ItemText:GetTextExtent() -- Get all text size
 local nW, nH = ItemText:GetTextExtent(3) -- Get text size from offset zero to three
 ````

* <h4 id="LuaItemText_GetTextPosExtent">GetTextPosExtent</h4>
Get the character offset at a given X position.

If `nPosX` is omitted, it uses the control width.

 > (`number` nOffset) ItemText:GetTextPosExtent([`number` nPosX])

 ````lua
 local nCount = ItemText:GetTextPosExtent()     -- Get the count of all of the text.
 local nOffset = ItemText:GetTextPosExtent(80)  -- Get the count of the text from offset zero to offset 80 pixels.
 ````

* <h4 id="LuaItemText_IsTextAutoTipEnabled">IsTextAutoTipEnabled</h4>
Get whether auto-tip for truncated text is enabled.

 > (`bool` bEnabled) ItemText:IsTextAutoTipEnabled()

 ````lua
 local bEnabled = ItemText:IsTextAutoTipEnabled()
 ````

* <h4 id="LuaItemText_SetTextAutoTipEnabled">SetTextAutoTipEnabled</h4>
Enable/disable auto-tip for truncated text.

Overloads:

> * (`void`) ItemText:SetTextAutoTipEnabled(`bool|number` bEnable)
> * (`void`) ItemText:SetTextAutoTipEnabled(`bool|number` bEnable, `bool|number` bFormatText)
> * (`void`) ItemText:SetTextAutoTipEnabled(`bool|number` bEnable, `bool|number` bFormatText, `bool|number` bClearMouseEnterEvent)

Defaults:

- `bFormatText = true`
- `bClearMouseEnterEvent = false` (only useful when disabling)

 ````lua
 ItemText:SetTextAutoTipEnabled(true)
 ItemText:SetTextAutoTipEnabled(true, true)
 ItemText:SetTextAutoTipEnabled(false, true, true)
 ````
