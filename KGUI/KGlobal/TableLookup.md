# Table Lookup Functions

Functions for looking up game data from tables. These functions provide access to item, skill, buff, NPC, and map information.

---

## Item Table Functions

### Table_GetItemIconID {#Table_GetItemIconID}

Get item icon ID.

```lua
local nIconID = Table_GetItemIconID(nUIID)
```

### Table_GetItemName {#Table_GetItemName}

Get item name.

```lua
local szName = Table_GetItemName(nUIID)
```

### Table_GetItemDesc {#Table_GetItemDesc}

Get item description.

```lua
local szDesc = Table_GetItemDesc(nUIID)
```

---

## Skill Table Functions

### Table_GetSkill {#Table_GetSkill}

Get skill data.

```lua
local tSkill = Table_GetSkill(dwSkillID, nLevel)
```

### Table_GetSkillIconID {#Table_GetSkillIconID}

Get skill icon ID.

```lua
local nIconID = Table_GetSkillIconID(dwSkillID, nLevel)
```

### Table_GetSkillName {#Table_GetSkillName}

Get skill name.

```lua
local szName = Table_GetSkillName(dwSkillID, nLevel)
```

### Table_GetSkillDesc {#Table_GetSkillDesc}

Get skill description.

```lua
local szDesc = Table_GetSkillDesc(dwSkillID, nLevel)
```

### Table_GetSkillShortDesc {#Table_GetSkillShortDesc}

Get skill short description.

```lua
local szDesc = Table_GetSkillShortDesc(dwSkillID, nLevel)
```

### Table_GetSkillSpecialDesc {#Table_GetSkillSpecialDesc}

Get skill special description.

```lua
local szDesc = Table_GetSkillSpecialDesc(dwSkillID, nLevel)
```

### Table_GetSkillSchoolName {#Table_GetSkillSchoolName}

Get skill school name.

```lua
local szSchool = Table_GetSkillSchoolName(dwSkillID)
```

### Table_GetSkillSchoolIconID {#Table_GetSkillSchoolIconID}

Get skill school icon ID.

```lua
local nIconID = Table_GetSkillSchoolIconID(dwSkillID)
```

### Table_GetSkillSortOrder {#Table_GetSkillSortOrder}

Get skill sort order for display.

```lua
local nOrder = Table_GetSkillSortOrder(dwSkillID)
```

### Table_IsSkillShow {#Table_IsSkillShow}

Check if skill should be shown.

```lua
local bShow = Table_IsSkillShow(dwSkillID, nLevel)
```

### Table_IsSkillCombatShow {#Table_IsSkillCombatShow}

Check if skill should be shown in combat.

```lua
local bShow = Table_IsSkillCombatShow(dwSkillID, nLevel)
```

### Table_IsSkillFormation {#Table_IsSkillFormation}

Check if skill is a formation skill.

```lua
local bFormation = Table_IsSkillFormation(dwSkillID)
```

### Table_IsSkillFormationCaster {#Table_IsSkillFormationCaster}

Check if skill is a formation caster skill.

```lua
local bCaster = Table_IsSkillFormationCaster(dwSkillID)
```

### Table_GetSkillPracticeID {#Table_GetSkillPracticeID}

Get practice ID for skill.

```lua
local dwPracticeID = Table_GetSkillPracticeID(dwSkillID)
```

### Table_GetLearnSkillInfo {#Table_GetLearnSkillInfo}

Get skill learning information.

```lua
local tInfo = Table_GetLearnSkillInfo(dwSkillID, nLevel)
```

---

## Skill Recipe Functions

### Table_GetSkillRecipe {#Table_GetSkillRecipe}

Get skill recipe data.

```lua
local tRecipe = Table_GetSkillRecipe(dwRecipeID)
```

### Table_GetRecipeList {#Table_GetRecipeList}

Get list of recipes for a profession.

```lua
local tList = Table_GetRecipeList(dwProfessionID)
```

---

## Buff Table Functions

### Table_GetBuff {#Table_GetBuff}

Get buff data.

```lua
local tBuff = Table_GetBuff(dwBuffID, nLevel)
```

### Table_GetBuffIconID {#Table_GetBuffIconID}

Get buff icon ID.

```lua
local nIconID = Table_GetBuffIconID(dwBuffID, nLevel)
```

### Table_GetBuffName {#Table_GetBuffName}

Get buff name.

```lua
local szName = Table_GetBuffName(dwBuffID, nLevel)
```

### Table_GetBuffDesc {#Table_GetBuffDesc}

Get buff description.

```lua
local szDesc = Table_GetBuffDesc(dwBuffID, nLevel)
```

### Table_BuffNeedSparking {#Table_BuffNeedSparking}

Check if buff needs sparking effect.

```lua
local bSpark = Table_BuffNeedSparking(dwBuffID)
```

### Table_BuffNeedShowTime {#Table_BuffNeedShowTime}

Check if buff should show remaining time.

```lua
local bShowTime = Table_BuffNeedShowTime(dwBuffID)
```

### Table_BuffNeedShow {#Table_BuffNeedShow}

Check if buff should be displayed.

```lua
local bShow = Table_BuffNeedShow(dwBuffID)
```

### Table_BuffIsVisible {#Table_BuffIsVisible}

Check if buff is visible.

```lua
local bVisible = Table_BuffIsVisible(dwBuffID, nLevel)
```

---

## NPC/Doodad Table Functions

### Table_GetNpcTemplateName {#Table_GetNpcTemplateName}

Get NPC template name.

```lua
local szName = Table_GetNpcTemplateName(dwTemplateID)
```

### Table_GetDoodadTemplateName {#Table_GetDoodadTemplateName}

Get doodad template name.

```lua
local szName = Table_GetDoodadTemplateName(dwTemplateID)
```

### Table_IsShieldedNpc {#Table_IsShieldedNpc}

Check if NPC is shielded (hidden).

```lua
local bShielded = Table_IsShieldedNpc(dwTemplateID)
```

### Table_GetBoss {#Table_GetBoss}

Get boss information.

```lua
local tBoss = Table_GetBoss(dwBossID)
```

### Table_GetCDProcessBoss {#Table_GetCDProcessBoss}

Get CD process boss information.

```lua
local tBoss = Table_GetCDProcessBoss(dwMapID)
```

---

## Map Table Functions

### Table_GetMapName {#Table_GetMapName}

Get map name.

```lua
local szName = Table_GetMapName(dwMapID)
```

### Table_IsTreasureBattleFieldMap {#Table_IsTreasureBattleFieldMap}

Check if map is treasure battlefield.

```lua
local bTreasure = Table_IsTreasureBattleFieldMap(dwMapID)
```

### Table_IsZombieBattleFieldMap {#Table_IsZombieBattleFieldMap}

Check if map is zombie battlefield.

```lua
local bZombie = Table_IsZombieBattleFieldMap(dwMapID)
```

### Table_IsMobaBattleFieldMap {#Table_IsMobaBattleFieldMap}

Check if map is MOBA battlefield.

```lua
local bMoba = Table_IsMobaBattleFieldMap(dwMapID)
```

---

## Force/Kungfu Functions

### Table_GetForceImageName {#Table_GetForceImageName}

Get force (faction) image name.

```lua
local szImage = Table_GetForceImageName(nForceID)
```

### Table_SchoolToForce {#Table_SchoolToForce}

Convert school ID to force ID.

```lua
local nForceID = Table_SchoolToForce(nSchoolID)
```

### Table_ForceToSchool {#Table_ForceToSchool}

Convert force ID to school ID.

```lua
local nSchoolID = Table_ForceToSchool(nForceID)
```

### Table_GetMKungfuBg {#Table_GetMKungfuBg}

Get mount kungfu background image.

```lua
local szBg = Table_GetMKungfuBg(dwKungfuID)
```

### Table_GetMKungfuList {#Table_GetMKungfuList}

Get mount kungfu list.

```lua
local tList = Table_GetMKungfuList(nForceID)
```

### Table_GetKungfuSkillList {#Table_GetKungfuSkillList}

Get kungfu skill list.

```lua
local tList = Table_GetKungfuSkillList(dwKungfuID)
```

---

## Pet Functions

### Table_GetPetSkill {#Table_GetPetSkill}

Get pet skill data.

```lua
local tSkill = Table_GetPetSkill(dwPetSkillID)
```

### Table_GetPetAvatar {#Table_GetPetAvatar}

Get pet avatar data.

```lua
local tAvatar = Table_GetPetAvatar(dwPetID)
```

---

## Other Functions

### Table_GetQuestPoint {#Table_GetQuestPoint}

Get quest point data.

```lua
local tPoint = Table_GetQuestPoint(dwQuestID)
```

### Table_GetMagicAttributeInfo {#Table_GetMagicAttributeInfo}

Get magic attribute information.

```lua
local tInfo = Table_GetMagicAttributeInfo(nAttributeID)
```

### Table_GetComboSkillInfo {#Table_GetComboSkillInfo}

Get combo skill information.

```lua
local tInfo = Table_GetComboSkillInfo(dwSkillID)
```

### Table_OpenSkillLevel {#Table_OpenSkillLevel}

Get skill open level requirement.

```lua
local nLevel = Table_OpenSkillLevel(dwSkillID)
```

### Table_GetSkillTeach {#Table_GetSkillTeach}

Get skill teaching information.

```lua
local tTeach = Table_GetSkillTeach(dwSkillID)
```

### Table_GetSkillTeachQixueRecommend {#Table_GetSkillTeachQixueRecommend}

Get recommended Qixue for skill.

```lua
local tRecommend = Table_GetSkillTeachQixueRecommend(dwSkillID)
```

### Table_GetGuideSoultion {#Table_GetGuideSoultion}

Get guide solution data.

```lua
local tSolution = Table_GetGuideSoultion(dwGuideID)
```

---

## Example Usage

```lua
-- Get skill info for display
function ShowSkillInfo(dwSkillID, nLevel)
    local szName = Table_GetSkillName(dwSkillID, nLevel)
    local szDesc = Table_GetSkillDesc(dwSkillID, nLevel)
    local nIconID = Table_GetSkillIconID(dwSkillID, nLevel)

    Output("Skill: " .. szName)
    Output("Description: " .. szDesc)
end

-- Get buff info
function ShowBuffInfo(dwBuffID, nLevel)
    local szName = Table_GetBuffName(dwBuffID, nLevel)
    local bVisible = Table_BuffIsVisible(dwBuffID, nLevel)

    if bVisible then
        Output("Buff: " .. szName)
    end
end

-- Check map type
function GetMapType(dwMapID)
    if Table_IsTreasureBattleFieldMap(dwMapID) then
        return "Treasure Battlefield"
    elseif Table_IsZombieBattleFieldMap(dwMapID) then
        return "Zombie Battlefield"
    elseif Table_IsMobaBattleFieldMap(dwMapID) then
        return "MOBA"
    end
    return Table_GetMapName(dwMapID)
end
```

---

## See Also

- [Table File Operations](./Table.md) - Tab file operations
- [Constants](./Constants-Skill.md) - Skill constants
