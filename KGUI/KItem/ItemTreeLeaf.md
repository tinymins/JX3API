# ItemTreeLeaf

Notes:

- `ItemTreeLeaf` metatable also includes all `ItemHandle` methods; see [KGUI/KItem/ItemHandle.md](./ItemHandle.md).
- For position/size related APIs here, Lua side uses **unscaled UI coordinates**. Internally values are multiplied by `Station.GetUIScale()`. Corresponding getters divide by UIScale before returning.

[`IsExpand`](#LuaItemTreeLeaf_IsExpand)
[`ExpandOrCollapse`](#LuaItemTreeLeaf_ExpandOrCollapse)
[`Expand`](#LuaItemTreeLeaf_Expand)
[`Collapse`](#LuaItemTreeLeaf_Collapse)
[`SetIndent`](#LuaItemTreeLeaf_SetIndent)
[`GetIndent`](#LuaItemTreeLeaf_GetIndent)
[`SetEachIndentWidth`](#LuaItemTreeLeaf_SetEachIndentWidth)
[`GetEachIndentWidth`](#LuaItemTreeLeaf_GetEachIndentWidth)
[`SetNodeIconSize`](#LuaItemTreeLeaf_SetNodeIconSize)
[`SetIconImage`](#LuaItemTreeLeaf_SetIconImage)
[`PtInIcon`](#LuaItemTreeLeaf_PtInIcon)
[`AdjustNodeIconPos`](#LuaItemTreeLeaf_AdjustNodeIconPos)
[`AutoSetIconSize`](#LuaItemTreeLeaf_AutoSetIconSize)
[`SetShowIndex`](#LuaItemTreeLeaf_SetShowIndex)
[`GetShowIndex`](#LuaItemTreeLeaf_GetShowIndex)
[`TreeLeafShow`](#LuaItemTreeLeaf_TreeLeafShow)

* <h4 id="LuaItemTreeLeaf_IsExpand">IsExpand</h4>
Check whether node is expanded.

 > (`bool` bExpand) ItemTreeLeaf:IsExpand()

 ````lua
 local bExpand = ItemTreeLeaf:IsExpand()
 ````

* <h4 id="LuaItemTreeLeaf_ExpandOrCollapse">ExpandOrCollapse</h4>
Toggle expand/collapse.

 > (`void`) ItemTreeLeaf:ExpandOrCollapse()

 ````lua
 ItemTreeLeaf:ExpandOrCollapse()
 ````

* <h4 id="LuaItemTreeLeaf_Expand">Expand</h4>
Expand node.

 > (`void`) ItemTreeLeaf:Expand()

 ````lua
 ItemTreeLeaf:Expand()
 ````

* <h4 id="LuaItemTreeLeaf_Collapse">Collapse</h4>
Collapse node.

 > (`void`) ItemTreeLeaf:Collapse()

 ````lua
 ItemTreeLeaf:Collapse()
 ````

* <h4 id="LuaItemTreeLeaf_SetIndent">SetIndent</h4>
Set indent level.

 > (`void`) ItemTreeLeaf:SetIndent(`number` nIndent)

 ````lua
 ItemTreeLeaf:SetIndent(0)
 ````

* <h4 id="LuaItemTreeLeaf_GetIndent">GetIndent</h4>
Get indent level.

 > (`number` nIndent) ItemTreeLeaf:GetIndent()

 ````lua
 local nIndent = ItemTreeLeaf:GetIndent()
 ````

* <h4 id="LuaItemTreeLeaf_SetEachIndentWidth">SetEachIndentWidth</h4>
Set indent width.

 > (`void`) ItemTreeLeaf:SetEachIndentWidth(`number` fW)

 ````lua
 ItemTreeLeaf:SetEachIndentWidth(16)
 ````

* <h4 id="LuaItemTreeLeaf_GetEachIndentWidth">GetEachIndentWidth</h4>
Get indent width.

 > (`number` fW) ItemTreeLeaf:GetEachIndentWidth()

 ````lua
 local fW = ItemTreeLeaf:GetEachIndentWidth()
 ````

* <h4 id="LuaItemTreeLeaf_SetNodeIconSize">SetNodeIconSize</h4>
Set icon size.

 > (`void`) ItemTreeLeaf:SetNodeIconSize(`number` fW, `number` fH)

 ````lua
 ItemTreeLeaf:SetNodeIconSize(16, 16)
 ````

* <h4 id="LuaItemTreeLeaf_SetIconImage">SetIconImage</h4>
Set icon image and frames.

 > (`void`) ItemTreeLeaf:SetIconImage(`string` szImage, `number` nExpandFrame, `number` nCollapseFrame)

 ````lua
 ItemTreeLeaf:SetIconImage("interface/ui/image/tex.tga", 0, 1)
 ````

* <h4 id="LuaItemTreeLeaf_PtInIcon">PtInIcon</h4>
Test if point is in icon.

`x`/`y` are unscaled values on Lua side; internally they are multiplied by UIScale.

 > (`bool` bInIcon) ItemTreeLeaf:PtInIcon(`number` x, `number` y)

 ````lua
 local bInIcon = ItemTreeLeaf:PtInIcon(100, 100)
 ````

* <h4 id="LuaItemTreeLeaf_AdjustNodeIconPos">AdjustNodeIconPos</h4>
Adjust icon position.

 > (`void`) ItemTreeLeaf:AdjustNodeIconPos()

 ````lua
 ItemTreeLeaf:AdjustNodeIconPos()
 ````

* <h4 id="LuaItemTreeLeaf_AutoSetIconSize">AutoSetIconSize</h4>
Auto set icon size.

 > (`void`) ItemTreeLeaf:AutoSetIconSize()

 ````lua
 ItemTreeLeaf:AutoSetIconSize()
 ````

* <h4 id="LuaItemTreeLeaf_SetShowIndex">SetShowIndex</h4>
Set show index.

 > (`void`) ItemTreeLeaf:SetShowIndex(`number` nShowIndex)

 ````lua
 ItemTreeLeaf:SetShowIndex(0)
 ````

* <h4 id="LuaItemTreeLeaf_GetShowIndex">GetShowIndex</h4>
Get show index.

 > (`number` nShowIndex) ItemTreeLeaf:GetShowIndex()

 ````lua
 local nShowIndex = ItemTreeLeaf:GetShowIndex()
 ````

* <h4 id="LuaItemTreeLeaf_TreeLeafShow">TreeLeafShow</h4>
Show/hide tree leaf.

This takes effect after calling parent `FormatAllItemPos()`.

 > (`void`) ItemTreeLeaf:TreeLeafShow([`bool` bShow = true])

 ````lua
 ItemTreeLeaf:TreeLeafShow(true)
 ItemTreeLeaf:TreeLeafShow(false)
 ````
