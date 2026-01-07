[English](./ItemNull.md) | 中文

# ItemNull

说明：

- 对于位置/尺寸相关 API：Lua 侧使用**未缩放的 UI 坐标**。内部会把输入乘以 `Station.GetUIScale()`；对应的 Get* 会在返回前除以 UIScale。

[`SetVisible`](#LuaItemNull_SetVisible)
[`Show`](#LuaItemNull_Show)
[`Hide`](#LuaItemNull_Hide)
[`PtInItem`](#LuaItemNull_PtInItem)
[`IsMouseIn`](#LuaItemNull_IsMouseIn)
[`SetMouseButtonStatusElement`](#LuaItemNull_SetMouseButtonStatusElement)
[`ClearMouseButtonStatusElement`](#LuaItemNull_ClearMouseButtonStatusElement)
[`SetHoverElement`](#LuaItemNull_SetHoverElement)
[`ClearHoverElement`](#LuaItemNull_ClearHoverElement)
[`SetRelX`](#LuaItemNull_SetRelX)
[`SetRelY`](#LuaItemNull_SetRelY)
[`GetRelX`](#LuaItemNull_GetRelX)
[`GetRelY`](#LuaItemNull_GetRelY)
[`SetAbsX`](#LuaItemNull_SetAbsX)
[`SetAbsY`](#LuaItemNull_SetAbsY)
[`GetAbsX`](#LuaItemNull_GetAbsX)
[`GetAbsY`](#LuaItemNull_GetAbsY)
[`SetW`](#LuaItemNull_SetW)
[`SetH`](#LuaItemNull_SetH)
[`GetW`](#LuaItemNull_GetW)
[`GetH`](#LuaItemNull_GetH)
[`SetRelPos`](#LuaItemNull_SetRelPos)
[`GetRelPos`](#LuaItemNull_GetRelPos)
[`SetAbsPos`](#LuaItemNull_SetAbsPos)
[`GetAbsPos`](#LuaItemNull_GetAbsPos)
[`SetSize`](#LuaItemNull_SetSize)
[`GetSize`](#LuaItemNull_GetSize)
[`SetPosType`](#LuaItemNull_SetPosType)
[`GetPosType`](#LuaItemNull_GetPosType)
[`IsVisible`](#LuaItemNull_IsVisible)
[`GetName`](#LuaItemNull_GetName)
[`SetName`](#LuaItemNull_SetName)
[`SetTip`](#LuaItemNull_SetTip)
[`GetTip`](#LuaItemNull_GetTip)
[`SetUserData`](#LuaItemNull_SetUserData)
[`GetUserData`](#LuaItemNull_GetUserData)
[`RegisterEvent`](#LuaItemNull_RegisterEvent)
[`ClearEvent`](#LuaItemNull_ClearEvent)
[`EnableScale`](#LuaItemNull_EnableScale)
[`Scale`](#LuaItemNull_Scale)
[`LockShowAndHide`](#LuaItemNull_LockShowAndHide)
[`SetAlpha`](#LuaItemNull_SetAlpha)
[`GetAlpha`](#LuaItemNull_GetAlpha)
[`GetParent`](#LuaItemNull_GetParent)
[`GetRoot`](#LuaItemNull_GetRoot)
[`GetType`](#LuaItemNull_GetType)
[`GetIndex`](#LuaItemNull_GetIndex)
[`SetIndex`](#LuaItemNull_SetIndex)
[`ExchangeIndex`](#LuaItemNull_ExchangeIndex)
[`GetTreePath`](#LuaItemNull_GetTreePath)
[`SetAreaTestFile`](#LuaItemNull_SetAreaTestFile)
[`SetIntPos`](#LuaItemNull_SetIntPos)
[`IsIntPos`](#LuaItemNull_IsIntPos)
[`IsLink`](#LuaItemNull_IsLink)
[`GetLinkInfo`](#LuaItemNull_GetLinkInfo)
[`SetLinkInfo`](#LuaItemNull_SetLinkInfo)
[`SetTweenAni`](#LuaItemNull_SetTweenAni)
[`GetTweenFile`](#LuaItemNull_GetTweenFile)
[`SetTweenFile`](#LuaItemNull_SetTweenFile)
[`GetTweenName`](#LuaItemNull_GetTweenName)
[`SetTweenName`](#LuaItemNull_SetTweenName)
[`GetAniParamID`](#LuaItemNull_GetAniParamID)
[`SetPoint`](#LuaItemNull_SetPoint)
[`SetBasicStatus`](#LuaItemNull_SetBasicStatus)
[`ToGray`](#LuaItemNull_ToGray)
[`ToNormal`](#LuaItemNull_ToNormal)
[`IsGray`](#LuaItemNull_IsGray)
[`Lookup`](#LuaItemNull_Lookup)
[`IsValid`](#LuaItemNull_IsValid)
[`__newindex`](#LuaItemNull_NewIndex)
[`__eq`](#LuaItemNull_Equal)
[`GetBaseType`](#LuaItemNull_GetBaseType)

* <h4 id="LuaItemNull_SetVisible">SetVisible</h4>
设置组件可见性。

 > (`void`) ItemNull:SetVisible(`bool` bVisible)

 ````lua
 ItemNull:SetVisible(false)
 ````

* <h4 id="LuaItemNull_Show">Show</h4>
显示组件，等同于 [`:SetVisible(true)`](#LuaItemNull_SetVisible)。

 > (`void`) ItemNull:Show([`bool|number` bShow = true])

如果提供了 `bShow` 且其为 `false`（或 `0`），则会**隐藏**该组件。

 ````lua
 ItemNull:Show()
 ItemNull:Show(true)
 ItemNull:Show(false) -- hide
 ````

* <h4 id="LuaItemNull_Hide">Hide</h4>
隐藏组件，等同于 [`:SetVisible(false)`](#LuaItemNull_SetVisible)。

 > (`void`) ItemNull:Hide([`bool|number` bHide = true])

如果提供了 `bHide` 且其为 `false`（或 `0`），则会**显示**该组件。

 ````lua
 ItemNull:Hide()
 ItemNull:Hide(true)
 ItemNull:Hide(false) -- show
 ````

* <h4 id="LuaItemNull_PtInItem">PtInItem</h4>
判断给定屏幕坐标是否落在该组件内。通常与 `Cursor.GetPos()` 配合使用。
 > (`bool` bIsInItem) ItemNull:PtInItem(`number` nX, `number` nY)

 ````lua
 local bIsInItem = ItemNull:PtInItem(600, 800)
 local bIsInItem = ItemNull:PtInItem(Cursor.GetPos())
 ````

* <h4 id="LuaItemNull_IsMouseIn">IsMouseIn</h4>
检查鼠标当前是否在该组件内部。

 > (`bool` bIsIn) ItemNull:IsMouseIn()

 ````lua
 local bIsIn = ItemNull:IsMouseIn()
 ````

* <h4 id="LuaItemNull_SetMouseButtonStatusElement">SetMouseButtonStatusElement</h4>
设置一个 UI 元素名，供引擎用于在该组件上反映鼠标按键状态。

 > (`void`) ItemNull:SetMouseButtonStatusElement(`string` szElementName)

 ````lua
 ItemNull:SetMouseButtonStatusElement("SomeUIElem")
 ````

* <h4 id="LuaItemNull_ClearMouseButtonStatusElement">ClearMouseButtonStatusElement</h4>
清除鼠标按键状态元素绑定。

 > (`void`) ItemNull:ClearMouseButtonStatusElement()

 ````lua
 ItemNull:ClearMouseButtonStatusElement()
 ````

* <h4 id="LuaItemNull_SetHoverElement">SetHoverElement</h4>
启用悬停响应样式，并设置悬停 UI 元素名。

 > (`void`) ItemNull:SetHoverElement(`string` szElementName)

 ````lua
 ItemNull:SetHoverElement("HoverElem")
 ````

* <h4 id="LuaItemNull_ClearHoverElement">ClearHoverElement</h4>
禁用悬停响应样式。

 > (`void`) ItemNull:ClearHoverElement()

 ````lua
 ItemNull:ClearHoverElement()
 ````

* <h4 id="LuaItemNull_SetRelX">SetRelX</h4>
设置组件相对坐标 X（相对父节点）。

 > (`void`) ItemNull:SetRelX(`number` nX)

 ````lua
 ItemNull:SetRelX(10)
 ````

* <h4 id="LuaItemNull_SetRelY">SetRelY</h4>
设置组件相对坐标 Y（相对父节点）。

 > (`void`) ItemNull:SetRelY(`number` nY)

 ````lua
 ItemNull:SetRelY(10)
 ````

* <h4 id="LuaItemNull_GetRelX">GetRelX</h4>
获取组件相对坐标 X（相对父节点）。

 > (`number` nX) ItemNull:GetRelX()

 ````lua
 local nX = ItemNull:GetRelX()
 ````

* <h4 id="LuaItemNull_GetRelY">GetRelY</h4>
获取组件相对坐标 Y（相对父节点）。

 > (`number` nY) ItemNull:GetRelY()

 ````lua
 local nY = ItemNull:GetRelY()
 ````

* <h4 id="LuaItemNull_SetAbsX">SetAbsX</h4>
设置组件绝对坐标 X（相对屏幕）。

 > (`void`) ItemNull:SetAbsX(`number` nX)

 ````lua
 ItemNull:SetAbsX(10)
 ````

* <h4 id="LuaItemNull_SetAbsY">SetAbsY</h4>
设置组件绝对坐标 Y（相对屏幕）。

 > (`void`) ItemNull:SetAbsY(`number` nY)

 ````lua
 ItemNull:SetAbsY(10)
 ````

* <h4 id="LuaItemNull_GetAbsX">GetAbsX</h4>
获取组件绝对坐标 X（相对屏幕）。

 > (`number` nX) ItemNull:GetAbsX()

 ````lua
 local nX = ItemNull:GetAbsX()
 ````

* <h4 id="LuaItemNull_GetAbsY">GetAbsY</h4>
获取组件绝对坐标 Y（相对屏幕）。

 > (`number` nY) ItemNull:GetAbsY()

 ````lua
 local nY = ItemNull:GetAbsY()
 ````

* <h4 id="LuaItemNull_SetW">SetW</h4>
设置组件宽度。

 > (`void`) ItemNull:SetW(`number` nW)

 ````lua
 ItemNull:SetW(100)
 ````

* <h4 id="LuaItemNull_SetH">SetH</h4>
设置组件高度。

 > (`void`) ItemNull:SetH(`number` nH)

 ````lua
 ItemNull:SetH(100)
 ````

* <h4 id="LuaItemNull_GetW">GetW</h4>
获取组件宽度。

 > (`number` nW) ItemNull:GetW()

 ````lua
 local nW = ItemNull:GetW()
 ````

* <h4 id="LuaItemNull_GetH">GetH</h4>
获取组件高度。

 > (`number` nH) ItemNull:GetH()

 ````lua
 local nH = ItemNull:GetH()
 ````

* <h4 id="LuaItemNull_SetRelPos">SetRelPos</h4>
设置组件相对坐标。相当于 [`:SetRelX`](#LuaItemNull_SetRelX) 与 [`:SetRelY`](#LuaItemNull_SetRelY) 的组合。

 > (`void`) ItemNull:SetRelPos(`number` nX, `number` nY)

 ````lua
 ItemNull:SetRelPos(100, 200)
 ````

* <h4 id="LuaItemNull_GetRelPos">GetRelPos</h4>
获取组件相对坐标。相当于 [`:GetRelX`](#LuaItemNull_GetRelX) 与 [`:GetRelY`](#LuaItemNull_GetRelY) 的组合。

 > (`number` nX, `number` nY) ItemNull:GetRelPos()

 ````lua
 local nX, nY = ItemNull:GetRelPos()
 ````

* <h4 id="LuaItemNull_SetAbsPos">SetAbsPos</h4>
设置组件绝对坐标。相当于 [`:SetAbsX`](#LuaItemNull_SetAbsX) 与 [`:SetAbsY`](#LuaItemNull_SetAbsY) 的组合。

 > (`void`) ItemNull:SetAbsPos(`number` nX, `number` nY)

 ````lua
 ItemNull:SetAbsPos(500, 300)
 ````

* <h4 id="LuaItemNull_GetAbsPos">GetAbsPos</h4>
获取组件绝对坐标。相当于 [`:GetAbsX`](#LuaItemNull_GetAbsX) 与 [`:GetAbsY`](#LuaItemNull_GetAbsY) 的组合。

 > (`number` nX, `number` nY) ItemNull:GetAbsPos()

 ````lua
 local nX, nY = ItemNull:GetAbsPos()
 ````

* <h4 id="LuaItemNull_SetSize">SetSize</h4>
设置组件尺寸。相当于 [`:SetW`](#LuaItemNull_SetW) 与 [`:SetH`](#LuaItemNull_SetH) 的组合。

 > (`void`) ItemNull:SetSize(`number` nW, `number` nH)

 ````lua
 ItemNull:SetSize(600, 800)
 ````

* <h4 id="LuaItemNull_GetSize">GetSize</h4>
获取组件尺寸。相当于 [`:GetW`](#LuaItemNull_GetW) 与 [`:GetH`](#LuaItemNull_GetH) 的组合。

 > (`number` nW, `number` nH) ItemNull:GetSize()

 ````lua
 local nW, nH = ItemNull:GetSize()
 ````

* <h4 id="LuaItemNull_SetPosType">SetPosType</h4>
设置组件位置类型。参见 [`ITEM_POSITION`](#ITEM_POSITION) 的枚举。

 > (`void`) ItemNull:SetPosType(`number` nPosType)

 ````lua
 ItemNull:SetPosType(ITEM_POSITION.RIGHT_BOTTOM)
 ````

* <h4 id="LuaItemNull_GetPosType">GetPosType</h4>
获取组件位置类型。参见 [`ITEM_POSITION`](#ITEM_POSITION) 的枚举。

 > (`enum` nPosType) ItemNull:GetPosType()

 ````lua
 local nPosType = ItemNull:GetPosType()
 ````

* <h4 id="LuaItemNull_IsVisible">IsVisible</h4>
获取组件可见性。

 > (`bool` bVisible) ItemNull:IsVisible()

 ````lua
 local bVisible = ItemNull:IsVisible()
 ````

* <h4 id="LuaItemNull_GetName">GetName</h4>
获取组件名。

 > (`string` szName) ItemNull:GetName()

 ````lua
 local szName = ItemNull:GetName()
 ````

* <h4 id="LuaItemNull_SetName">SetName</h4>
设置组件名。

 > (`void`) ItemNull:SetName(`string` szName)

 ````lua
 ItemNull:SetName("Item_001")
 ````

* <h4 id="LuaItemNull_SetTip">SetTip</h4>
设置组件 Tip。鼠标移入时会显示 Tip。

重载：

> * (`void`) ItemNull:SetTip(`number` nTipIndex)
> * (`void`) ItemNull:SetTip(`string` szTip, `number` nShowTipType[, `bool|number` bRichText[, `string` szBgPath[, `number` nBgFrame[, `number` nBgAlpha]]]])

说明：

- 如果 `nTipIndex < 0`，会清除 Tip（设置为无效的 tip index）。

 ````lua
 ItemNull:SetTip(-1) -- 清除
 ItemNull:SetTip(123) -- 使用已有 tip index

 -- 从文本 + 展示类型创建
 ItemNull:SetTip("this is a tip", 0)
 ItemNull:SetTip('<text>text="rich tip"</text>', 0, true)
 ````

* <h4 id="LuaItemNull_GetTip">GetTip</h4>
获取组件 Tip。

 > (`string` szTip, `number` nShowTipType) ItemNull:GetTip()

 ````lua
 local szTip, nShowTipType = ItemNull:GetTip()
 ````

* <h4 id="LuaItemNull_SetUserData">SetUserData</h4>
给组件设置一个数字 userdata。

 > (`void`) ItemNull:SetUserData(`number` nData)

 ````lua
 ItemNull:SetUserData(27)
 ````

* <h4 id="LuaItemNull_GetUserData">GetUserData</h4>
获取组件的 userdata。

 > (`number` nData) ItemNull:GetUserData()

 ````lua
 local nData = ItemNull:GetUserData()
 ````

* <h4 id="LuaItemNull_RegisterEvent">RegisterEvent</h4>
注册 UI 事件，使该组件能够响应指定的 UI 事件（例如鼠标点击事件）。

 > (`void`) ItemNull:RegisterEvent(`number` nUIEvent)

 ````lua
 ItemNull:RegisterEvent(256)
 ````

* <h4 id="LuaItemNull_ClearEvent">ClearEvent</h4>
清除该组件上的所有 UI 事件。

 > (`void`) ItemNull:ClearEvent([`bool|number` bForceClear = false])

 ````lua
 ItemNull:ClearEvent()
 ItemNull:ClearEvent(true)
 ````

* <h4 id="LuaItemNull_EnableScale">EnableScale</h4>
设置该组件是否可缩放。

 > (`void`) ItemNull:EnableScale(`bool` bEnableScale)

 ````lua
 ItemNull:EnableScale(true)
 ````

* <h4 id="LuaItemNull_Scale">Scale</h4>
缩放该组件。

注意：其子组件也会一起缩放。另外请记得把缩放值自行保存到某处，因为没有 API 可以获取当前缩放值。

此 API 的工作原理是：遍历自身与所有子节点，将宽高乘以给定缩放值。

 > (`void`) ItemNull:Scale(`number` fScaleX, `number` fScaleY)

 ````lua
 ItemNull:Scale(0.7, 0.9)
 ````

* <h4 id="LuaItemNull_LockShowAndHide">LockShowAndHide</h4>
设置该组件的默认可见性是否为不可见。

 > (`void`) ItemNull:LockShowAndHide(`bool` bEnable)

 ````lua
 ItemNull:LockShowAndHide(true)
 ````

* <h4 id="LuaItemNull_SetAlpha">SetAlpha</h4>
设置 alpha，范围 0~255。

 > (`void`) ItemNull:SetAlpha(`number` nAlpha)

 ````lua
 ItemNull:SetAlpha(255)
 ````

* <h4 id="LuaItemNull_GetAlpha">GetAlpha</h4>
获取 alpha（0~255）。

 > (`number` nAlpha) ItemNull:GetAlpha()

 ````lua
 local nAlpha = ItemNull:GetAlpha()
 ````

* <h4 id="LuaItemNull_GetParent">GetParent</h4>
获取父节点。

如果它有父 Item，则返回该父 Item。

如果它没有父 Item（例如根 handle），则返回它所属的 Window。

 > (`KGUI OBJECT` pParent) ItemNull:GetParent()

 ````lua
 local hParent = ItemNull:GetParent()
 ````

* <h4 id="LuaItemNull_GetRoot">GetRoot</h4>
获取根父节点（frame）。

 > (`KGUI Frame` pFrame) ItemNull:GetRoot()

 ````lua
 local hFrame = ItemNull:GetRoot()
 ````

* <h4 id="LuaItemNull_GetType">GetType</h4>
获取 UI 类型，例如 `WndWindow`、`Handle`、`Text` 等。

 > (`string` szType) ItemNull:GetType()

 ````lua
 local szType = ItemNull:GetType()
 ````

* <h4 id="LuaItemNull_GetIndex">GetIndex</h4>
获取索引。取值范围为 0 到其兄弟节点数量。

 > (`number` nIndex) ItemNull:GetIndex()

 ````lua
 local nIndex = ItemNull:GetIndex()
 ````

* <h4 id="LuaItemNull_SetIndex">SetIndex</h4>
设置索引。取值必须在 0 到其兄弟节点数量范围内。

 > (`void`) ItemNull:SetIndex(`number` nIndex)

 ````lua
 ItemNull:SetIndex(0)
 ````

* <h4 id="LuaItemNull_ExchangeIndex">ExchangeIndex</h4>
与某个兄弟节点交换索引。
> * (`void`) ItemNull:ExchangeIndex(`number` nIndex)
> * (`void`) ItemNull:ExchangeIndex(`KGUI Object` pBrotherItem)

 ````lua
 ItemNull:ExchangeIndex(0)
 ItemNull:ExchangeIndex(ItemNull:GetParent():Lookup(0))
 ````

* <h4 id="LuaItemNull_GetTreePath">GetTreePath</h4>
获取该组件的树路径。

 > (`string` szWndTreePath, `string` szHandleTreePath) ItemNull:GetTreePath()

 ````lua
 local szWndTreePath, szHandleTreePath = ItemNull:GetTreePath()
 ````

* <h4 id="LuaItemNull_SetAreaTestFile">SetAreaTestFile</h4>
设置（或清除）引擎用于命中测试的 area test 文件。

 > (`void`) ItemNull:SetAreaTestFile([`string` szFile])

 ````lua
 ItemNull:SetAreaTestFile("ui/areatest/xxx.atf")
 ItemNull:SetAreaTestFile() -- 清除
 ````

* <h4 id="LuaItemNull_SetIntPos">SetIntPos</h4>
启用/禁用整数坐标模式。

 > (`void`) ItemNull:SetIntPos(`bool|number` bIntPos)

 ````lua
 ItemNull:SetIntPos(true)
 ````

* <h4 id="LuaItemNull_IsIntPos">IsIntPos</h4>
获取整数坐标模式。

 > (`bool` bIntPos) ItemNull:IsIntPos()

 ````lua
 local bIntPos = ItemNull:IsIntPos()
 ````

* <h4 id="LuaItemNull_IsLink">IsLink</h4>
检查该组件是否为 link 组件。

 > (`bool` bIsLink) ItemNull:IsLink()

 ````lua
 local bIsLink = ItemNull:IsLink()
 ````

* <h4 id="LuaItemNull_GetLinkInfo">GetLinkInfo</h4>
获取 link info 字符串。

 > (`string` szLinkInfo) ItemNull:GetLinkInfo()

 ````lua
 local szLinkInfo = ItemNull:GetLinkInfo()
 ````

* <h4 id="LuaItemNull_SetLinkInfo">SetLinkInfo</h4>
设置 link info 字符串。

 > (`void`) ItemNull:SetLinkInfo(`string` szLinkInfo)

 ````lua
 ItemNull:SetLinkInfo("some_link_payload")
 ````

* <h4 id="LuaItemNull_SetTweenAni">SetTweenAni</h4>
同时设置 tween 文件与 tween 名称。

 > (`void`) ItemNull:SetTweenAni(`string` szTweenFile, `string` szTweenName)

 ````lua
 ItemNull:SetTweenAni("ui/tween/some.tween", "FadeIn")
 ````

* <h4 id="LuaItemNull_GetTweenFile">GetTweenFile</h4>
获取 tween 文件路径。

如果未设置，则该 API 不返回任何值。

 > (`string|nil` szTweenFile) ItemNull:GetTweenFile()

 ````lua
 local szTweenFile = ItemNull:GetTweenFile()
 ````

* <h4 id="LuaItemNull_SetTweenFile">SetTweenFile</h4>
设置 tween 文件路径。

 > (`void`) ItemNull:SetTweenFile(`string` szTweenFile)

 ````lua
 ItemNull:SetTweenFile("ui/tween/some.tween")
 ````

* <h4 id="LuaItemNull_GetTweenName">GetTweenName</h4>
获取 tween 名称。

如果未设置，则该 API 不返回任何值。

 > (`string|nil` szTweenName) ItemNull:GetTweenName()

 ````lua
 local szTweenName = ItemNull:GetTweenName()
 ````

* <h4 id="LuaItemNull_SetTweenName">SetTweenName</h4>
设置 tween 名称。

 > (`void`) ItemNull:SetTweenName(`string` szTweenName)

 ````lua
 ItemNull:SetTweenName("FadeIn")
 ````

* <h4 id="LuaItemNull_GetAniParamID">GetAniParamID</h4>
获取一个不透明的动画参数 id 对象（userdata）。

 > (`userdata` pAniParamID) ItemNull:GetAniParamID()

 ````lua
 local pAniParamID = ItemNull:GetAniParamID()
 ````

* <h4 id="LuaItemNull_SetPoint">SetPoint</h4>
锚定/定位该组件。

重载：

> * (`void`) ItemNull:SetPoint(`number` nX, `number` nY)
> * (`void`) ItemNull:SetPoint(`string` szSrcSide, `number` nX, `number` nY, `string` szRelSide, `number` nOffsetX, `number` nOffsetY)
> * (`void`) ItemNull:SetPoint(`string` szSrcSide, `number` nX, `number` nY, `KGUI Object|string` hRelUIOrWndTreePath, `string` szRelSide, `number` nOffsetX, `number` nOffsetY)

说明：

- 在 6 参数重载（不含 `hRelUIOrWndTreePath`）中，相对目标默认是**根 client area**。
- `szSrcSide` / `szRelSide` 使用与窗口锚点相同的 side 字符串（例如 `"TOPLEFT"`、`"CENTER"`、`"BOTTOMRIGHT"` 等）。

 ````lua
 -- absolute
 ItemNull:SetPoint(100, 200)

 -- relative to root client area
 ItemNull:SetPoint("TOPLEFT", 0, 0, "TOPLEFT", 10, 10)

 -- relative to another UI object or a window treepath
 ItemNull:SetPoint("CENTER", 0, 0, SomeOtherItem, "CENTER", 0, 0)
 ItemNull:SetPoint("CENTER", 0, 0, "UI/Frame1", "CENTER", 0, 0)
 ````

* <h4 id="LuaItemNull_SetBasicStatus">SetBasicStatus</h4>
启用/禁用该组件上的基础状态标志。

 > (`void`) ItemNull:SetBasicStatus(`number` nStatus, `bool` bEnable)

 ````lua
 ItemNull:SetBasicStatus(0, true)
 ````

* <h4 id="LuaItemNull_ToGray">ToGray</h4>
应用灰化效果。

 > (`void`) ItemNull:ToGray()

 ````lua
 ItemNull:ToGray()
 ````

* <h4 id="LuaItemNull_ToNormal">ToNormal</h4>
移除灰化效果。

 > (`void`) ItemNull:ToNormal()

 ````lua
 ItemNull:ToNormal()
 ````

* <h4 id="LuaItemNull_IsGray">IsGray</h4>
检查是否已应用灰化效果。

 > (`bool` bGray) ItemNull:IsGray()

 ````lua
 local bGray = ItemNull:IsGray()
 ````

* <h4 id="LuaItemNull_Lookup">Lookup</h4>
按树路径（相对该组件）查找后代组件。

返回找到的组件对象；如果未找到则不返回任何值。

 > (`KGUI Object|nil` hItem) ItemNull:Lookup(`string` szTreePath)

 ````lua
 local hItem = ItemNull:Lookup("Child1/Child2")
 ````

* <h4 id="LuaItemNull_IsValid">IsValid</h4>
检查该组件是否仍然有效。一旦组件被销毁，该 API 会返回 `false`。

 > (`bool` bValid) ItemNull:IsValid()

 ````lua
 local bValid = ItemNull:IsValid()
 ````

* <h4 id="LuaItemNull_NewIndex">__newindex</h4>
当对 ItemNull 对象赋值自定义字段时触发的元方法（例如 `ItemNull.someField = value`）。

当该元方法启用时：首次写入时引擎会把 Lua 侧对象表保存为 registry 引用，然后用 `rawset` 将字段写入该对象表。

注意：当前源码中 ItemNull 元表里 `__newindex` 的注册被注释掉了，因此该元方法可能不会生效。

 > (`void`) ItemNull:__newindex(`string|number` key, `bool|number|string|table|userdata|nil` value)

 ````lua
 ItemNull.someField = 123
 ItemNull["anotherField"] = "abc"
 ItemNull.someField = nil -- delete
 ````

* <h4 id="LuaItemNull_Equal">__eq</h4>
用于 `==` 的元方法，用来比较两个 ItemNull 对象是否相等。

仅当两侧引用同一个底层引擎对象指针（且指针非空）时返回 `true`。

 > (`bool` bEqual) ItemNull:__eq(`ItemNull` other)

 ````lua
 if ItemNullA == ItemNullB then
	 -- same item
 end
 ````

* <h4 id="LuaItemNull_GetBaseType">GetBaseType</h4>
获取基础类型。对 Item* 对象而言该接口固定返回 `Item`。

 > (`string` szBaseType) ItemNull:GetBaseType()

 ````lua
 local szBaseType = ItemNull:GetBaseType()
 ````
