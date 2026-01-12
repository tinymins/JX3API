[English](./UI.md) | 中文

# UI 函数

UI 操作相关函数。

## Station 函数

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

## Wnd 函数

[`Wnd.ToggleWindow`](#Wnd_ToggleWindow)
[`Wnd.OpenWindow`](#Wnd_OpenWindow)
[`Wnd.CloseWindow`](#Wnd_CloseWindow)
[`Wnd.LookupWindow`](#Wnd_LookupWindow)
[`Wnd.KeepInClient`](#Wnd_KeepInClient)
[`Wnd.SetTipPosByRect`](#Wnd_SetTipPosByRect)
[`Wnd.SetTipPosByWnd`](#Wnd_SetTipPosByWnd)

## 光标函数

[`Cursor.GetPos`](#Cursor_GetPos)
[`Cursor.SetPos`](#Cursor_SetPos)
[`Cursor.Switch`](#Cursor_Switch)

## 工具函数

[`GetFormatText`](#GetFormatText)
[`GetFormatImage`](#GetFormatImage)
[`OutputMessage`](#OutputMessage)
[`OpenURL`](#OpenURL)
[`GetPureText`](#GetPureText)

---

* <h4 id="Station_Lookup">Station.Lookup</h4>

根据路径查找 UI 元素。

 > (`Wnd` wnd) Station.Lookup(`string` szPath, ...)

* <h4 id="Station_GetFocusWindow">Station.GetFocusWindow</h4>

获取当前获得焦点的窗口。

 > (`Wnd` wnd) Station.GetFocusWindow()

* <h4 id="Station_SetFocusWindow">Station.SetFocusWindow</h4>

设置窗口焦点。

 > (`void`) Station.SetFocusWindow(`Wnd` wnd)

* <h4 id="Station_GetMouseOverWindow">Station.GetMouseOverWindow</h4>

获取鼠标指针下的窗口。

 > (`Wnd` wnd) Station.GetMouseOverWindow()

* <h4 id="Station_GetMessageWindow">Station.GetMessageWindow</h4>

获取当前消息窗口。

 > (`Wnd` wnd) Station.GetMessageWindow()

* <h4 id="Station_SetMessageWindow">Station.SetMessageWindow</h4>

设置消息窗口。

 > (`void`) Station.SetMessageWindow(`Wnd` wnd)

* <h4 id="Station_GetClientSize">Station.GetClientSize</h4>

获取客户端窗口大小。

 > (`number` nWidth, `number` nHeight) Station.GetClientSize()

* <h4 id="Cursor_GetPos">Cursor.GetPos</h4>

获取当前光标位置。

 > (`number` nX, `number` nY) Cursor.GetPos()

* <h4 id="Cursor_SetPos">Cursor.SetPos</h4>

设置光标位置。

 > (`void`) Cursor.SetPos(`number` nX, `number` nY)

* <h4 id="Cursor_Switch">Cursor.Switch</h4>

切换光标类型。

 > (`void`) Cursor.Switch(`number` nType)

* <h4 id="GetFormatText">GetFormatText</h4>

创建用于 UI 显示的格式化文本。

 > (`string` szFormatText) GetFormatText(`string` szText, `number` nFont, `number` nR, `number` nG, `number` nB)

* <h4 id="GetFormatImage">GetFormatImage</h4>

创建用于 UI 显示的格式化图像。

 > (`string` szFormatImage) GetFormatImage(`string` szPath, `number` nFrame)

* <h4 id="OutputMessage">OutputMessage</h4>

向消息窗口输出消息。

 > (`void`) OutputMessage(`string` szChannel, `string` szMessage, `boolean` bTop)

* <h4 id="OpenURL">OpenURL</h4>

在网页浏览器中打开 URL。

 > (`void`) OpenURL(`string` szURL)

* <h4 id="GetPureText">GetPureText</h4>

从格式化文本中提取纯文本。

 > (`string` szText) GetPureText(`string` szFormatText)

---

## Station 详细方法

* <h4 id="Station_GetActiveFrame">Station.GetActiveFrame</h4>

获取当前活动窗口框架。

 > (`WndFrame` frame) Station.GetActiveFrame()

* <h4 id="Station_SetActiveFrame">Station.SetActiveFrame</h4>

设置活动窗口框架。

 > (`void`) Station.SetActiveFrame(`WndFrame` frame)

* <h4 id="Station_GetCapture">Station.GetCapture</h4>

获取捕获鼠标的窗口。

 > (`Wnd` wnd) Station.GetCapture()

* <h4 id="Station_SetCapture">Station.SetCapture</h4>

设置鼠标捕获窗口。

 > (`void`) Station.SetCapture(`Wnd` wnd)

* <h4 id="Station_ReleaseCapture">Station.ReleaseCapture</h4>

释放鼠标捕获。

 > (`void`) Station.ReleaseCapture()

* <h4 id="Station_GetClientPosition">Station.GetClientPosition</h4>

获取客户端窗口位置。

 > (`number` nX, `number` nY) Station.GetClientPosition()

* <h4 id="Station_GetWindowPosition">Station.GetWindowPosition</h4>

获取窗口位置。

 > (`number` nX, `number` nY) Station.GetWindowPosition()

* <h4 id="Station_SetUIScale">Station.SetUIScale</h4>

设置 UI 缩放比例。

 > (`void`) Station.SetUIScale(`number` fScale)

* <h4 id="Station_GetUIScale">Station.GetUIScale</h4>

获取当前 UI 缩放比例。

 > (`number` fScale) Station.GetUIScale()

* <h4 id="Station_GetMaxUIScale">Station.GetMaxUIScale</h4>

获取最大 UI 缩放比例。

 > (`number` fMaxScale) Station.GetMaxUIScale()

* <h4 id="Station_IsFullScreen">Station.IsFullScreen</h4>

检查是否为全屏模式。

 > (`boolean` bFullScreen) Station.IsFullScreen()

* <h4 id="Station_IsPanauision">Station.IsPanauision</h4>

检查是否为宽屏模式。

 > (`boolean` bPanauvision) Station.IsPanauision()

* <h4 id="Station_IsExclusiveMode">Station.IsExclusiveMode</h4>

检查是否为独占模式。

 > (`boolean` bExclusive) Station.IsExclusiveMode()

* <h4 id="Station_IsVisible">Station.IsVisible</h4>

检查 UI 是否可见。

 > (`boolean` bVisible) Station.IsVisible()

* <h4 id="Station_Show">Station.Show</h4>

显示 UI。

 > (`void`) Station.Show()

* <h4 id="Station_Hide">Station.Hide</h4>

隐藏 UI。

 > (`void`) Station.Hide()

* <h4 id="Station_GetIdleTime">Station.GetIdleTime</h4>

获取用户空闲时间（毫秒）。

 > (`number` nIdleTime) Station.GetIdleTime()

* <h4 id="Station_GetScreenPos">Station.GetScreenPos</h4>

获取屏幕位置。

 > (`number` nX, `number` nY) Station.GetScreenPos()

* <h4 id="Station_GetMessagePos">Station.GetMessagePos</h4>

获取当前消息的鼠标位置。

 > (`number` nX, `number` nY) Station.GetMessagePos()

* <h4 id="Station_GetMessageWheelDelta">Station.GetMessageWheelDelta</h4>

获取鼠标滚轮增量。

 > (`number` nDelta) Station.GetMessageWheelDelta()

* <h4 id="Station_GetMessageKey">Station.GetMessageKey</h4>

获取当前消息的按键。

 > (`number` nKey) Station.GetMessageKey()

* <h4 id="Station_ToggleWindow">Station.ToggleWindow</h4>

切换窗口显示状态。

 > (`WndFrame` frame) Station.ToggleWindow(`string` szPath)

* <h4 id="Station_OpenWindow">Station.OpenWindow</h4>

打开窗口。

 > (`WndFrame` frame) Station.OpenWindow(`string` szPath, `string` szName)

* <h4 id="Station_CloseWindow">Station.CloseWindow</h4>

关闭窗口。

 > (`void`) Station.CloseWindow(`WndFrame` frame)

* <h4 id="Station_OriginalToAdjustPos">Station.OriginalToAdjustPos</h4>

将原始坐标转换为调整后的坐标。

 > (`number` nAdjustedX, `number` nAdjustedY) Station.OriginalToAdjustPos(`number` nOrigX, `number` nOrigY)

* <h4 id="Station_AdjustToOriginalPos">Station.AdjustToOriginalPos</h4>

将调整后的坐标转换为原始坐标。

 > (`number` nOrigX, `number` nOrigY) Station.AdjustToOriginalPos(`number` nAdjustedX, `number` nAdjustedY)

* <h4 id="Station_GetAllFrame">Station.GetAllFrame</h4>

获取所有窗口框架列表。

 > (`table` tFrameList) Station.GetAllFrame()

* <h4 id="Station_GetStandardClientSize">Station.GetStandardClientSize</h4>

获取标准客户端大小。

 > (`number` nWidth, `number` nHeight) Station.GetStandardClientSize()

---

## Wnd 详细方法

* <h4 id="Wnd_ToggleWindow">Wnd.ToggleWindow</h4>

切换窗口显示状态。

 > (`WndFrame` frame) Wnd.ToggleWindow(`string` szPath)

* <h4 id="Wnd_OpenWindow">Wnd.OpenWindow</h4>

打开窗口。

 > (`WndFrame` frame) Wnd.OpenWindow(`string` szPath, `string` szName)

* <h4 id="Wnd_CloseWindow">Wnd.CloseWindow</h4>

关闭窗口。

 > (`void`) Wnd.CloseWindow(`WndFrame` frame)

* <h4 id="Wnd_LookupWindow">Wnd.LookupWindow</h4>

根据名称查找窗口。

 > (`Wnd` wnd) Wnd.LookupWindow(`string` szName)

* <h4 id="Wnd_KeepInClient">Wnd.KeepInClient</h4>

确保窗口保持在客户端区域内。

 > (`void`) Wnd.KeepInClient(`WndFrame` frame)

* <h4 id="Wnd_SetTipPosByRect">Wnd.SetTipPosByRect</h4>

根据矩形区域设置提示框位置。

 > (`void`) Wnd.SetTipPosByRect(`number` nX, `number` nY, `number` nW, `number` nH)

* <h4 id="Wnd_SetTipPosByWnd">Wnd.SetTipPosByWnd</h4>

根据窗口设置提示框位置。

 > (`void`) Wnd.SetTipPosByWnd(`Wnd` wnd)
