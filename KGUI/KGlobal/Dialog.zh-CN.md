[English](./Dialog.md) | 中文

# 对话框函数

对话框和消息操作相关函数。

## 函数

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

显示消息框对话框。

 > (`void`) MessageBox(`string` szMessage, `string` szTitle, `function` fnYes, `function` fnNo)

* <h4 id="PopupMenu">PopupMenu</h4>

显示弹出菜单。

 > (`void`) PopupMenu(`table` tMenu, `number` nX, `number` nY)

* <h4 id="HidePopupMenu">HidePopupMenu</h4>

隐藏当前弹出菜单。

 > (`void`) HidePopupMenu()

* <h4 id="Talk">Talk</h4>

在频道中发送聊天消息。

 > (`void`) Talk(`number` nChannel, `string` szMessage)

* <h4 id="Say">Say</h4>

发送密语消息。

 > (`void`) Say(`string` szTarget, `string` szMessage)

* <h4 id="SysMsg">SysMsg</h4>

显示系统消息。

 > (`void`) SysMsg(`string` szMessage)

* <h4 id="InfoTip">InfoTip</h4>

在光标位置显示信息提示。

 > (`void`) InfoTip(`string` szMessage, `number` nTime)

* <h4 id="TargetTip">TargetTip</h4>

在光标位置显示目标提示。

 > (`void`) TargetTip(`string` szMessage)
