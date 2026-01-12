# 表格查询函数

用于从游戏数据表中查询信息的函数。这些函数提供对物品、技能、Buff、NPC 和地图信息的访问。

---

## 物品表函数

### Table_GetItemIconID {#Table_GetItemIconID}

获取物品图标 ID。

```lua
local nIconID = Table_GetItemIconID(nUIID)
```

### Table_GetItemName {#Table_GetItemName}

获取物品名称。

```lua
local szName = Table_GetItemName(nUIID)
```

### Table_GetItemDesc {#Table_GetItemDesc}

获取物品描述。

```lua
local szDesc = Table_GetItemDesc(nUIID)
```

---

## 技能表函数

### Table_GetSkill {#Table_GetSkill}

获取技能数据。

```lua
local tSkill = Table_GetSkill(dwSkillID, nLevel)
```

### Table_GetSkillIconID {#Table_GetSkillIconID}

获取技能图标 ID。

```lua
local nIconID = Table_GetSkillIconID(dwSkillID, nLevel)
```

### Table_GetSkillName {#Table_GetSkillName}

获取技能名称。

```lua
local szName = Table_GetSkillName(dwSkillID, nLevel)
```

### Table_GetSkillDesc {#Table_GetSkillDesc}

获取技能描述。

```lua
local szDesc = Table_GetSkillDesc(dwSkillID, nLevel)
```

### Table_GetSkillShortDesc {#Table_GetSkillShortDesc}

获取技能简短描述。

```lua
local szDesc = Table_GetSkillShortDesc(dwSkillID, nLevel)
```

### Table_GetSkillSpecialDesc {#Table_GetSkillSpecialDesc}

获取技能特殊描述。

```lua
local szDesc = Table_GetSkillSpecialDesc(dwSkillID, nLevel)
```

### Table_GetSkillSchoolName {#Table_GetSkillSchoolName}

获取技能门派名称。

```lua
local szSchool = Table_GetSkillSchoolName(dwSkillID)
```

### Table_GetSkillSchoolIconID {#Table_GetSkillSchoolIconID}

获取技能门派图标 ID。

```lua
local nIconID = Table_GetSkillSchoolIconID(dwSkillID)
```

### Table_GetSkillSortOrder {#Table_GetSkillSortOrder}

获取技能排序顺序。

```lua
local nOrder = Table_GetSkillSortOrder(dwSkillID)
```

### Table_IsSkillShow {#Table_IsSkillShow}

检查技能是否应该显示。

```lua
local bShow = Table_IsSkillShow(dwSkillID, nLevel)
```

### Table_IsSkillCombatShow {#Table_IsSkillCombatShow}

检查技能是否应该在战斗中显示。

```lua
local bShow = Table_IsSkillCombatShow(dwSkillID, nLevel)
```

### Table_IsSkillFormation {#Table_IsSkillFormation}

检查技能是否是阵法技能。

```lua
local bFormation = Table_IsSkillFormation(dwSkillID)
```

### Table_IsSkillFormationCaster {#Table_IsSkillFormationCaster}

检查技能是否是阵法施放技能。

```lua
local bCaster = Table_IsSkillFormationCaster(dwSkillID)
```

### Table_GetSkillPracticeID {#Table_GetSkillPracticeID}

获取技能的修炼 ID。

```lua
local dwPracticeID = Table_GetSkillPracticeID(dwSkillID)
```

### Table_GetLearnSkillInfo {#Table_GetLearnSkillInfo}

获取技能学习信息。

```lua
local tInfo = Table_GetLearnSkillInfo(dwSkillID, nLevel)
```

---

## 技能秘籍函数

### Table_GetSkillRecipe {#Table_GetSkillRecipe}

获取技能秘籍数据。

```lua
local tRecipe = Table_GetSkillRecipe(dwRecipeID)
```

### Table_GetRecipeList {#Table_GetRecipeList}

获取某生活技能的配方列表。

```lua
local tList = Table_GetRecipeList(dwProfessionID)
```

---

## Buff 表函数

### Table_GetBuff {#Table_GetBuff}

获取 Buff 数据。

```lua
local tBuff = Table_GetBuff(dwBuffID, nLevel)
```

### Table_GetBuffIconID {#Table_GetBuffIconID}

获取 Buff 图标 ID。

```lua
local nIconID = Table_GetBuffIconID(dwBuffID, nLevel)
```

### Table_GetBuffName {#Table_GetBuffName}

获取 Buff 名称。

```lua
local szName = Table_GetBuffName(dwBuffID, nLevel)
```

### Table_GetBuffDesc {#Table_GetBuffDesc}

获取 Buff 描述。

```lua
local szDesc = Table_GetBuffDesc(dwBuffID, nLevel)
```

### Table_BuffNeedSparking {#Table_BuffNeedSparking}

检查 Buff 是否需要闪烁效果。

```lua
local bSpark = Table_BuffNeedSparking(dwBuffID)
```

### Table_BuffNeedShowTime {#Table_BuffNeedShowTime}

检查 Buff 是否应该显示剩余时间。

```lua
local bShowTime = Table_BuffNeedShowTime(dwBuffID)
```

### Table_BuffNeedShow {#Table_BuffNeedShow}

检查 Buff 是否应该显示。

```lua
local bShow = Table_BuffNeedShow(dwBuffID)
```

### Table_BuffIsVisible {#Table_BuffIsVisible}

检查 Buff 是否可见。

```lua
local bVisible = Table_BuffIsVisible(dwBuffID, nLevel)
```

---

## NPC/交互物件表函数

### Table_GetNpcTemplateName {#Table_GetNpcTemplateName}

获取 NPC 模板名称。

```lua
local szName = Table_GetNpcTemplateName(dwTemplateID)
```

### Table_GetDoodadTemplateName {#Table_GetDoodadTemplateName}

获取交互物件模板名称。

```lua
local szName = Table_GetDoodadTemplateName(dwTemplateID)
```

### Table_IsShieldedNpc {#Table_IsShieldedNpc}

检查 NPC 是否被屏蔽（隐藏）。

```lua
local bShielded = Table_IsShieldedNpc(dwTemplateID)
```

### Table_GetBoss {#Table_GetBoss}

获取 Boss 信息。

```lua
local tBoss = Table_GetBoss(dwBossID)
```

### Table_GetCDProcessBoss {#Table_GetCDProcessBoss}

获取 CD 进度 Boss 信息。

```lua
local tBoss = Table_GetCDProcessBoss(dwMapID)
```

---

## 地图表函数

### Table_GetMapName {#Table_GetMapName}

获取地图名称。

```lua
local szName = Table_GetMapName(dwMapID)
```

### Table_IsTreasureBattleFieldMap {#Table_IsTreasureBattleFieldMap}

检查地图是否是夺宝战场。

```lua
local bTreasure = Table_IsTreasureBattleFieldMap(dwMapID)
```

### Table_IsZombieBattleFieldMap {#Table_IsZombieBattleFieldMap}

检查地图是否是僵尸战场。

```lua
local bZombie = Table_IsZombieBattleFieldMap(dwMapID)
```

### Table_IsMobaBattleFieldMap {#Table_IsMobaBattleFieldMap}

检查地图是否是 MOBA 战场。

```lua
local bMoba = Table_IsMobaBattleFieldMap(dwMapID)
```

---

## 门派/心法函数

### Table_GetForceImageName {#Table_GetForceImageName}

获取门派图片名称。

```lua
local szImage = Table_GetForceImageName(nForceID)
```

### Table_SchoolToForce {#Table_SchoolToForce}

将门派 ID 转换为势力 ID。

```lua
local nForceID = Table_SchoolToForce(nSchoolID)
```

### Table_ForceToSchool {#Table_ForceToSchool}

将势力 ID 转换为门派 ID。

```lua
local nSchoolID = Table_ForceToSchool(nForceID)
```

### Table_GetMKungfuBg {#Table_GetMKungfuBg}

获取心法背景图。

```lua
local szBg = Table_GetMKungfuBg(dwKungfuID)
```

### Table_GetMKungfuList {#Table_GetMKungfuList}

获取心法列表。

```lua
local tList = Table_GetMKungfuList(nForceID)
```

### Table_GetKungfuSkillList {#Table_GetKungfuSkillList}

获取心法技能列表。

```lua
local tList = Table_GetKungfuSkillList(dwKungfuID)
```

---

## 宠物函数

### Table_GetPetSkill {#Table_GetPetSkill}

获取宠物技能数据。

```lua
local tSkill = Table_GetPetSkill(dwPetSkillID)
```

### Table_GetPetAvatar {#Table_GetPetAvatar}

获取宠物外观数据。

```lua
local tAvatar = Table_GetPetAvatar(dwPetID)
```

---

## 其他函数

### Table_GetQuestPoint {#Table_GetQuestPoint}

获取任务点数据。

```lua
local tPoint = Table_GetQuestPoint(dwQuestID)
```

### Table_GetMagicAttributeInfo {#Table_GetMagicAttributeInfo}

获取魔法属性信息。

```lua
local tInfo = Table_GetMagicAttributeInfo(nAttributeID)
```

### Table_GetComboSkillInfo {#Table_GetComboSkillInfo}

获取连招技能信息。

```lua
local tInfo = Table_GetComboSkillInfo(dwSkillID)
```

### Table_OpenSkillLevel {#Table_OpenSkillLevel}

获取技能开放等级要求。

```lua
local nLevel = Table_OpenSkillLevel(dwSkillID)
```

### Table_GetSkillTeach {#Table_GetSkillTeach}

获取技能教学信息。

```lua
local tTeach = Table_GetSkillTeach(dwSkillID)
```

### Table_GetSkillTeachQixueRecommend {#Table_GetSkillTeachQixueRecommend}

获取技能推荐奇穴。

```lua
local tRecommend = Table_GetSkillTeachQixueRecommend(dwSkillID)
```

### Table_GetGuideSoultion {#Table_GetGuideSoultion}

获取引导方案数据。

```lua
local tSolution = Table_GetGuideSoultion(dwGuideID)
```

---

## 使用示例

```lua
-- 获取技能信息用于显示
function ShowSkillInfo(dwSkillID, nLevel)
    local szName = Table_GetSkillName(dwSkillID, nLevel)
    local szDesc = Table_GetSkillDesc(dwSkillID, nLevel)
    local nIconID = Table_GetSkillIconID(dwSkillID, nLevel)

    Output("技能：" .. szName)
    Output("描述：" .. szDesc)
end

-- 获取 Buff 信息
function ShowBuffInfo(dwBuffID, nLevel)
    local szName = Table_GetBuffName(dwBuffID, nLevel)
    local bVisible = Table_BuffIsVisible(dwBuffID, nLevel)

    if bVisible then
        Output("Buff：" .. szName)
    end
end

-- 检查地图类型
function GetMapType(dwMapID)
    if Table_IsTreasureBattleFieldMap(dwMapID) then
        return "夺宝战场"
    elseif Table_IsZombieBattleFieldMap(dwMapID) then
        return "僵尸战场"
    elseif Table_IsMobaBattleFieldMap(dwMapID) then
        return "MOBA 战场"
    end
    return Table_GetMapName(dwMapID)
end
```

---

## 相关链接

- [表格文件操作](./Table.zh-CN.md) - Tab 文件操作
- [常量](./Constants-Skill.zh-CN.md) - 技能常量
