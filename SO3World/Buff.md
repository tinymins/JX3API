English | [中文](./Buff.zh-CN.md)

# Buff Functions

Functions for buff/debuff operations.

## Functions

[`GetBuffName`](#GetBuffName)
[`GetBuffInfo`](#GetBuffInfo)
[`GetBuffDesc`](#GetBuffDesc)
[`GetBuffTip`](#GetBuffTip)
[`GetBuffAttrib`](#GetBuffAttrib)

---

* <h4 id="GetBuffName">GetBuffName</h4>

Gets the name of a buff.

 > (`string` szName) GetBuffName(`number` dwBuffID, `number` nLevel)

* <h4 id="GetBuffInfo">GetBuffInfo</h4>

Gets buff information.

 > (`table` tBuffInfo) GetBuffInfo(`number` dwBuffID, `number` nLevel)

* <h4 id="GetBuffDesc">GetBuffDesc</h4>

Gets the description of a buff.

 > (`string` szDesc) GetBuffDesc(`number` dwBuffID, `number` nLevel)

* <h4 id="GetBuffTip">GetBuffTip</h4>

Gets the tooltip text for a buff.

 > (`string` szTip) GetBuffTip(`number` dwBuffID, `number` nLevel, `table` tExtraInfo)

* <h4 id="GetBuffAttrib">GetBuffAttrib</h4>

Gets buff attributes.

 > (`table` tAttrib) GetBuffAttrib(`number` dwBuffID, `number` nLevel)
