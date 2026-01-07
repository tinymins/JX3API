[English](./ItemTreeLeaf.md) | 中文

# ItemTreeLeaf（树叶节点）

说明：

- `ItemTreeLeaf` 的 metatable 同时包含所有 `ItemHandle` 方法；详见 [KGUI/KItem/ItemHandle.md](./ItemHandle.md)。
- 本文件中与位置/尺寸相关的 API：Lua 侧使用**未缩放的 UI 坐标**；内部会把输入乘以 `Station.GetUIScale()`；对应的 Get* 会再除以 UIScale 后返回。

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
检查节点是否处于展开状态。

 > (`bool` bExpand) ItemTreeLeaf:IsExpand()

 ````lua
 local bExpand = ItemTreeLeaf:IsExpand()
 ````

* <h4 id="LuaItemTreeLeaf_ExpandOrCollapse">ExpandOrCollapse</h4>
在展开/收起之间切换。

 > (`void`) ItemTreeLeaf:ExpandOrCollapse()

 ````lua
 ItemTreeLeaf:ExpandOrCollapse()
 ````

* <h4 id="LuaItemTreeLeaf_Expand">Expand</h4>
展开节点。

 > (`void`) ItemTreeLeaf:Expand()

 ````lua
 ItemTreeLeaf:Expand()
 ````

* <h4 id="LuaItemTreeLeaf_Collapse">Collapse</h4>
收起节点。

 > (`void`) ItemTreeLeaf:Collapse()

 ````lua
 ItemTreeLeaf:Collapse()
 ````

* <h4 id="LuaItemTreeLeaf_SetIndent">SetIndent</h4>
设置indent level。

 > (`void`) ItemTreeLeaf:SetIndent(`number` nIndent)

 ````lua
 ItemTreeLeaf:SetIndent(0)
 ````

* <h4 id="LuaItemTreeLeaf_GetIndent">GetIndent</h4>
获取indent level。

 > (`number` nIndent) ItemTreeLeaf:GetIndent()

 ````lua
 local nIndent = ItemTreeLeaf:GetIndent()
 ````

* <h4 id="LuaItemTreeLeaf_SetEachIndentWidth">SetEachIndentWidth</h4>
设置indent 宽度。

 > (`void`) ItemTreeLeaf:SetEachIndentWidth(`number` fW)

 ````lua
 ItemTreeLeaf:SetEachIndentWidth(16)
 ````

* <h4 id="LuaItemTreeLeaf_GetEachIndentWidth">GetEachIndentWidth</h4>
获取indent 宽度。

 > (`number` fW) ItemTreeLeaf:GetEachIndentWidth()

 ````lua
 local fW = ItemTreeLeaf:GetEachIndentWidth()
 ````

* <h4 id="LuaItemTreeLeaf_SetNodeIconSize">SetNodeIconSize</h4>
设置图标 尺寸。

 > (`void`) ItemTreeLeaf:SetNodeIconSize(`number` fW, `number` fH)

 ````lua
 ItemTreeLeaf:SetNodeIconSize(16, 16)
 ````

* <h4 id="LuaItemTreeLeaf_SetIconImage">SetIconImage</h4>
设置图标图片及帧号。

 > (`void`) ItemTreeLeaf:SetIconImage(`string` szImage, `number` nExpandFrame, `number` nCollapseFrame)

 ````lua
 ItemTreeLeaf:SetIconImage("interface/ui/image/tex.tga", 0, 1)
 ````

* <h4 id="LuaItemTreeLeaf_PtInIcon">PtInIcon</h4>
测试点是否位于图标内。

`x`/`y` 在 Lua 侧为未缩放值；内部会乘以 UIScale。

 > (`bool` bInIcon) ItemTreeLeaf:PtInIcon(`number` x, `number` y)

 ````lua
 local bInIcon = ItemTreeLeaf:PtInIcon(100, 100)
 ````

* <h4 id="LuaItemTreeLeaf_AdjustNodeIconPos">AdjustNodeIconPos</h4>
调整图标位置。

 > (`void`) ItemTreeLeaf:AdjustNodeIconPos()

 ````lua
 ItemTreeLeaf:AdjustNodeIconPos()
 ````

* <h4 id="LuaItemTreeLeaf_AutoSetIconSize">AutoSetIconSize</h4>
自动设置图标 尺寸。

 > (`void`) ItemTreeLeaf:AutoSetIconSize()

 ````lua
 ItemTreeLeaf:AutoSetIconSize()
 ````

* <h4 id="LuaItemTreeLeaf_SetShowIndex">SetShowIndex</h4>
设置show 索引。

 > (`void`) ItemTreeLeaf:SetShowIndex(`number` nShowIndex)

 ````lua
 ItemTreeLeaf:SetShowIndex(0)
 ````

* <h4 id="LuaItemTreeLeaf_GetShowIndex">GetShowIndex</h4>
获取show 索引。

 > (`number` nShowIndex) ItemTreeLeaf:GetShowIndex()

 ````lua
 local nShowIndex = ItemTreeLeaf:GetShowIndex()
 ````

* <h4 id="LuaItemTreeLeaf_TreeLeafShow">TreeLeafShow</h4>
显示/隐藏树叶节点。

该设置在父级调用 `FormatAllItemPos()` 后生效。

 > (`void`) ItemTreeLeaf:TreeLeafShow([`bool` bShow = true])

 ````lua
 ItemTreeLeaf:TreeLeafShow(true)
 ItemTreeLeaf:TreeLeafShow(false)
 ````
