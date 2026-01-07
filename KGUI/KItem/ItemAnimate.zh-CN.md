[English](./ItemAnimate.md) | 中文

# ItemAnimate（动画）

[`SetGroup`](#LuaItemAnimate_SetGroup)
[`SetLoopCount`](#LuaItemAnimate_SetLoopCount)
[`SetImagePath`](#LuaItemAnimate_SetImagePath)
[`SetAnimate`](#LuaItemAnimate_SetAnimate)
[`AutoSize`](#LuaItemAnimate_AutoSize)
[`Replay`](#LuaItemAnimate_Replay)
[`SetIdenticalInterval`](#LuaItemAnimate_SetIdenticalInterval)
[`SetInterval`](#LuaItemAnimate_SetInterval)
[`IsFinished`](#LuaItemAnimate_IsFinished)
[`SetAnimateType`](#LuaItemAnimate_SetAnimateType)
[`SetPercentage`](#LuaItemAnimate_SetPercentage)
[`SetFrame`](#LuaItemAnimate_SetFrame)
[`EnableReverse`](#LuaItemAnimate_EnableReverse)
[`IsReverse`](#LuaItemAnimate_IsReverse)

* <h4 id="LuaItemAnimate_SetGroup">SetGroup</h4>
设置动画 group。

如果 `nGroup < 0`，则会被设置为 `-1`。

 > (`void`) ItemAnimate:SetGroup(`number` nGroup)

 ````lua
 ItemAnimate:SetGroup(0)
 ````

* <h4 id="LuaItemAnimate_SetLoopCount">SetLoopCount</h4>
设置循环次数。

该值会原样传入底层；负数的含义由底层解释（常见用法是 `-1` 表示无限循环）。

 > (`void`) ItemAnimate:SetLoopCount(`number` nLoopCount)

 ````lua
 ItemAnimate:SetLoopCount(-1)
 ````

* <h4 id="LuaItemAnimate_SetImagePath">SetImagePath</h4>
设置动画使用的图片路径。

`szImage` 会经过 `FormatFilePath()` 处理后再传入底层。

 > (`void`) ItemAnimate:SetImagePath(`string` szImage)

 ````lua
 ItemAnimate:SetImagePath("interface/ui/ani/ani.tga")
 ````

* <h4 id="LuaItemAnimate_SetAnimate">SetAnimate</h4>
设置动画资源：图片路径 + group，并可选设置循环次数与动画类型。

`szImage` 会经过 `FormatFilePath()` 处理后再传入底层。

参数个数必须为 3/4/5，否则会报错。

 > (`void`) ItemAnimate:SetAnimate(`string` szImage, `number` nGroup[, `number` nLoopCount = -1[, `number` nAnimateType = ITEMANIMATE_NORMAL]])

 ````lua
 ItemAnimate:SetAnimate("interface/ui/ani/ani.tga", 0)
 ItemAnimate:SetAnimate("interface/ui/ani/ani.tga", 0, -1)
 ItemAnimate:SetAnimate("interface/ui/ani/ani.tga", 0, -1, 0)
 ````

* <h4 id="LuaItemAnimate_AutoSize">AutoSize</h4>
根据当前动画资源自动调整组件尺寸。

 > (`void`) ItemAnimate:AutoSize()

 ````lua
 ItemAnimate:AutoSize()
 ````

* <h4 id="LuaItemAnimate_Replay">Replay</h4>
从头重新播放当前动画。

 > (`void`) ItemAnimate:Replay()

 ````lua
 ItemAnimate:Replay()
 ````

* <h4 id="LuaItemAnimate_SetIdenticalInterval">SetIdenticalInterval</h4>
设置所有帧使用相同的间隔。

如果底层设置失败，会报错且不返回值。

 > (`void`) ItemAnimate:SetIdenticalInterval(`number` nValue)

 ````lua
 ItemAnimate:SetIdenticalInterval(33)
 ````

* <h4 id="LuaItemAnimate_SetInterval">SetInterval</h4>
按 group 帧设置间隔。

如果底层设置失败，会报错且不返回值。

 > (`void`) ItemAnimate:SetInterval(`number` nGroupFrame, `number` nValue)

 ````lua
 ItemAnimate:SetInterval(0, 33)
 ````

* <h4 id="LuaItemAnimate_IsFinished">IsFinished</h4>
判断动画是否播放完成。

 > (`bool` bFinished) ItemAnimate:IsFinished()

 ````lua
 local bFinished = ItemAnimate:IsFinished()
 ````

* <h4 id="LuaItemAnimate_SetAnimateType">SetAnimateType</h4>
设置动画类型。

如果底层设置失败，会报错且不返回值。

 > (`void`) ItemAnimate:SetAnimateType(`number` nAnimateType)

 ````lua
 ItemAnimate:SetAnimateType(0)
 ````

* <h4 id="LuaItemAnimate_SetPercentage">SetPercentage</h4>
设置动画进度百分比。

如果底层设置失败，会报错且不返回值。

 > (`void`) ItemAnimate:SetPercentage(`number` fPercentage)

 ````lua
 ItemAnimate:SetPercentage(0.5)
 ````

* <h4 id="LuaItemAnimate_SetFrame">SetFrame</h4>
设置当前帧。

如果底层设置失败，会报错且不返回值。

 > (`void`) ItemAnimate:SetFrame(`number` nFrame)

 ````lua
 ItemAnimate:SetFrame(0)
 ````

* <h4 id="LuaItemAnimate_EnableReverse">EnableReverse</h4>
启用/禁用倒放。

 > (`void`) ItemAnimate:EnableReverse(`bool` bReverse)

 ````lua
 ItemAnimate:EnableReverse(true)
 ````

* <h4 id="LuaItemAnimate_IsReverse">IsReverse</h4>
获取是否启用了倒放。

 > (`bool` bReverse) ItemAnimate:IsReverse()

 ````lua
 local bReverse = ItemAnimate:IsReverse()
 ````
