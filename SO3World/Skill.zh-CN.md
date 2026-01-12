[English](./Skill.md) | 中文

# 技能函数

技能操作相关函数。

## 函数

[`GetSkill`](#GetSkill)
[`GetSkillName`](#GetSkillName)
[`GetSkillDesc`](#GetSkillDesc)
[`GetSkillTip`](#GetSkillTip)
[`GetSkillAttrib`](#GetSkillAttrib)
[`GetCDInterval`](#GetCDInterval)
[`GetCDLeft`](#GetCDLeft)
[`GetGCDLeft`](#GetGCDLeft)
[`IsCDComplete`](#IsCDComplete)

---

* <h4 id="GetSkill">GetSkill</h4>

根据 ID 和等级获取技能对象。

 > ([`KSkill`](./KGameObject/KSkill.zh-CN.md) skill) GetSkill(`number` dwSkillID, `number` nLevel)

* <h4 id="GetSkillName">GetSkillName</h4>

获取技能名称。

 > (`string` szName) GetSkillName(`number` dwSkillID, `number` nLevel)

* <h4 id="GetSkillDesc">GetSkillDesc</h4>

获取技能描述。

 > (`string` szDesc) GetSkillDesc(`number` dwSkillID, `number` nLevel)

* <h4 id="GetSkillTip">GetSkillTip</h4>

获取技能提示文本。

 > (`string` szTip) GetSkillTip(`number` dwSkillID, `number` nLevel)

* <h4 id="GetSkillAttrib">GetSkillAttrib</h4>

获取技能属性。

 > (`table` tAttrib) GetSkillAttrib(`number` dwSkillID, `number` nLevel)

* <h4 id="GetCDInterval">GetCDInterval</h4>

获取技能的冷却间隔。

 > (`number` nInterval) GetCDInterval(`number` nCDIndex)

* <h4 id="GetCDLeft">GetCDLeft</h4>

获取技能的剩余冷却时间。

 > (`number` nLeft) GetCDLeft(`number` nCDIndex)

* <h4 id="GetGCDLeft">GetGCDLeft</h4>

获取剩余的全局冷却时间。

 > (`number` nLeft) GetGCDLeft()

* <h4 id="IsCDComplete">IsCDComplete</h4>

检查冷却是否完成。

 > (`boolean` bComplete) IsCDComplete(`number` nCDIndex)
