[English](./Camera.md) | 中文

# 镜头函数

镜头控制相关函数。

## 函数

[`Camera.GetRTS`](#Camera_GetRTS)
[`Camera.SetRTS`](#Camera_SetRTS)
[`Camera.GetRTSLookAt`](#Camera_GetRTSLookAt)
[`Camera.SetRTSLookAt`](#Camera_SetRTSLookAt)
[`CameraControl.GetMode`](#CameraControl_GetMode)
[`CameraControl.SetMode`](#CameraControl_SetMode)
[`CameraControl.Enable`](#CameraControl_Enable)

---

* <h4 id="Camera_GetRTS">Camera.GetRTS</h4>

获取镜头的旋转、倾斜和缩放。

 > (`number` nRotation, `number` nTilt, `number` nScale) Camera.GetRTS()

* <h4 id="Camera_SetRTS">Camera.SetRTS</h4>

设置镜头的旋转、倾斜和缩放。

 > (`void`) Camera.SetRTS(`number` nRotation, `number` nTilt, `number` nScale)

* <h4 id="Camera_GetRTSLookAt">Camera.GetRTSLookAt</h4>

获取镜头的注视目标位置。

 > (`number` nX, `number` nY, `number` nZ) Camera.GetRTSLookAt()

* <h4 id="Camera_SetRTSLookAt">Camera.SetRTSLookAt</h4>

设置镜头的注视目标位置。

 > (`void`) Camera.SetRTSLookAt(`number` nX, `number` nY, `number` nZ)

* <h4 id="CameraControl_GetMode">CameraControl.GetMode</h4>

获取镜头控制模式。

 > (`number` nMode) CameraControl.GetMode()

* <h4 id="CameraControl_SetMode">CameraControl.SetMode</h4>

设置镜头控制模式。

 > (`void`) CameraControl.SetMode(`number` nMode)

* <h4 id="CameraControl_Enable">CameraControl.Enable</h4>

启用或禁用镜头控制。

 > (`void`) CameraControl.Enable(`boolean` bEnable)
