[English](./ItemImage.md) | 中文

# ItemImage（图片）

[`SetFrame`](#LuaItemImage_SetFrame)
[`GetFrame`](#LuaItemImage_GetFrame)
[`AutoSize`](#LuaItemImage_AutoSize)
[`SetImageType`](#LuaItemImage_SetImageType)
[`GetImageType`](#LuaItemImage_GetImageType)
[`SetPercentage`](#LuaItemImage_SetPercentage)
[`GetPercentage`](#LuaItemImage_GetPercentage)
[`SetRotate`](#LuaItemImage_SetRotate)
[`GetRotate`](#LuaItemImage_GetRotate)
[`SetTimeStartAngle`](#LuaItemImage_SetTimeStartAngle)
[`GetImageID`](#LuaItemImage_GetImageID)
[`GetImageInfoID`](#LuaItemImage_GetImageInfoID)
[`GetImagePath`](#LuaItemImage_GetImagePath)
[`IsFromTexturFile`](#LuaItemImage_IsFromTexturFile)
[`FromUITex`](#LuaItemImage_FromUITex)
[`FromTextureFile`](#LuaItemImage_FromTextureFile)
[`FromRemoteFile`](#LuaItemImage_FromRemoteFile)
[`UnloadSource`](#LuaItemImage_UnloadSource)
[`FromScene`](#LuaItemImage_FromScene)
[`FromImageID`](#LuaItemImage_FromImageID)
[`FromIconID`](#LuaItemImage_FromIconID)
[`FromWindow`](#LuaItemImage_FromWindow)
[`FromItem`](#LuaItemImage_FromItem)
[`ToManagedImage`](#LuaItemImage_ToManagedImage)
[`SetPaintOffset`](#LuaItemImage_SetPaintOffset)
[`FromSpecialMiniScene`](#LuaItemImage_FromSpecialMiniScene)
[`SaveImage`](#LuaItemImage_SaveImage)

* <h4 id="LuaItemImage_SetFrame">SetFrame</h4>
设置图片 帧。

 > (`void`) ItemImage:SetFrame(`number` nFrame)

 ````lua
 ItemImage:SetFrame(0)
 ````

* <h4 id="LuaItemImage_GetFrame">GetFrame</h4>
获取current 图片 帧。

 > (`number` nFrame) ItemImage:GetFrame()

 ````lua
 local nFrame = ItemImage:GetFrame()
 ````

* <h4 id="LuaItemImage_AutoSize">AutoSize</h4>
根据当前图片资源自动调整组件尺寸。

 > (`void`) ItemImage:AutoSize()

 ````lua
 ItemImage:AutoSize()
 ````

* <h4 id="LuaItemImage_SetImageType">SetImageType</h4>
设置图片渲染类型。

 > (`void`) ItemImage:SetImageType(`number` nType)

 ````lua
 ItemImage:SetImageType(0)
 ````

* <h4 id="LuaItemImage_GetImageType">GetImageType</h4>
获取图片渲染类型。

 > (`number` nType) ItemImage:GetImageType()

 ````lua
 local nType = ItemImage:GetImageType()
 ````

* <h4 id="LuaItemImage_SetPercentage">SetPercentage</h4>
设置图片百分比（仅对部分图片类型生效，具体由底层渲染方式决定）。

 > (`void`) ItemImage:SetPercentage(`number` fPercentage)

 ````lua
 ItemImage:SetPercentage(1.0)
 ````

* <h4 id="LuaItemImage_GetPercentage">GetPercentage</h4>
获取current 图片 百分比。

 > (`number` fPercentage) ItemImage:GetPercentage()

 ````lua
 local fPercentage = ItemImage:GetPercentage()
 ````

* <h4 id="LuaItemImage_SetRotate">SetRotate</h4>
设置图片 旋转。

 > (`void`) ItemImage:SetRotate(`number` fRotate)

 ````lua
 ItemImage:SetRotate(0)
 ````

* <h4 id="LuaItemImage_GetRotate">GetRotate</h4>
获取图片 旋转。

 > (`number` fRotate) ItemImage:GetRotate()

 ````lua
 local fRotate = ItemImage:GetRotate()
 ````

* <h4 id="LuaItemImage_SetTimeStartAngle">SetTimeStartAngle</h4>
设置计时起始角度（仅对部分图片类型生效，具体由底层渲染方式决定）。

 > (`void`) ItemImage:SetTimeStartAngle(`number` fAngle)

 ````lua
 ItemImage:SetTimeStartAngle(0)
 ````

* <h4 id="LuaItemImage_GetImageID">GetImageID</h4>
获取current 图片 id。

 > (`number` dwImageID) ItemImage:GetImageID()

 ````lua
 local dwImageID = ItemImage:GetImageID()
 ````

* <h4 id="LuaItemImage_GetImageInfoID">GetImageInfoID</h4>
获取current 图片 info id。

 > (`number` dwImageInfoID) ItemImage:GetImageInfoID()

 ````lua
 local dwImageInfoID = ItemImage:GetImageInfoID()
 ````

* <h4 id="LuaItemImage_GetImagePath">GetImagePath</h4>
获取current 图片 路径。

如果当前帧号 >= 0，则也会一并返回帧号。

 > (`string` szPath[, `number` nFrame]) ItemImage:GetImagePath()

 ````lua
 local szPath = ItemImage:GetImagePath()
 local szPath, nFrame = ItemImage:GetImagePath()
 ````

* <h4 id="LuaItemImage_IsFromTexturFile">IsFromTexturFile</h4>
当前图片来源是否为纹理文件。

 > (`bool` bIsFromTextureFile) ItemImage:IsFromTexturFile()

 ````lua
 local bIsFromTextureFile = ItemImage:IsFromTexturFile()
 ````

* <h4 id="LuaItemImage_FromUITex">FromUITex</h4>
从 UI 纹理加载图片（带帧号）。

 > (`void`) ItemImage:FromUITex(`string` szImage, `number` nFrame)

 ````lua
 ItemImage:FromUITex("interface/ui/image/ui_tex.tga", 0)
 ````

* <h4 id="LuaItemImage_FromTextureFile">FromTextureFile</h4>
从纹理文件加载图片。

 > (`void`) ItemImage:FromTextureFile(`string` szImage[, `bool` bCache])

 ````lua
 ItemImage:FromTextureFile("interface/ui/image/tex.tga")
 ItemImage:FromTextureFile("interface/ui/image/tex.tga", true)
 ````

* <h4 id="LuaItemImage_FromRemoteFile">FromRemoteFile</h4>
从远程 URL 加载图片。

该调用会转发到 Lua 全局处理函数 `__OnKItemImage_LoadRemoteFile(ItemImage, url, cache, callback)`。

 > (`void`) ItemImage:FromRemoteFile(`string` szUrl[, `bool` bCache[, `function` fnCallback]])

 ````lua
 ItemImage:FromRemoteFile("https://example.com/a.png")
 ItemImage:FromRemoteFile("https://example.com/a.png", true)
 ItemImage:FromRemoteFile("https://example.com/a.png", true, function(bOk)
     -- 回调由 __OnKItemImage_LoadRemoteFile 处理
 end)
 ````

* <h4 id="LuaItemImage_UnloadSource">UnloadSource</h4>
卸载当前图片来源。

 > (`void`) ItemImage:UnloadSource()

 ````lua
 ItemImage:UnloadSource()
 ````

* <h4 id="LuaItemImage_FromScene">FromScene</h4>
从场景抓取图像。

实际绑定会对 `sceneId` 调用 `ToIKG3DObjID()`。

 > (`void`) ItemImage:FromScene(`userdata|number` sceneId)

 ````lua
 ItemImage:FromScene(Scene)
 ````

* <h4 id="LuaItemImage_FromImageID">FromImageID</h4>
按 image id 加载。

 > (`void`) ItemImage:FromImageID(`number` dwImageID)

 ````lua
 ItemImage:FromImageID(123)
 ````

* <h4 id="LuaItemImage_FromIconID">FromIconID</h4>
按 icon id 加载。

 > (`void`) ItemImage:FromIconID(`number` nIconID)

 ````lua
 ItemImage:FromIconID(123)
 ````

* <h4 id="LuaItemImage_FromWindow">FromWindow</h4>
从窗口抓取图像。

 > (`void`) ItemImage:FromWindow(`WndWindow` WndWindow)

 ````lua
 ItemImage:FromWindow(WndWindow)
 ````

* <h4 id="LuaItemImage_FromItem">FromItem</h4>
从另一个组件抓取图像。

 > (`void`) ItemImage:FromItem(`ItemNull` Item)

 ````lua
 ItemImage:FromItem(ItemNull)
 ````

* <h4 id="LuaItemImage_ToManagedImage">ToManagedImage</h4>
转换为托管图片（managed image）。

 > (`void`) ItemImage:ToManagedImage()

 ````lua
 ItemImage:ToManagedImage()
 ````

* <h4 id="LuaItemImage_SetPaintOffset">SetPaintOffset</h4>
按索引设置绘制偏移（百分比值）。

 > (`void`) ItemImage:SetPaintOffset(`number` nIndex, `number` fPercentX, `number` fPercentY)

 ````lua
 ItemImage:SetPaintOffset(0, 0.5, 0.5)
 ````

* <h4 id="LuaItemImage_FromSpecialMiniScene">FromSpecialMiniScene</h4>
从特殊 mini scene（小场景）抓取图像。

 > (`void`) ItemImage:FromSpecialMiniScene(`userdata|number` sceneId, `string` szImageFile, `number` nUid)

 ````lua
 ItemImage:FromSpecialMiniScene(Scene, "interface/ui/image/out.png", 1)
 ````

* <h4 id="LuaItemImage_SaveImage">SaveImage</h4>
将当前图片保存到文件。

 > (`void`) ItemImage:SaveImage(`string` szImageFile)

 ````lua
 ItemImage:SaveImage("interface/ui/image/out.png")
 ````
