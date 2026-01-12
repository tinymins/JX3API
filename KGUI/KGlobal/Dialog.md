English | [中文](./Dialog.zh-CN.md)

# Dialog Functions

Functions for dialog and message operations.

## Functions

[`MessageBox`](#MessageBox)
[`PopupMenu`](#PopupMenu)
[`HidePopupMenu`](#HidePopupMenu)
[`Talk`](#Talk)
[`Say`](#Say)
[`SysMsg`](#SysMsg)
[`InfoTip`](#InfoTip)
[`TargetTip`](#TargetTip)

---

* <h4 id="MessageBox">MessageBox</h4>

Shows a message box dialog.

 > (`void`) MessageBox(`string` szMessage, `string` szTitle, `function` fnYes, `function` fnNo)

* <h4 id="PopupMenu">PopupMenu</h4>

Shows a popup menu.

 > (`void`) PopupMenu(`table` tMenu, `number` nX, `number` nY)

* <h4 id="HidePopupMenu">HidePopupMenu</h4>

Hides the current popup menu.

 > (`void`) HidePopupMenu()

* <h4 id="Talk">Talk</h4>

Sends a talk message in a channel.

 > (`void`) Talk(`number` nChannel, `string` szMessage)

* <h4 id="Say">Say</h4>

Sends a say message.

 > (`void`) Say(`string` szTarget, `string` szMessage)

* <h4 id="SysMsg">SysMsg</h4>

Shows a system message.

 > (`void`) SysMsg(`string` szMessage)

* <h4 id="InfoTip">InfoTip</h4>

Shows an info tip at cursor position.

 > (`void`) InfoTip(`string` szMessage, `number` nTime)

* <h4 id="TargetTip">TargetTip</h4>

Shows a target tip at cursor position.

 > (`void`) TargetTip(`string` szMessage)
