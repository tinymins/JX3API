English | [中文](./Achievement.zh-CN.md)

# Achievement Functions

Functions for achievement operations.

## Functions

[`GetAchievementInfo`](#GetAchievementInfo)
[`GetAchievementCount`](#GetAchievementCount)
[`GetAchievementList`](#GetAchievementList)
[`IsAchievementAcquired`](#IsAchievementAcquired)
[`GetAchievementPoint`](#GetAchievementPoint)

---

* <h4 id="GetAchievementInfo">GetAchievementInfo</h4>

Gets achievement information by ID.

 > (`table` tAchievementInfo) GetAchievementInfo(`number` nAchievementID)

* <h4 id="GetAchievementCount">GetAchievementCount</h4>

Gets the total achievement count.

 > (`number` nCount) GetAchievementCount()

* <h4 id="GetAchievementList">GetAchievementList</h4>

Gets the list of achievements.

 > (`table` tAchievementList) GetAchievementList(`number` nCategory)

* <h4 id="IsAchievementAcquired">IsAchievementAcquired</h4>

Checks if an achievement has been acquired.

 > (`boolean` bAcquired) IsAchievementAcquired(`number` nAchievementID)

* <h4 id="GetAchievementPoint">GetAchievementPoint</h4>

Gets the total achievement points.

 > (`number` nPoint) GetAchievementPoint()
