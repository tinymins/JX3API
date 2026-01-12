[English](./Achievement.md) | 中文

# 成就函数

成就操作相关函数。

## 函数

[`GetAchievementInfo`](#GetAchievementInfo)
[`GetAchievementCount`](#GetAchievementCount)
[`GetAchievementList`](#GetAchievementList)
[`IsAchievementAcquired`](#IsAchievementAcquired)
[`GetAchievementPoint`](#GetAchievementPoint)

---

* <h4 id="GetAchievementInfo">GetAchievementInfo</h4>

根据 ID 获取成就信息。

 > (`table` tAchievementInfo) GetAchievementInfo(`number` nAchievementID)

* <h4 id="GetAchievementCount">GetAchievementCount</h4>

获取成就总数。

 > (`number` nCount) GetAchievementCount()

* <h4 id="GetAchievementList">GetAchievementList</h4>

获取成就列表。

 > (`table` tAchievementList) GetAchievementList(`number` nCategory)

* <h4 id="IsAchievementAcquired">IsAchievementAcquired</h4>

检查成就是否已获得。

 > (`boolean` bAcquired) IsAchievementAcquired(`number` nAchievementID)

* <h4 id="GetAchievementPoint">GetAchievementPoint</h4>

获取总成就点数。

 > (`number` nPoint) GetAchievementPoint()
