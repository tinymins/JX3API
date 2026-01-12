English | [中文](./UI.zh-CN.md)

# UI Functions

Functions for UI operations.

## Station Functions

[`Station.Lookup`](#Station_Lookup)
[`Station.GetFocusWindow`](#Station_GetFocusWindow)
[`Station.SetFocusWindow`](#Station_SetFocusWindow)
[`Station.GetActiveFrame`](#Station_GetActiveFrame)
[`Station.SetActiveFrame`](#Station_SetActiveFrame)
[`Station.GetMouseOverWindow`](#Station_GetMouseOverWindow)
[`Station.GetCapture`](#Station_GetCapture)
[`Station.SetCapture`](#Station_SetCapture)
[`Station.ReleaseCapture`](#Station_ReleaseCapture)
[`Station.GetClientSize`](#Station_GetClientSize)
[`Station.GetClientPosition`](#Station_GetClientPosition)
[`Station.GetWindowPosition`](#Station_GetWindowPosition)
[`Station.SetUIScale`](#Station_SetUIScale)
[`Station.GetUIScale`](#Station_GetUIScale)
[`Station.GetMaxUIScale`](#Station_GetMaxUIScale)
[`Station.IsFullScreen`](#Station_IsFullScreen)
[`Station.IsPanauision`](#Station_IsPanauision)
[`Station.IsExclusiveMode`](#Station_IsExclusiveMode)
[`Station.IsVisible`](#Station_IsVisible)
[`Station.Show`](#Station_Show)
[`Station.Hide`](#Station_Hide)
[`Station.GetIdleTime`](#Station_GetIdleTime)
[`Station.GetScreenPos`](#Station_GetScreenPos)
[`Station.GetMessagePos`](#Station_GetMessagePos)
[`Station.GetMessageWheelDelta`](#Station_GetMessageWheelDelta)
[`Station.GetMessageKey`](#Station_GetMessageKey)
[`Station.ToggleWindow`](#Station_ToggleWindow)
[`Station.OpenWindow`](#Station_OpenWindow)
[`Station.CloseWindow`](#Station_CloseWindow)
[`Station.OriginalToAdjustPos`](#Station_OriginalToAdjustPos)
[`Station.AdjustToOriginalPos`](#Station_AdjustToOriginalPos)
[`Station.GetAllFrame`](#Station_GetAllFrame)
[`Station.GetStandardClientSize`](#Station_GetStandardClientSize)

## Wnd Functions

[`Wnd.ToggleWindow`](#Wnd_ToggleWindow)
[`Wnd.OpenWindow`](#Wnd_OpenWindow)
[`Wnd.CloseWindow`](#Wnd_CloseWindow)
[`Wnd.LookupWindow`](#Wnd_LookupWindow)
[`Wnd.KeepInClient`](#Wnd_KeepInClient)
[`Wnd.SetTipPosByRect`](#Wnd_SetTipPosByRect)
[`Wnd.SetTipPosByWnd`](#Wnd_SetTipPosByWnd)

## Cursor Functions

[`Cursor.GetPos`](#Cursor_GetPos)
[`Cursor.SetPos`](#Cursor_SetPos)
[`Cursor.Switch`](#Cursor_Switch)

## Utility Functions

[`GetFormatText`](#GetFormatText)
[`GetFormatImage`](#GetFormatImage)
[`OutputMessage`](#OutputMessage)
[`OpenURL`](#OpenURL)
[`GetPureText`](#GetPureText)

---

* <h4 id="Station_Lookup">Station.Lookup</h4>

Looks up a UI element by path.

 > (`Wnd` wnd) Station.Lookup(`string` szPath, ...)

* <h4 id="Station_GetFocusWindow">Station.GetFocusWindow</h4>

Gets the currently focused window.

 > (`Wnd` wnd) Station.GetFocusWindow()

* <h4 id="Station_SetFocusWindow">Station.SetFocusWindow</h4>

Sets the focus to a window.

 > (`void`) Station.SetFocusWindow(`Wnd` wnd)

* <h4 id="Station_GetMouseOverWindow">Station.GetMouseOverWindow</h4>

Gets the window under the mouse cursor.

 > (`Wnd` wnd) Station.GetMouseOverWindow()

* <h4 id="Station_GetMessageWindow">Station.GetMessageWindow</h4>

Gets the current message window.

 > (`Wnd` wnd) Station.GetMessageWindow()

* <h4 id="Station_SetMessageWindow">Station.SetMessageWindow</h4>

Sets the message window.

 > (`void`) Station.SetMessageWindow(`Wnd` wnd)

* <h4 id="Station_GetClientSize">Station.GetClientSize</h4>

Gets the client window size.

 > (`number` nWidth, `number` nHeight) Station.GetClientSize()

* <h4 id="Cursor_GetPos">Cursor.GetPos</h4>

Gets the current cursor position.

 > (`number` nX, `number` nY) Cursor.GetPos()

* <h4 id="Cursor_SetPos">Cursor.SetPos</h4>

Sets the cursor position.

 > (`void`) Cursor.SetPos(`number` nX, `number` nY)

* <h4 id="Cursor_Switch">Cursor.Switch</h4>

Switches the cursor type.

 > (`void`) Cursor.Switch(`number` nType)

* <h4 id="GetFormatText">GetFormatText</h4>

Creates formatted text for UI display.

 > (`string` szFormatText) GetFormatText(`string` szText, `number` nFont, `number` nR, `number` nG, `number` nB)

* <h4 id="GetFormatImage">GetFormatImage</h4>

Creates formatted image for UI display.

 > (`string` szFormatImage) GetFormatImage(`string` szPath, `number` nFrame)

* <h4 id="OutputMessage">OutputMessage</h4>

Outputs a message to the message window.

 > (`void`) OutputMessage(`string` szChannel, `string` szMessage, `boolean` bTop)

* <h4 id="OpenURL">OpenURL</h4>

Opens a URL in the web browser.

 > (`void`) OpenURL(`string` szURL)

* <h4 id="GetPureText">GetPureText</h4>

Extracts pure text from formatted text.

 > (`string` szText) GetPureText(`string` szFormatText)

---

## Station Detailed Methods

* <h4 id="Station_GetActiveFrame">Station.GetActiveFrame</h4>

Gets the currently active window frame.

 > (`WndFrame` frame) Station.GetActiveFrame()

* <h4 id="Station_SetActiveFrame">Station.SetActiveFrame</h4>

Sets the active window frame.

 > (`void`) Station.SetActiveFrame(`WndFrame` frame)

* <h4 id="Station_GetCapture">Station.GetCapture</h4>

Gets the window that has captured the mouse.

 > (`Wnd` wnd) Station.GetCapture()

* <h4 id="Station_SetCapture">Station.SetCapture</h4>

Sets the mouse capture window.

 > (`void`) Station.SetCapture(`Wnd` wnd)

* <h4 id="Station_ReleaseCapture">Station.ReleaseCapture</h4>

Releases the mouse capture.

 > (`void`) Station.ReleaseCapture()

* <h4 id="Station_GetClientPosition">Station.GetClientPosition</h4>

Gets the client window position.

 > (`number` nX, `number` nY) Station.GetClientPosition()

* <h4 id="Station_GetWindowPosition">Station.GetWindowPosition</h4>

Gets the window position.

 > (`number` nX, `number` nY) Station.GetWindowPosition()

* <h4 id="Station_SetUIScale">Station.SetUIScale</h4>

Sets the UI scale ratio.

 > (`void`) Station.SetUIScale(`number` fScale)

* <h4 id="Station_GetUIScale">Station.GetUIScale</h4>

Gets the current UI scale ratio.

 > (`number` fScale) Station.GetUIScale()

* <h4 id="Station_GetMaxUIScale">Station.GetMaxUIScale</h4>

Gets the maximum UI scale ratio.

 > (`number` fMaxScale) Station.GetMaxUIScale()

* <h4 id="Station_IsFullScreen">Station.IsFullScreen</h4>

Checks if in fullscreen mode.

 > (`boolean` bFullScreen) Station.IsFullScreen()

* <h4 id="Station_IsPanauision">Station.IsPanauision</h4>

Checks if in widescreen mode.

 > (`boolean` bPanauvision) Station.IsPanauision()

* <h4 id="Station_IsExclusiveMode">Station.IsExclusiveMode</h4>

Checks if in exclusive mode.

 > (`boolean` bExclusive) Station.IsExclusiveMode()

* <h4 id="Station_IsVisible">Station.IsVisible</h4>

Checks if UI is visible.

 > (`boolean` bVisible) Station.IsVisible()

* <h4 id="Station_Show">Station.Show</h4>

Shows the UI.

 > (`void`) Station.Show()

* <h4 id="Station_Hide">Station.Hide</h4>

Hides the UI.

 > (`void`) Station.Hide()

* <h4 id="Station_GetIdleTime">Station.GetIdleTime</h4>

Gets user idle time in milliseconds.

 > (`number` nIdleTime) Station.GetIdleTime()

* <h4 id="Station_GetScreenPos">Station.GetScreenPos</h4>

Gets the screen position.

 > (`number` nX, `number` nY) Station.GetScreenPos()

* <h4 id="Station_GetMessagePos">Station.GetMessagePos</h4>

Gets the mouse position for current message.

 > (`number` nX, `number` nY) Station.GetMessagePos()

* <h4 id="Station_GetMessageWheelDelta">Station.GetMessageWheelDelta</h4>

Gets the mouse wheel delta.

 > (`number` nDelta) Station.GetMessageWheelDelta()

* <h4 id="Station_GetMessageKey">Station.GetMessageKey</h4>

Gets the key for current message.

 > (`number` nKey) Station.GetMessageKey()

* <h4 id="Station_ToggleWindow">Station.ToggleWindow</h4>

Toggles window visibility.

 > (`WndFrame` frame) Station.ToggleWindow(`string` szPath)

* <h4 id="Station_OpenWindow">Station.OpenWindow</h4>

Opens a window.

 > (`WndFrame` frame) Station.OpenWindow(`string` szPath, `string` szName)

* <h4 id="Station_CloseWindow">Station.CloseWindow</h4>

Closes a window.

 > (`void`) Station.CloseWindow(`WndFrame` frame)

* <h4 id="Station_OriginalToAdjustPos">Station.OriginalToAdjustPos</h4>

Converts original coordinates to adjusted coordinates.

 > (`number` nAdjustedX, `number` nAdjustedY) Station.OriginalToAdjustPos(`number` nOrigX, `number` nOrigY)

* <h4 id="Station_AdjustToOriginalPos">Station.AdjustToOriginalPos</h4>

Converts adjusted coordinates to original coordinates.

 > (`number` nOrigX, `number` nOrigY) Station.AdjustToOriginalPos(`number` nAdjustedX, `number` nAdjustedY)

* <h4 id="Station_GetAllFrame">Station.GetAllFrame</h4>

Gets list of all window frames.

 > (`table` tFrameList) Station.GetAllFrame()

* <h4 id="Station_GetStandardClientSize">Station.GetStandardClientSize</h4>

Gets the standard client size.

 > (`number` nWidth, `number` nHeight) Station.GetStandardClientSize()

---

## Wnd Detailed Methods

* <h4 id="Wnd_ToggleWindow">Wnd.ToggleWindow</h4>

Toggles window visibility.

 > (`WndFrame` frame) Wnd.ToggleWindow(`string` szPath)

* <h4 id="Wnd_OpenWindow">Wnd.OpenWindow</h4>

Opens a window.

 > (`WndFrame` frame) Wnd.OpenWindow(`string` szPath, `string` szName)

* <h4 id="Wnd_CloseWindow">Wnd.CloseWindow</h4>

Closes a window.

 > (`void`) Wnd.CloseWindow(`WndFrame` frame)

* <h4 id="Wnd_LookupWindow">Wnd.LookupWindow</h4>

Looks up a window by name.

 > (`Wnd` wnd) Wnd.LookupWindow(`string` szName)

* <h4 id="Wnd_KeepInClient">Wnd.KeepInClient</h4>

Keeps window within client area.

 > (`void`) Wnd.KeepInClient(`WndFrame` frame)

* <h4 id="Wnd_SetTipPosByRect">Wnd.SetTipPosByRect</h4>

Sets tooltip position by rectangle.

 > (`void`) Wnd.SetTipPosByRect(`number` nX, `number` nY, `number` nW, `number` nH)

* <h4 id="Wnd_SetTipPosByWnd">Wnd.SetTipPosByWnd</h4>

Sets tooltip position by window.

 > (`void`) Wnd.SetTipPosByWnd(`Wnd` wnd)
