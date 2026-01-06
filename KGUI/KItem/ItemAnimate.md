# ItemAnimate

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
Set animation group.

If `nGroup < 0`, it will be set to `-1`.

 > (`void`) ItemAnimate:SetGroup(`number` nGroup)

 ````lua
 ItemAnimate:SetGroup(0)
 ````

* <h4 id="LuaItemAnimate_SetLoopCount">SetLoopCount</h4>
Set loop count.

 > (`void`) ItemAnimate:SetLoopCount(`number` nLoopCount)

 ````lua
 ItemAnimate:SetLoopCount(-1)
 ````

* <h4 id="LuaItemAnimate_SetImagePath">SetImagePath</h4>
Set image path.

 > (`void`) ItemAnimate:SetImagePath(`string` szImage)

 ````lua
 ItemAnimate:SetImagePath("interface/ui/ani/ani.tga")
 ````

* <h4 id="LuaItemAnimate_SetAnimate">SetAnimate</h4>
Set animate with image path and group.

 > (`void`) ItemAnimate:SetAnimate(`string` szImage, `number` nGroup[, `number` nLoopCount = -1[, `number` nAnimateType = ITEMANIMATE_NORMAL]])

 ````lua
 ItemAnimate:SetAnimate("interface/ui/ani/ani.tga", 0)
 ItemAnimate:SetAnimate("interface/ui/ani/ani.tga", 0, -1)
 ItemAnimate:SetAnimate("interface/ui/ani/ani.tga", 0, -1, 0)
 ````

* <h4 id="LuaItemAnimate_AutoSize">AutoSize</h4>
Auto size item by current animation.

 > (`void`) ItemAnimate:AutoSize()

 ````lua
 ItemAnimate:AutoSize()
 ````

* <h4 id="LuaItemAnimate_Replay">Replay</h4>
Replay animation.

 > (`void`) ItemAnimate:Replay()

 ````lua
 ItemAnimate:Replay()
 ````

* <h4 id="LuaItemAnimate_SetIdenticalInterval">SetIdenticalInterval</h4>
Set identical interval.

 > (`void`) ItemAnimate:SetIdenticalInterval(`number` nValue)

 ````lua
 ItemAnimate:SetIdenticalInterval(33)
 ````

* <h4 id="LuaItemAnimate_SetInterval">SetInterval</h4>
Set interval by group frame.

 > (`void`) ItemAnimate:SetInterval(`number` nGroupFrame, `number` nValue)

 ````lua
 ItemAnimate:SetInterval(0, 33)
 ````

* <h4 id="LuaItemAnimate_IsFinished">IsFinished</h4>
Check whether animation is finished.

 > (`bool` bFinished) ItemAnimate:IsFinished()

 ````lua
 local bFinished = ItemAnimate:IsFinished()
 ````

* <h4 id="LuaItemAnimate_SetAnimateType">SetAnimateType</h4>
Set animate type.

 > (`void`) ItemAnimate:SetAnimateType(`number` nAnimateType)

 ````lua
 ItemAnimate:SetAnimateType(0)
 ````

* <h4 id="LuaItemAnimate_SetPercentage">SetPercentage</h4>
Set animation progress percentage.

 > (`void`) ItemAnimate:SetPercentage(`number` fPercentage)

 ````lua
 ItemAnimate:SetPercentage(0.5)
 ````

* <h4 id="LuaItemAnimate_SetFrame">SetFrame</h4>
Set current frame.

 > (`void`) ItemAnimate:SetFrame(`number` nFrame)

 ````lua
 ItemAnimate:SetFrame(0)
 ````

* <h4 id="LuaItemAnimate_EnableReverse">EnableReverse</h4>
Enable/disable reverse.

 > (`void`) ItemAnimate:EnableReverse(`bool` bReverse)

 ````lua
 ItemAnimate:EnableReverse(true)
 ````

* <h4 id="LuaItemAnimate_IsReverse">IsReverse</h4>
Check whether reverse is enabled.

 > (`bool` bReverse) ItemAnimate:IsReverse()

 ````lua
 local bReverse = ItemAnimate:IsReverse()
 ````
