# ItemNull

Notes:

- For position/size related APIs, Lua side uses **unscaled UI coordinates**. Internally values are multiplied by `Station.GetUIScale()`. Corresponding getters divide by UIScale before returning.

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
Set Item Visibility.

 > (`void`) ItemNull:SetVisible(`bool` bVisible)

 ````lua
 ItemNull:SetVisible(false)
 ````

* <h4 id="LuaItemNull_Show">Show</h4>
Show Item, same as [`:SetVisible(true)`](#LuaItemNull_SetVisible).

 > (`void`) ItemNull:Show([`bool|number` bShow = true])

If `bShow` is provided and is `false` (or `0`), it will **hide** the item.

 ````lua
 ItemNull:Show()
 ItemNull:Show(true)
 ItemNull:Show(false) -- hide
 ````

* <h4 id="LuaItemNull_Hide">Hide</h4>
Hide Item, same as [`:SetVisible(false)`](#LuaItemNull_SetVisible).

 > (`void`) ItemNull:Hide([`bool|number` bHide = true])

If `bHide` is provided and is `false` (or `0`), it will **show** the item.

 ````lua
 ItemNull:Hide()
 ItemNull:Hide(true)
 ItemNull:Hide(false) -- show
 ````

* <h4 id="LuaItemNull_PtInItem">PtInItem</h4>
Judge if a given screen position is in this Item. Always use with `Cursor.GetPos()`.
 > (`bool` bIsInItem) ItemNull:PtInItem(`number` nX, `number` nY)

 ````lua
 local bIsInItem = ItemNull:PtInItem(600, 800)
 local bIsInItem = ItemNull:PtInItem(Cursor.GetPos())
 ````

* <h4 id="LuaItemNull_IsMouseIn">IsMouseIn</h4>
Check whether mouse cursor is currently inside this item.

 > (`bool` bIsIn) ItemNull:IsMouseIn()

 ````lua
 local bIsIn = ItemNull:IsMouseIn()
 ````

* <h4 id="LuaItemNull_SetMouseButtonStatusElement">SetMouseButtonStatusElement</h4>
Set a UI element name used by the engine to reflect mouse button status on this item.

 > (`void`) ItemNull:SetMouseButtonStatusElement(`string` szElementName)

 ````lua
 ItemNull:SetMouseButtonStatusElement("SomeUIElem")
 ````

* <h4 id="LuaItemNull_ClearMouseButtonStatusElement">ClearMouseButtonStatusElement</h4>
Clear the mouse button status element binding.

 > (`void`) ItemNull:ClearMouseButtonStatusElement()

 ````lua
 ItemNull:ClearMouseButtonStatusElement()
 ````

* <h4 id="LuaItemNull_SetHoverElement">SetHoverElement</h4>
Enable hover response style and set the hover UI element name.

 > (`void`) ItemNull:SetHoverElement(`string` szElementName)

 ````lua
 ItemNull:SetHoverElement("HoverElem")
 ````

* <h4 id="LuaItemNull_ClearHoverElement">ClearHoverElement</h4>
Disable hover response style.

 > (`void`) ItemNull:ClearHoverElement()

 ````lua
 ItemNull:ClearHoverElement()
 ````

* <h4 id="LuaItemNull_SetRelX">SetRelX</h4>
Set Item's relative X (to its parent).

 > (`void`) ItemNull:SetRelX(`number` nX)

 ````lua
 ItemNull:SetRelX(10)
 ````

* <h4 id="LuaItemNull_SetRelY">SetRelY</h4>
Set Item's relative Y (to its parent).

 > (`void`) ItemNull:SetRelY(`number` nY)

 ````lua
 ItemNull:SetRelY(10)
 ````

* <h4 id="LuaItemNull_GetRelX">GetRelX</h4>
Get Item's relative X (to its parent).

 > (`number` nX) ItemNull:GetRelX()

 ````lua
 local nX = ItemNull:GetRelX()
 ````

* <h4 id="LuaItemNull_GetRelY">GetRelY</h4>
Get Item's relative Y (to its parent).

 > (`number` nY) ItemNull:GetRelY()

 ````lua
 local nY = ItemNull:GetRelY()
 ````

* <h4 id="LuaItemNull_SetAbsX">SetAbsX</h4>
Set Item's absolute X (to the screen).

 > (`void`) ItemNull:SetAbsX(`number` nX)

 ````lua
 ItemNull:SetAbsX(10)
 ````

* <h4 id="LuaItemNull_SetAbsY">SetAbsY</h4>
Set Item's absolute Y (to the screen).

 > (`void`) ItemNull:SetAbsY(`number` nY)

 ````lua
 ItemNull:SetAbsY(10)
 ````

* <h4 id="LuaItemNull_GetAbsX">GetAbsX</h4>
Get Item's absolute X (to the screen).

 > (`number` nX) ItemNull:GetAbsX()

 ````lua
 local nX = ItemNull:GetAbsX()
 ````

* <h4 id="LuaItemNull_GetAbsY">GetAbsY</h4>
Get Item's absolute Y (to the screen).

 > (`number` nY) ItemNull:GetAbsY()

 ````lua
 local nY = ItemNull:GetAbsY()
 ````

* <h4 id="LuaItemNull_SetW">SetW</h4>
Set Item's width.

 > (`void`) ItemNull:SetW(`number` nW)

 ````lua
 ItemNull:SetW(100)
 ````

* <h4 id="LuaItemNull_SetH">SetH</h4>
Set Item's height.

 > (`void`) ItemNull:SetH(`number` nH)

 ````lua
 ItemNull:SetH(100)
 ````

* <h4 id="LuaItemNull_GetW">GetW</h4>
Get Item's width.

 > (`number` nW) ItemNull:GetW()

 ````lua
 local nW = ItemNull:GetW()
 ````

* <h4 id="LuaItemNull_GetH">GetH</h4>
Get Item's height.

 > (`number` nH) ItemNull:GetH()

 ````lua
 local nH = ItemNull:GetH()
 ````

* <h4 id="LuaItemNull_SetRelPos">SetRelPos</h4>
Set Item's relative position. The union of [`:SetRelX`](#LuaItemNull_SetRelX) and [`:SetRelY`](#LuaItemNull_SetRelY).

 > (`void`) ItemNull:SetRelPos(`number` nX, `number` nY)

 ````lua
 ItemNull:SetRelPos(100, 200)
 ````

* <h4 id="LuaItemNull_GetRelPos">GetRelPos</h4>
Get Item's relative position. The union of [`:GetRelX`](#LuaItemNull_GetRelX) and [`:GetRelY`](#LuaItemNull_GetRelY).

 > (`number` nX, `number` nY) ItemNull:GetRelPos()

 ````lua
 local nX, nY = ItemNull:GetRelPos()
 ````

* <h4 id="LuaItemNull_SetAbsPos">SetAbsPos</h4>
Set Item's absolute position. The union of [`:SetAbsX`](#LuaItemNull_SetAbsX) and [`:SetAbsY`](#LuaItemNull_SetAbsY).

 > (`void`) ItemNull:SetAbsPos(`number` nX, `number` nY)

 ````lua
 ItemNull:SetAbsPos(500, 300)
 ````

* <h4 id="LuaItemNull_GetAbsPos">GetAbsPos</h4>
Get Item's absolute position. The union of [`:GetAbsX`](#LuaItemNull_GetAbsX) and [`:GetAbsY`](#LuaItemNull_GetAbsY).

 > (`number` nX, `number` nY) ItemNull:GetAbsPos()

 ````lua
 local nX, nY = ItemNull:GetAbsPos()
 ````

* <h4 id="LuaItemNull_SetSize">SetSize</h4>
Set Item's size. The union of [`:SetW`](#LuaItemNull_SetW) and [`:SetH`](#LuaItemNull_SetH).

 > (`void`) ItemNull:SetSize(`number` nW, `number` nH)

 ````lua
 ItemNull:SetSize(600, 800)
 ````

* <h4 id="LuaItemNull_GetSize">GetSize</h4>
Get Item's size. The union of [`:GetW`](#LuaItemNull_GetW) and [`:GetH`](#LuaItemNull_GetH).

 > (`number` nW, `number` nH) ItemNull:GetSize()

 ````lua
 local nW, nH = ItemNull:GetSize()
 ````

* <h4 id="LuaItemNull_SetPosType">SetPosType</h4>
Set Item's position type. See the enum of [`ITEM_POSITION`](#ITEM_POSITION).

 > (`void`) ItemNull:SetPosType(`number` nPosType)

 ````lua
 ItemNull:SetPosType(ITEM_POSITION.RIGHT_BOTTOM)
 ````

* <h4 id="LuaItemNull_GetPosType">GetPosType</h4>
Get Item's position type. See the enum of [`ITEM_POSITION`](#ITEM_POSITION).

 > (`enum` nPosType) ItemNull:GetPosType()

 ````lua
 local nPosType = ItemNull:GetPosType()
 ````

* <h4 id="LuaItemNull_IsVisible">IsVisible</h4>
Get Item's visibility.

 > (`bool` bVisible) ItemNull:IsVisible()

 ````lua
 local bVisible = ItemNull:IsVisible()
 ````

* <h4 id="LuaItemNull_GetName">GetName</h4>
Get Item's name.

 > (`string` szName) ItemNull:GetName()

 ````lua
 local szName = ItemNull:GetName()
 ````

* <h4 id="LuaItemNull_SetName">SetName</h4>
Set Item's name.

 > (`void`) ItemNull:SetName(`string` szName)

 ````lua
 ItemNull:SetName("Item_001")
 ````

* <h4 id="LuaItemNull_SetTip">SetTip</h4>
Set Item's tip. When mouse enter it, the tip will be shown.

Overloads:

> * (`void`) ItemNull:SetTip(`number` nTipIndex)
> * (`void`) ItemNull:SetTip(`string` szTip, `number` nShowTipType[, `bool|number` bRichText[, `string` szBgPath[, `number` nBgFrame[, `number` nBgAlpha]]]])

Notes:

- If `nTipIndex < 0`, it will clear the tip (set to an invalid tip index).

 ````lua
 ItemNull:SetTip(-1) -- clear
 ItemNull:SetTip(123) -- set by existing tip index

 -- create from text + show type
 ItemNull:SetTip("this is a tip", 0)
 ItemNull:SetTip('<text>text="rich tip"</text>', 0, true)
 ````

* <h4 id="LuaItemNull_GetTip">GetTip</h4>
Get Item's tip.

 > (`string` szTip, `number` nShowTipType) ItemNull:GetTip()

 ````lua
 local szTip, nShowTipType = ItemNull:GetTip()
 ````

* <h4 id="LuaItemNull_SetUserData">SetUserData</h4>
Set a number to the Item.

 > (`void`) ItemNull:SetUserData(`number` nData)

 ````lua
 ItemNull:SetUserData(27)
 ````

* <h4 id="LuaItemNull_GetUserData">GetUserData</h4>
Get Item's userdata.

 > (`number` nData) ItemNull:GetUserData()

 ````lua
 local nData = ItemNull:GetUserData()
 ````

* <h4 id="LuaItemNull_RegisterEvent">RegisterEvent</h4>
Register an ui event so that this item is able to response the specified ui event such as mouse click event.

 > (`void`) ItemNull:RegisterEvent(`number` nUIEvent)

 ````lua
 ItemNull:RegisterEvent(256)
 ````

* <h4 id="LuaItemNull_ClearEvent">ClearEvent</h4>
Clear all ui event on this Item.

 > (`void`) ItemNull:ClearEvent([`bool|number` bForceClear = false])

 ````lua
 ItemNull:ClearEvent()
 ItemNull:ClearEvent(true)
 ````

* <h4 id="LuaItemNull_EnableScale">EnableScale</h4>
Set if this Item can be scaled.

 > (`void`) ItemNull:EnableScale(`bool` bEnableScale)

 ````lua
 ItemNull:EnableScale(true)
 ````

* <h4 id="LuaItemNull_Scale">Scale</h4>
Scale an Item. Please noticed that it's children will also be scaled. And remember to save the scale to some place because there is no api to get current scale level. The working principle of this api is just traverse all its children and itself and make their width and height multiplied with the given scale value.

 > (`void`) ItemNull:Scale(`number` fScaleX, `number` fScaleY)

 ````lua
 ItemNull:Scale(0.7, 0.9)
 ````

* <h4 id="LuaItemNull_LockShowAndHide">LockShowAndHide</h4>
Set if this Item's default visibility is invisible.

 > (`void`) ItemNull:LockShowAndHide(`bool` bEnable)

 ````lua
 ItemNull:LockShowAndHide(true)
 ````

* <h4 id="LuaItemNull_SetAlpha">SetAlpha</h4>
Set its alpha. The value can be set between 0 and 255.

 > (`void`) ItemNull:SetAlpha(`number` nAlpha)

 ````lua
 ItemNull:SetAlpha(255)
 ````

* <h4 id="LuaItemNull_GetAlpha">GetAlpha</h4>
Get its alpha value (0 - 255).

 > (`number` nAlpha) ItemNull:GetAlpha()

 ````lua
 local nAlpha = ItemNull:GetAlpha()
 ````

* <h4 id="LuaItemNull_GetParent">GetParent</h4>
Get its parent node.

If it has a parent item, returns that parent item.

If it does not have a parent item (e.g. a root handle), it returns its owner window.

 > (`KGUI OBJECT` pParent) ItemNull:GetParent()

 ````lua
 local hParent = ItemNull:GetParent()
 ````

* <h4 id="LuaItemNull_GetRoot">GetRoot</h4>
Get its root parent node (the frame).

 > (`KGUI Frame` pFrame) ItemNull:GetRoot()

 ````lua
 local hFrame = ItemNull:GetRoot()
 ````

* <h4 id="LuaItemNull_GetType">GetType</h4>
Get its ui type, such as `WndWindow`, `Handle`, `Text`, etc.

 > (`string` szType) ItemNull:GetType()

 ````lua
 local szType = ItemNull:GetType()
 ````

* <h4 id="LuaItemNull_GetIndex">GetIndex</h4>
Get its index. The value will between 0 and the count of its brothers.

 > (`number` nIndex) ItemNull:GetIndex()

 ````lua
 local nIndex = ItemNull:GetIndex()
 ````

* <h4 id="LuaItemNull_SetIndex">SetIndex</h4>
Set its index. The value must between 0 and the count of its brothers.

 > (`void`) ItemNull:SetIndex(`number` nIndex)

 ````lua
 ItemNull:SetIndex(0)
 ````

* <h4 id="LuaItemNull_ExchangeIndex">ExchangeIndex</h4>
Exchange the index with one of its brothers.
> * (`void`) ItemNull:ExchangeIndex(`number` nIndex)
> * (`void`) ItemNull:ExchangeIndex(`KGUI Object` pBrotherItem)

 ````lua
 ItemNull:ExchangeIndex(0)
 ItemNull:ExchangeIndex(ItemNull:GetParent():Lookup(0))
 ````

* <h4 id="LuaItemNull_GetTreePath">GetTreePath</h4>
Get the tree path of this Item.

 > (`string` szWndTreePath, `string` szHandleTreePath) ItemNull:GetTreePath()

 ````lua
 local szWndTreePath, szHandleTreePath = ItemNull:GetTreePath()
 ````

* <h4 id="LuaItemNull_SetAreaTestFile">SetAreaTestFile</h4>
Set (or clear) the area test file used by the engine for hit-testing.

 > (`void`) ItemNull:SetAreaTestFile([`string` szFile])

 ````lua
 ItemNull:SetAreaTestFile("ui/areatest/xxx.atf")
 ItemNull:SetAreaTestFile() -- clear
 ````

* <h4 id="LuaItemNull_SetIntPos">SetIntPos</h4>
Enable/disable integer-position mode.

 > (`void`) ItemNull:SetIntPos(`bool|number` bIntPos)

 ````lua
 ItemNull:SetIntPos(true)
 ````

* <h4 id="LuaItemNull_IsIntPos">IsIntPos</h4>
Get integer-position mode.

 > (`bool` bIntPos) ItemNull:IsIntPos()

 ````lua
 local bIntPos = ItemNull:IsIntPos()
 ````

* <h4 id="LuaItemNull_IsLink">IsLink</h4>
Check whether this item is a link item.

 > (`bool` bIsLink) ItemNull:IsLink()

 ````lua
 local bIsLink = ItemNull:IsLink()
 ````

* <h4 id="LuaItemNull_GetLinkInfo">GetLinkInfo</h4>
Get link info string.

 > (`string` szLinkInfo) ItemNull:GetLinkInfo()

 ````lua
 local szLinkInfo = ItemNull:GetLinkInfo()
 ````

* <h4 id="LuaItemNull_SetLinkInfo">SetLinkInfo</h4>
Set link info string.

 > (`void`) ItemNull:SetLinkInfo(`string` szLinkInfo)

 ````lua
 ItemNull:SetLinkInfo("some_link_payload")
 ````

* <h4 id="LuaItemNull_SetTweenAni">SetTweenAni</h4>
Set both tween file and tween name.

 > (`void`) ItemNull:SetTweenAni(`string` szTweenFile, `string` szTweenName)

 ````lua
 ItemNull:SetTweenAni("ui/tween/some.tween", "FadeIn")
 ````

* <h4 id="LuaItemNull_GetTweenFile">GetTweenFile</h4>
Get tween file path.

If not set, this API returns no value.

 > (`string|nil` szTweenFile) ItemNull:GetTweenFile()

 ````lua
 local szTweenFile = ItemNull:GetTweenFile()
 ````

* <h4 id="LuaItemNull_SetTweenFile">SetTweenFile</h4>
Set tween file path.

 > (`void`) ItemNull:SetTweenFile(`string` szTweenFile)

 ````lua
 ItemNull:SetTweenFile("ui/tween/some.tween")
 ````

* <h4 id="LuaItemNull_GetTweenName">GetTweenName</h4>
Get tween name.

If not set, this API returns no value.

 > (`string|nil` szTweenName) ItemNull:GetTweenName()

 ````lua
 local szTweenName = ItemNull:GetTweenName()
 ````

* <h4 id="LuaItemNull_SetTweenName">SetTweenName</h4>
Set tween name.

 > (`void`) ItemNull:SetTweenName(`string` szTweenName)

 ````lua
 ItemNull:SetTweenName("FadeIn")
 ````

* <h4 id="LuaItemNull_GetAniParamID">GetAniParamID</h4>
Get an opaque animation parameter id object (userdata).

 > (`userdata` pAniParamID) ItemNull:GetAniParamID()

 ````lua
 local pAniParamID = ItemNull:GetAniParamID()
 ````

* <h4 id="LuaItemNull_SetPoint">SetPoint</h4>
Anchor/position this item.

Overloads:

> * (`void`) ItemNull:SetPoint(`number` nX, `number` nY)
> * (`void`) ItemNull:SetPoint(`string` szSrcSide, `number` nX, `number` nY, `string` szRelSide, `number` nOffsetX, `number` nOffsetY)
> * (`void`) ItemNull:SetPoint(`string` szSrcSide, `number` nX, `number` nY, `KGUI Object|string` hRelUIOrWndTreePath, `string` szRelSide, `number` nOffsetX, `number` nOffsetY)

Notes:

- In the 6-arg overload (without `hRelUIOrWndTreePath`), the relative target defaults to the **root client area**.
- `szSrcSide` / `szRelSide` uses the same side strings as window anchoring (e.g. `"TOPLEFT"`, `"CENTER"`, `"BOTTOMRIGHT"`, etc.).

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
Enable/disable a basic status flag on this item.

 > (`void`) ItemNull:SetBasicStatus(`number` nStatus, `bool` bEnable)

 ````lua
 ItemNull:SetBasicStatus(0, true)
 ````

* <h4 id="LuaItemNull_ToGray">ToGray</h4>
Apply gray effect.

 > (`void`) ItemNull:ToGray()

 ````lua
 ItemNull:ToGray()
 ````

* <h4 id="LuaItemNull_ToNormal">ToNormal</h4>
Remove gray effect.

 > (`void`) ItemNull:ToNormal()

 ````lua
 ItemNull:ToNormal()
 ````

* <h4 id="LuaItemNull_IsGray">IsGray</h4>
Check if gray effect is applied.

 > (`bool` bGray) ItemNull:IsGray()

 ````lua
 local bGray = ItemNull:IsGray()
 ````

* <h4 id="LuaItemNull_Lookup">Lookup</h4>
Lookup a descendant item by tree path (relative to this item).

Returns the found item object, or nothing if not found.

 > (`KGUI Object|nil` hItem) ItemNull:Lookup(`string` szTreePath)

 ````lua
 local hItem = ItemNull:Lookup("Child1/Child2")
 ````

* <h4 id="LuaItemNull_IsValid">IsValid</h4>
Check if this Item is still vaild. Once the Item get destroyed, this api will return `false`.

 > (`bool` bValid) ItemNull:IsValid()

 ````lua
 local bValid = ItemNull:IsValid()
 ````

* <h4 id="LuaItemNull_NewIndex">__newindex</h4>
Metamethod used when assigning a custom field on the ItemNull object (for example `ItemNull.someField = value`).

When enabled, the engine stores a registry reference to the Lua-side object table on the first assignment, then performs a `rawset` to save the field.

Note: in current source, `__newindex` registration is commented out in the ItemNull metatable, so this metamethod may not be active.

 > (`void`) ItemNull:__newindex(`string|number` key, `bool|number|string|table|userdata|nil` value)

 ````lua
 ItemNull.someField = 123
 ItemNull["anotherField"] = "abc"
 ItemNull.someField = nil -- delete
 ````

* <h4 id="LuaItemNull_Equal">__eq</h4>
Metamethod used by `==` to compare two ItemNull objects.

Returns `true` only when both operands refer to the same underlying engine object pointer (and the pointer is not null).

 > (`bool` bEqual) ItemNull:__eq(`ItemNull` other)

 ````lua
 if ItemNullA == ItemNullB then
	 -- same item
 end
 ````

* <h4 id="LuaItemNull_GetBaseType">GetBaseType</h4>
Get its base type. For Item* objects this always returns `Item`.

 > (`string` szBaseType) ItemNull:GetBaseType()

 ````lua
 local szBaseType = ItemNull:GetBaseType()
 ````
