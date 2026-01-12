English | [中文](./Skill.zh-CN.md)

# Skill Functions

Functions for skill operations.

## Functions

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

Gets a skill object by ID and level.

 > ([`KSkill`](./KGameObject/KSkill.md) skill) GetSkill(`number` dwSkillID, `number` nLevel)

* <h4 id="GetSkillName">GetSkillName</h4>

Gets the name of a skill.

 > (`string` szName) GetSkillName(`number` dwSkillID, `number` nLevel)

* <h4 id="GetSkillDesc">GetSkillDesc</h4>

Gets the description of a skill.

 > (`string` szDesc) GetSkillDesc(`number` dwSkillID, `number` nLevel)

* <h4 id="GetSkillTip">GetSkillTip</h4>

Gets the tooltip text for a skill.

 > (`string` szTip) GetSkillTip(`number` dwSkillID, `number` nLevel)

* <h4 id="GetSkillAttrib">GetSkillAttrib</h4>

Gets skill attributes.

 > (`table` tAttrib) GetSkillAttrib(`number` dwSkillID, `number` nLevel)

* <h4 id="GetCDInterval">GetCDInterval</h4>

Gets the cooldown interval for a skill.

 > (`number` nInterval) GetCDInterval(`number` nCDIndex)

* <h4 id="GetCDLeft">GetCDLeft</h4>

Gets the remaining cooldown time for a skill.

 > (`number` nLeft) GetCDLeft(`number` nCDIndex)

* <h4 id="GetGCDLeft">GetGCDLeft</h4>

Gets the remaining global cooldown time.

 > (`number` nLeft) GetGCDLeft()

* <h4 id="IsCDComplete">IsCDComplete</h4>

Checks if a cooldown is complete.

 > (`boolean` bComplete) IsCDComplete(`number` nCDIndex)
