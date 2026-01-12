English | [中文](./Camera.zh-CN.md)

# Camera Functions

Functions for camera control.

## Functions

[`Camera.GetRTS`](#Camera_GetRTS)
[`Camera.SetRTS`](#Camera_SetRTS)
[`Camera.GetRTSLookAt`](#Camera_GetRTSLookAt)
[`Camera.SetRTSLookAt`](#Camera_SetRTSLookAt)
[`CameraControl.GetMode`](#CameraControl_GetMode)
[`CameraControl.SetMode`](#CameraControl_SetMode)
[`CameraControl.Enable`](#CameraControl_Enable)

---

* <h4 id="Camera_GetRTS">Camera.GetRTS</h4>

Gets the camera rotation, tilt, and scale.

 > (`number` nRotation, `number` nTilt, `number` nScale) Camera.GetRTS()

* <h4 id="Camera_SetRTS">Camera.SetRTS</h4>

Sets the camera rotation, tilt, and scale.

 > (`void`) Camera.SetRTS(`number` nRotation, `number` nTilt, `number` nScale)

* <h4 id="Camera_GetRTSLookAt">Camera.GetRTSLookAt</h4>

Gets the camera look-at target position.

 > (`number` nX, `number` nY, `number` nZ) Camera.GetRTSLookAt()

* <h4 id="Camera_SetRTSLookAt">Camera.SetRTSLookAt</h4>

Sets the camera look-at target position.

 > (`void`) Camera.SetRTSLookAt(`number` nX, `number` nY, `number` nZ)

* <h4 id="CameraControl_GetMode">CameraControl.GetMode</h4>

Gets the camera control mode.

 > (`number` nMode) CameraControl.GetMode()

* <h4 id="CameraControl_SetMode">CameraControl.SetMode</h4>

Sets the camera control mode.

 > (`void`) CameraControl.SetMode(`number` nMode)

* <h4 id="CameraControl_Enable">CameraControl.Enable</h4>

Enables or disables camera control.

 > (`void`) CameraControl.Enable(`boolean` bEnable)
