English | [中文](./KPlayer.zh-CN.md)

# KPlayer

Player object representing a player character in the game.

Notes:

- Obtained via `GetClientPlayer()`, `GetControlPlayer()`, `GetPlayer()`
- Client player is the local player, control player may differ in certain scenarios

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `dwID` | `number` | Player unique ID |
| `nX` | `number` | X coordinate |
| `nY` | `number` | Y coordinate |
| `nZ` | `number` | Z coordinate |
| `nFaceDirection` | `number` | Face direction |
| `szName` | `string` | Player name |
| `szTitle` | `string` | Player title |
| `dwForceID` | `number` | Force ID |
| `nLevel` | `number` | Player level |
| `nExperience` | `number` | Current experience |
| `nOnPracticeRoom` | `number` | Practice room status |
| `nCurrentStamina` | `number` | Current stamina |
| `nCurrentThew` | `number` | Current thew |
| `nMaxStamina` | `number` | Maximum stamina |
| `nMaxThew` | `number` | Maximum thew |
| `nCurrentVigor` | `number` | Current vigor (energy for crafting) |
| `nBattleFieldSide` | `number` | Battlefield side |
| `dwSchoolID` | `number` | School (sect) ID |
| `nGender` | `number` | Gender |
| `dwTongID` | `number` | Guild ID |
| `nMoveState` | `number` | Move state (see `MOVE_STATE`) |
| `bOnHorse` | `boolean` | Whether on mount |
| `bFightState` | `boolean` | Whether in combat |
| `nCurrentTrainValue` | `number` | Current train value |
| `nMaxTrainValue` | `number` | Maximum train value |
| `nUsedTrainValue` | `number` | Used train value |
| `nDirectionXY` | `number` | XY direction |
| `nCurrentLife` | `number` | Current life |
| `nMaxLife` | `number` | Maximum life |
| `nMaxLifeBase` | `number` | Base maximum life |
| `nCurrentMana` | `number` | Current mana |
| `nMaxMana` | `number` | Maximum mana |
| `nMaxManaBase` | `number` | Base maximum mana |
| `nCurrentEnergy` | `number` | Current energy |
| `nMaxEnergy` | `number` | Maximum energy |
| `nEnergyReplenish` | `number` | Energy replenish rate |
| `nAccumulateValue` | `number` | Accumulate value |
| `nCurrentSunEnergy` | `number` | Current sun energy (for certain schools) |
| `nSunPowerValue` | `number` | Sun power value |
| `nMaxSunEnergy` | `number` | Maximum sun energy |
| `nCurrentMoonEnergy` | `number` | Current moon energy |
| `nMoonPowerValue` | `number` | Moon power value |
| `nMaxMoonEnergy` | `number` | Maximum moon energy |
| `nCamp` | `number` | Camp type |
| `bCampFlag` | `boolean` | Camp flag |
| `nCurrentPrestige` | `number` | Current prestige |
| `nPoseState` | `number` | Pose state (see `POSE_TYPE`) |
| `nCurrentRage` | `number` | Current rage |
| `nMaxRage` | `number` | Maximum rage |
| `nRunSpeed` | `number` | Run speed |
| `nRunSpeedBase` | `number` | Base run speed |
| `dwTeamID` | `number` | Team ID |
| `nRoleType` | `number` | Role type (see `ROLE_TYPE`) |
| `nContribution` | `number` | Contribution points |
| `nCoin` | `number` | Coin amount |
| `nJustice` | `number` | Justice points |
| `nExamPrint` | `number` | Exam print (trial points) |
| `nArenaAward` | `number` | Arena award points |
| `nActivityAward` | `number` | Activity award points |
| `bHideHat` | `boolean` | Whether hat is hidden |
| `bRedName` | `boolean` | Whether has red name (PK flag) |
| `dwKillCount` | `number` | Kill count |
| `nRankPoint` | `number` | Rank points |
| `nTitle` | `number` | Current title ID |
| `nTitlePoint` | `number` | Title points |
| `dwPetID` | `number` | Pet ID |
| `bCanUseBigSword` | `boolean` | Whether can use big sword |
| `dwMiniAvatarID` | `number` | Mini avatar ID |
| `nSprintPower` | `number` | Sprint power |
| `nSprintPowerMax` | `number` | Maximum sprint power |
| `nSprintPowerRevive` | `number` | Sprint power revive rate |
| `nHorseSprintPower` | `number` | Horse sprint power |
| `nHorseSprintPowerMax` | `number` | Maximum horse sprint power |
| `nHorseSprintPowerRevive` | `number` | Horse sprint power revive rate |
| `bSprintFlag` | `boolean` | Sprint flag |

## Methods

### Object Retrieval Methods

[`GetItem`](#KPlayer_GetItem)
[`GetKungfuMount`](#KPlayer_GetKungfuMount)
[`GetTalkLinkItem`](#KPlayer_GetTalkLinkItem)
[`GetPet`](#KPlayer_GetPet)
[`GetScene`](#KPlayer_GetScene)

### Status Methods

[`GetTarget`](#KPlayer_GetTarget)
[`GetGlobalID`](#KPlayer_GetGlobalID)
[`GetBoxSize`](#KPlayer_GetBoxSize)
[`GetBuffCount`](#KPlayer_GetBuffCount)
[`GetBuff`](#KPlayer_GetBuff)
[`IsInParty`](#KPlayer_IsInParty)
[`IsInRaid`](#KPlayer_IsInRaid)
[`IsPlayerInMyParty`](#KPlayer_IsPlayerInMyParty)
[`IsPartyMemberInSameScene`](#KPlayer_IsPartyMemberInSameScene)
[`IsPartyLeader`](#KPlayer_IsPartyLeader)
[`IsPartyFull`](#KPlayer_IsPartyFull)
[`GetMapID`](#KPlayer_GetMapID)
[`GetAbsoluteCoordinate`](#KPlayer_GetAbsoluteCoordinate)
[`GetOTActionState`](#KPlayer_GetOTActionState)
[`GetSkillOTActionState`](#KPlayer_GetSkillOTActionState)
[`GetSkillPrepareState`](#KPlayer_GetSkillPrepareState)
[`GetMoney`](#KPlayer_GetMoney)

### Skill Methods

[`GetAllSkillList`](#KPlayer_GetAllSkillList)
[`GetSkillList`](#KPlayer_GetSkillList)
[`GetKungfuList`](#KPlayer_GetKungfuList)
[`GetSkillLevel`](#KPlayer_GetSkillLevel)
[`GetSkillCDProgress`](#KPlayer_GetSkillCDProgress)
[`GetSkillRecipeKey`](#KPlayer_GetSkillRecipeKey)
[`GetSkillRecipeList`](#KPlayer_GetSkillRecipeList)
[`GetCDLeft`](#KPlayer_GetCDLeft)
[`GetCDInterval`](#KPlayer_GetCDInterval)
[`GetCDMaxCount`](#KPlayer_GetCDMaxCount)
[`GetCDMaxOverDraftCount`](#KPlayer_GetCDMaxOverDraftCount)
[`ActiveSkillRecipe`](#KPlayer_ActiveSkillRecipe)
[`DeactiveSKillRecipe`](#KPlayer_DeactiveSKillRecipe)
[`GetKungfuMountID`](#KPlayer_GetKungfuMountID)

### Item Methods

[`GetItemAmount`](#KPlayer_GetItemAmount)
[`GetItemAmountInAllPackages`](#KPlayer_GetItemAmountInAllPackages)
[`GetBoxFreeRoomSize`](#KPlayer_GetBoxFreeRoomSize)
[`GetItemCDProgress`](#KPlayer_GetItemCDProgress)
[`GetItemPos`](#KPlayer_GetItemPos)
[`GetEquipPos`](#KPlayer_GetEquipPos)
[`ExchangeItem`](#KPlayer_ExchangeItem)
[`GetBankPackageCount`](#KPlayer_GetBankPackageCount)

### Quest Methods

[`GetQuestPhase`](#KPlayer_GetQuestPhase)
[`GetQuestTree`](#KPlayer_GetQuestTree)
[`GetQuestID`](#KPlayer_GetQuestID)
[`GetQuestTraceInfo`](#KPlayer_GetQuestTraceInfo)
[`GetQuestState`](#KPlayer_GetQuestState)
[`GetQuestDiffcultyLevel`](#KPlayer_GetQuestDiffcultyLevel)
[`GetQuestExpAttenuation`](#KPlayer_GetQuestExpAttenuation)
[`GetQuestAssistDailyCount`](#KPlayer_GetQuestAssistDailyCount)
[`GetFinishedDailyQuestCount`](#KPlayer_GetFinishedDailyQuestCount)
[`GetMaxAcceptDailyQuestCount`](#KPlayer_GetMaxAcceptDailyQuestCount)
[`CanAcceptQuest`](#KPlayer_CanAcceptQuest)

### Profession Methods

[`GetProfession`](#KPlayer_GetProfession)
[`GetProfessionLevel`](#KPlayer_GetProfessionLevel)
[`GetProfessionMaxLevel`](#KPlayer_GetProfessionMaxLevel)
[`GetProfessionProficiency`](#KPlayer_GetProfessionProficiency)
[`GetProfessionBranch`](#KPlayer_GetProfessionBranch)
[`GetProfessionAdjustLevel`](#KPlayer_GetProfessionAdjustLevel)
[`IsProfessionLearnedByCraftID`](#KPlayer_IsProfessionLearnedByCraftID)
[`CastProfessionSkill`](#KPlayer_CastProfessionSkill)
[`IsRecipeLearned`](#KPlayer_IsRecipeLearned)
[`GetRecipe`](#KPlayer_GetRecipe)

### Book Methods

[`IsBookMemorized`](#KPlayer_IsBookMemorized)
[`GetBookList`](#KPlayer_GetBookList)
[`GetBookSegmentList`](#KPlayer_GetBookSegmentList)

### Fellowship Methods

[`GetFellowshipGroupInfo`](#KPlayer_GetFellowshipGroupInfo)
[`GetFellowshipInfo`](#KPlayer_GetFellowshipInfo)
[`GetFoeInfo`](#KPlayer_GetFoeInfo)
[`SetFellowshipRemark`](#KPlayer_SetFellowshipRemark)

### Equipment Methods

[`GetRepresentID`](#KPlayer_GetRepresentID)
[`GetEquipIDArray`](#KPlayer_GetEquipIDArray)
[`GetTotalEquipScore`](#KPlayer_GetTotalEquipScore)
[`GetBaseEquipScore`](#KPlayer_GetBaseEquipScore)
[`GetStrengthEquipScore`](#KPlayer_GetStrengthEquipScore)
[`GetMountsEquipScore`](#KPlayer_GetMountsEquipScore)
[`CanBreakEquip`](#KPlayer_CanBreakEquip)

### Reputation Methods

[`GetReputation`](#KPlayer_GetReputation)
[`GetReputeLevel`](#KPlayer_GetReputeLevel)

### Achievement Methods

[`IsAchievementAcquired`](#KPlayer_IsAchievementAcquired)
[`GetAchievementRecord`](#KPlayer_GetAchievementRecord)
[`IsDesignationPrefixAcquired`](#KPlayer_IsDesignationPrefixAcquired)
[`IsDesignationPostfixAcquired`](#KPlayer_IsDesignationPostfixAcquired)

### Talent Methods

[`OpenTalent`](#KPlayer_OpenTalent)
[`GetTalentInfo`](#KPlayer_GetTalentInfo)
[`OpenVenation`](#KPlayer_OpenVenation)

### Action Methods

[`Talk`](#KPlayer_Talk)
[`GetTalkData`](#KPlayer_GetTalkData)
[`Jump`](#KPlayer_Jump)
[`StopCurrentAction`](#KPlayer_StopCurrentAction)
[`CancelBuff`](#KPlayer_CancelBuff)
[`WindowSelect`](#KPlayer_WindowSelect)
[`CanDialog`](#KPlayer_CanDialog)
[`CanApplyDuel`](#KPlayer_CanApplyDuel)
[`CanAddFoe`](#KPlayer_CanAddFoe)

### Misc Methods

[`GetMaxExamPrint`](#KPlayer_GetMaxExamPrint)
[`GetExamPrintRemainSpace`](#KPlayer_GetExamPrintRemainSpace)
[`GetMapVisitFlag`](#KPlayer_GetMapVisitFlag)
[`SatisfyRequire`](#KPlayer_SatisfyRequire)
[`GetMaxVigor`](#KPlayer_GetMaxVigor)
[`GetVigorRemainSpace`](#KPlayer_GetVigorRemainSpace)

---

* <h4 id="KPlayer_GetItem">GetItem</h4>

Gets an item from player's inventory.

 > ([`KGItem`](./KGItem.md) item) KPlayer:GetItem(`number` nPackage, `number` nIndex)

* <h4 id="KPlayer_GetKungfuMount">GetKungfuMount</h4>

Gets the currently mounted kungfu (inner skill).

 > ([`KSkill`](./KSkill.md) skill) KPlayer:GetKungfuMount()

* <h4 id="KPlayer_GetTalkLinkItem">GetTalkLinkItem</h4>

Gets item from chat link.

 > ([`KGItem`](./KGItem.md) item) KPlayer:GetTalkLinkItem(`number` nIndex)

* <h4 id="KPlayer_GetPet">GetPet</h4>

Gets the player's pet NPC.

 > ([`KNpc`](./KNpc.md) pet) KPlayer:GetPet()

* <h4 id="KPlayer_GetScene">GetScene</h4>

Gets the scene where the player is located.

 > ([`KScene`](./KScene.md) scene) KPlayer:GetScene()

* <h4 id="KPlayer_GetTarget">GetTarget</h4>

Gets the player's current target.

 > (`number` dwTargetType, `number` dwTargetID) KPlayer:GetTarget()

* <h4 id="KPlayer_GetGlobalID">GetGlobalID</h4>

Gets the player's global ID.

 > (`number` dwGlobalID) KPlayer:GetGlobalID()

* <h4 id="KPlayer_GetBoxSize">GetBoxSize</h4>

Gets the size of specified inventory box.

 > (`number` nSize) KPlayer:GetBoxSize(`number` nBox)

* <h4 id="KPlayer_GetBuffCount">GetBuffCount</h4>

Gets the number of buffs on the player.

 > (`number` nCount) KPlayer:GetBuffCount()

* <h4 id="KPlayer_GetBuff">GetBuff</h4>

Gets buff information by index.

 > (`table` tBuff) KPlayer:GetBuff(`number` nIndex)

* <h4 id="KPlayer_IsInParty">IsInParty</h4>

Checks if the player is in a party.

 > (`boolean` bInParty) KPlayer:IsInParty()

* <h4 id="KPlayer_IsInRaid">IsInRaid</h4>

Checks if the player is in a raid.

 > (`boolean` bInRaid) KPlayer:IsInRaid()

* <h4 id="KPlayer_IsPlayerInMyParty">IsPlayerInMyParty</h4>

Checks if specified player is in the same party.

 > (`boolean` bInParty) KPlayer:IsPlayerInMyParty(`number` dwPlayerID)

* <h4 id="KPlayer_IsPartyMemberInSameScene">IsPartyMemberInSameScene</h4>

Checks if a party member is in the same scene.

 > (`boolean` bSameScene) KPlayer:IsPartyMemberInSameScene(`number` dwPlayerID)

* <h4 id="KPlayer_IsPartyLeader">IsPartyLeader</h4>

Checks if the player is party leader.

 > (`boolean` bLeader) KPlayer:IsPartyLeader()

* <h4 id="KPlayer_IsPartyFull">IsPartyFull</h4>

Checks if the party is full.

 > (`boolean` bFull) KPlayer:IsPartyFull()

* <h4 id="KPlayer_GetMapID">GetMapID</h4>

Gets the map ID where the player is located.

 > (`number` dwMapID) KPlayer:GetMapID()

* <h4 id="KPlayer_GetAbsoluteCoordinate">GetAbsoluteCoordinate</h4>

Gets the player's absolute world coordinates.

 > (`number` nX, `number` nY, `number` nZ) KPlayer:GetAbsoluteCoordinate()

* <h4 id="KPlayer_GetOTActionState">GetOTActionState</h4>

Gets the player's OT action state.

 > (`table` tState) KPlayer:GetOTActionState()

* <h4 id="KPlayer_GetSkillOTActionState">GetSkillOTActionState</h4>

Gets the player's skill OT action state.

Notes:
- Returns nil for enemy players

 > (`table` tState) KPlayer:GetSkillOTActionState()

* <h4 id="KPlayer_GetSkillPrepareState">GetSkillPrepareState</h4>

Gets the player's skill prepare state (legacy).

 > (`table` tState) KPlayer:GetSkillPrepareState()

* <h4 id="KPlayer_GetMoney">GetMoney</h4>

Gets the player's money amount.

 > (`number` nMoney) KPlayer:GetMoney()

* <h4 id="KPlayer_GetAllSkillList">GetAllSkillList</h4>

Gets all skills of the player.

 > (`table` tSkillList) KPlayer:GetAllSkillList()

* <h4 id="KPlayer_GetSkillList">GetSkillList</h4>

Gets skills of specified kungfu.

 > (`table` tSkillList) KPlayer:GetSkillList(`number` dwKungfuID)

* <h4 id="KPlayer_GetKungfuList">GetKungfuList</h4>

Gets the list of kungfu (inner skills).

 > (`table` tKungfuList) KPlayer:GetKungfuList()

* <h4 id="KPlayer_GetSkillLevel">GetSkillLevel</h4>

Gets the level of specified skill.

 > (`number` nLevel) KPlayer:GetSkillLevel(`number` dwSkillID)

* <h4 id="KPlayer_GetSkillCDProgress">GetSkillCDProgress</h4>

Gets skill cooldown progress.

 > (`number` nLeft, `number` nTotal) KPlayer:GetSkillCDProgress(`number` dwSkillID)

* <h4 id="KPlayer_GetSkillRecipeKey">GetSkillRecipeKey</h4>

Gets the skill recipe key.

 > (`number` nKey) KPlayer:GetSkillRecipeKey(`number` dwSkillID, `number` dwSkillLevel)

* <h4 id="KPlayer_GetSkillRecipeList">GetSkillRecipeList</h4>

Gets the list of skill recipes.

 > (`table` tRecipeList) KPlayer:GetSkillRecipeList(`number` dwSkillID)

* <h4 id="KPlayer_GetCDLeft">GetCDLeft</h4>

Gets remaining cooldown time.

 > (`number` nLeft) KPlayer:GetCDLeft(`number` dwCDID)

* <h4 id="KPlayer_GetCDInterval">GetCDInterval</h4>

Gets cooldown interval.

 > (`number` nInterval) KPlayer:GetCDInterval(`number` dwCDID)

* <h4 id="KPlayer_GetCDMaxCount">GetCDMaxCount</h4>

Gets maximum CD count.

 > (`number` nMaxCount) KPlayer:GetCDMaxCount(`number` dwCDID)

* <h4 id="KPlayer_GetCDMaxOverDraftCount">GetCDMaxOverDraftCount</h4>

Gets maximum overdraft count for CD.

 > (`number` nMaxOverDraft) KPlayer:GetCDMaxOverDraftCount(`number` dwCDID)

* <h4 id="KPlayer_ActiveSkillRecipe">ActiveSkillRecipe</h4>

Activates a skill recipe.

 > (`void`) KPlayer:ActiveSkillRecipe(`number` dwRecipeID)

* <h4 id="KPlayer_DeactiveSKillRecipe">DeactiveSKillRecipe</h4>

Deactivates a skill recipe.

 > (`void`) KPlayer:DeactiveSKillRecipe(`number` dwRecipeID)

* <h4 id="KPlayer_GetKungfuMountID">GetKungfuMountID</h4>

Gets the mounted kungfu ID.

 > (`number` dwKungfuID) KPlayer:GetKungfuMountID()

* <h4 id="KPlayer_GetItemAmount">GetItemAmount</h4>

Gets the amount of specified item in inventory.

 > (`number` nAmount) KPlayer:GetItemAmount(`number` dwTabType, `number` dwIndex)

* <h4 id="KPlayer_GetItemAmountInAllPackages">GetItemAmountInAllPackages</h4>

Gets item amount across all packages.

 > (`number` nAmount) KPlayer:GetItemAmountInAllPackages(`number` dwTabType, `number` dwIndex)

* <h4 id="KPlayer_GetBoxFreeRoomSize">GetBoxFreeRoomSize</h4>

Gets free room size in specified box.

 > (`number` nFreeRoom) KPlayer:GetBoxFreeRoomSize(`number` nBox)

* <h4 id="KPlayer_GetItemCDProgress">GetItemCDProgress</h4>

Gets item cooldown progress.

 > (`number` nLeft, `number` nTotal) KPlayer:GetItemCDProgress(`number` dwTabType, `number` dwIndex)

* <h4 id="KPlayer_GetItemPos">GetItemPos</h4>

Gets the position of an item in inventory.

 > (`number` nPackage, `number` nIndex) KPlayer:GetItemPos(`number` dwTabType, `number` dwIndex)

* <h4 id="KPlayer_GetEquipPos">GetEquipPos</h4>

Gets equipment position.

 > (`number` nPos) KPlayer:GetEquipPos(`number` nEquipSlot)

* <h4 id="KPlayer_ExchangeItem">ExchangeItem</h4>

Exchanges items between inventory slots.

 > (`void`) KPlayer:ExchangeItem(`number` nFromPackage, `number` nFromIndex, `number` nToPackage, `number` nToIndex)

* <h4 id="KPlayer_GetBankPackageCount">GetBankPackageCount</h4>

Gets the number of bank packages.

 > (`number` nCount) KPlayer:GetBankPackageCount()

* <h4 id="KPlayer_GetQuestPhase">GetQuestPhase</h4>

Gets the current phase of a quest.

 > (`number` nPhase) KPlayer:GetQuestPhase(`number` dwQuestID)

* <h4 id="KPlayer_GetQuestTree">GetQuestTree</h4>

Gets the quest tree structure.

 > (`table` tQuestTree) KPlayer:GetQuestTree()

* <h4 id="KPlayer_GetQuestID">GetQuestID</h4>

Gets quest ID by index.

 > (`number` dwQuestID) KPlayer:GetQuestID(`number` nIndex)

* <h4 id="KPlayer_GetQuestTraceInfo">GetQuestTraceInfo</h4>

Gets quest trace information.

 > (`table` tTraceInfo) KPlayer:GetQuestTraceInfo(`number` dwQuestID)

* <h4 id="KPlayer_GetQuestState">GetQuestState</h4>

Gets the state of a quest.

 > (`number` nState) KPlayer:GetQuestState(`number` dwQuestID)

* <h4 id="KPlayer_GetQuestDiffcultyLevel">GetQuestDiffcultyLevel</h4>

Gets quest difficulty level.

 > (`number` nDifficulty) KPlayer:GetQuestDiffcultyLevel(`number` dwQuestID)

* <h4 id="KPlayer_GetQuestExpAttenuation">GetQuestExpAttenuation</h4>

Gets quest experience attenuation.

 > (`number` fAttenuation) KPlayer:GetQuestExpAttenuation(`number` dwQuestID)

* <h4 id="KPlayer_GetQuestAssistDailyCount">GetQuestAssistDailyCount</h4>

Gets daily quest assist count.

 > (`number` nCount) KPlayer:GetQuestAssistDailyCount()

* <h4 id="KPlayer_GetFinishedDailyQuestCount">GetFinishedDailyQuestCount</h4>

Gets finished daily quest count.

 > (`number` nCount) KPlayer:GetFinishedDailyQuestCount()

* <h4 id="KPlayer_GetMaxAcceptDailyQuestCount">GetMaxAcceptDailyQuestCount</h4>

Gets maximum acceptable daily quest count.

 > (`number` nMax) KPlayer:GetMaxAcceptDailyQuestCount()

* <h4 id="KPlayer_CanAcceptQuest">CanAcceptQuest</h4>

Checks if a quest can be accepted.

 > (`boolean` bCanAccept) KPlayer:CanAcceptQuest(`number` dwQuestID)

* <h4 id="KPlayer_GetProfession">GetProfession</h4>

Gets profession information.

 > (`table` tProfession) KPlayer:GetProfession(`number` nProfessionID)

* <h4 id="KPlayer_GetProfessionLevel">GetProfessionLevel</h4>

Gets profession level.

 > (`number` nLevel) KPlayer:GetProfessionLevel(`number` nProfessionID)

* <h4 id="KPlayer_GetProfessionMaxLevel">GetProfessionMaxLevel</h4>

Gets maximum profession level.

 > (`number` nMaxLevel) KPlayer:GetProfessionMaxLevel(`number` nProfessionID)

* <h4 id="KPlayer_GetProfessionProficiency">GetProfessionProficiency</h4>

Gets profession proficiency.

 > (`number` nProficiency) KPlayer:GetProfessionProficiency(`number` nProfessionID)

* <h4 id="KPlayer_GetProfessionBranch">GetProfessionBranch</h4>

Gets profession branch.

 > (`number` nBranch) KPlayer:GetProfessionBranch(`number` nProfessionID)

* <h4 id="KPlayer_GetProfessionAdjustLevel">GetProfessionAdjustLevel</h4>

Gets profession adjust level.

 > (`number` nAdjustLevel) KPlayer:GetProfessionAdjustLevel(`number` nProfessionID)

* <h4 id="KPlayer_IsProfessionLearnedByCraftID">IsProfessionLearnedByCraftID</h4>

Checks if profession is learned by craft ID.

 > (`boolean` bLearned) KPlayer:IsProfessionLearnedByCraftID(`number` dwCraftID)

* <h4 id="KPlayer_CastProfessionSkill">CastProfessionSkill</h4>

Casts a profession skill.

 > (`void`) KPlayer:CastProfessionSkill(`number` dwRecipeID)

* <h4 id="KPlayer_IsRecipeLearned">IsRecipeLearned</h4>

Checks if a recipe is learned.

 > (`boolean` bLearned) KPlayer:IsRecipeLearned(`number` dwRecipeID)

* <h4 id="KPlayer_GetRecipe">GetRecipe</h4>

Gets recipe information.

 > (`table` tRecipe) KPlayer:GetRecipe(`number` dwRecipeID)

* <h4 id="KPlayer_IsBookMemorized">IsBookMemorized</h4>

Checks if a book is memorized.

 > (`boolean` bMemorized) KPlayer:IsBookMemorized(`number` dwBookID)

* <h4 id="KPlayer_GetBookList">GetBookList</h4>

Gets the list of memorized books.

 > (`table` tBookList) KPlayer:GetBookList()

* <h4 id="KPlayer_GetBookSegmentList">GetBookSegmentList</h4>

Gets book segment list.

 > (`table` tSegmentList) KPlayer:GetBookSegmentList(`number` dwBookID)

* <h4 id="KPlayer_GetFellowshipGroupInfo">GetFellowshipGroupInfo</h4>

Gets fellowship group information.

 > (`table` tGroupInfo) KPlayer:GetFellowshipGroupInfo()

* <h4 id="KPlayer_GetFellowshipInfo">GetFellowshipInfo</h4>

Gets fellowship information.

 > (`table` tFellowship) KPlayer:GetFellowshipInfo(`number` dwPlayerID)

* <h4 id="KPlayer_GetFoeInfo">GetFoeInfo</h4>

Gets foe information.

 > (`table` tFoeInfo) KPlayer:GetFoeInfo(`number` dwPlayerID)

* <h4 id="KPlayer_SetFellowshipRemark">SetFellowshipRemark</h4>

Sets fellowship remark.

 > (`void`) KPlayer:SetFellowshipRemark(`number` dwPlayerID, `string` szRemark)

* <h4 id="KPlayer_GetRepresentID">GetRepresentID</h4>

Gets represent (appearance) ID.

 > (`number` dwRepresentID) KPlayer:GetRepresentID(`number` nSlot)

* <h4 id="KPlayer_GetEquipIDArray">GetEquipIDArray</h4>

Gets equipment ID array.

 > (`table` tEquipIDs) KPlayer:GetEquipIDArray()

* <h4 id="KPlayer_GetTotalEquipScore">GetTotalEquipScore</h4>

Gets total equipment score.

 > (`number` nScore) KPlayer:GetTotalEquipScore()

* <h4 id="KPlayer_GetBaseEquipScore">GetBaseEquipScore</h4>

Gets base equipment score.

 > (`number` nScore) KPlayer:GetBaseEquipScore()

* <h4 id="KPlayer_GetStrengthEquipScore">GetStrengthEquipScore</h4>

Gets strengthen equipment score.

 > (`number` nScore) KPlayer:GetStrengthEquipScore()

* <h4 id="KPlayer_GetMountsEquipScore">GetMountsEquipScore</h4>

Gets mounts (gems) equipment score.

 > (`number` nScore) KPlayer:GetMountsEquipScore()

* <h4 id="KPlayer_CanBreakEquip">CanBreakEquip</h4>

Checks if equipment can be broken down.

 > (`boolean` bCanBreak) KPlayer:CanBreakEquip(`number` nPackage, `number` nIndex)

* <h4 id="KPlayer_GetReputation">GetReputation</h4>

Gets reputation with a faction.

 > (`number` nReputation) KPlayer:GetReputation(`number` dwFactionID)

* <h4 id="KPlayer_GetReputeLevel">GetReputeLevel</h4>

Gets reputation level with a faction.

 > (`number` nLevel) KPlayer:GetReputeLevel(`number` dwFactionID)

* <h4 id="KPlayer_IsAchievementAcquired">IsAchievementAcquired</h4>

Checks if an achievement is acquired.

 > (`boolean` bAcquired) KPlayer:IsAchievementAcquired(`number` dwAchievementID)

* <h4 id="KPlayer_GetAchievementRecord">GetAchievementRecord</h4>

Gets achievement record.

 > (`table` tRecord) KPlayer:GetAchievementRecord(`number` dwAchievementID)

* <h4 id="KPlayer_IsDesignationPrefixAcquired">IsDesignationPrefixAcquired</h4>

Checks if a designation prefix is acquired.

 > (`boolean` bAcquired) KPlayer:IsDesignationPrefixAcquired(`number` dwDesignationID)

* <h4 id="KPlayer_IsDesignationPostfixAcquired">IsDesignationPostfixAcquired</h4>

Checks if a designation postfix is acquired.

 > (`boolean` bAcquired) KPlayer:IsDesignationPostfixAcquired(`number` dwDesignationID)

* <h4 id="KPlayer_OpenTalent">OpenTalent</h4>

Opens talent panel.

 > (`void`) KPlayer:OpenTalent()

* <h4 id="KPlayer_GetTalentInfo">GetTalentInfo</h4>

Gets talent information.

 > (`table` tTalentInfo) KPlayer:GetTalentInfo()

* <h4 id="KPlayer_OpenVenation">OpenVenation</h4>

Opens venation (meridian) panel.

 > (`void`) KPlayer:OpenVenation()

* <h4 id="KPlayer_Talk">Talk</h4>

Sends a chat message.

Notes:
- Channel restrictions apply based on addon permissions
- Some channels require user action

 > (`void`) KPlayer:Talk(`number` nChannel, `string` szReceiver, `table` tContent)

* <h4 id="KPlayer_GetTalkData">GetTalkData</h4>

Gets talk data.

 > (`table` tTalkData) KPlayer:GetTalkData()

* <h4 id="KPlayer_Jump">Jump</h4>

Makes the player jump.

 > (`void`) KPlayer:Jump()

* <h4 id="KPlayer_StopCurrentAction">StopCurrentAction</h4>

Stops the current action.

 > (`void`) KPlayer:StopCurrentAction()

* <h4 id="KPlayer_CancelBuff">CancelBuff</h4>

Cancels a buff.

 > (`void`) KPlayer:CancelBuff(`number` dwBuffID, `number` nLevel)

* <h4 id="KPlayer_WindowSelect">WindowSelect</h4>

Performs a window selection.

 > (`void`) KPlayer:WindowSelect(`number` nOption)

* <h4 id="KPlayer_CanDialog">CanDialog</h4>

Checks if dialog is possible.

 > (`boolean` bCanDialog) KPlayer:CanDialog()

* <h4 id="KPlayer_CanApplyDuel">CanApplyDuel</h4>

Checks if duel application is possible.

 > (`boolean` bCanApply) KPlayer:CanApplyDuel(`number` dwTargetID)

* <h4 id="KPlayer_CanAddFoe">CanAddFoe</h4>

Checks if a player can be added as foe.

 > (`boolean` bCanAdd) KPlayer:CanAddFoe(`number` dwTargetID)

* <h4 id="KPlayer_GetMaxExamPrint">GetMaxExamPrint</h4>

Gets maximum exam print (trial points).

 > (`number` nMax) KPlayer:GetMaxExamPrint()

* <h4 id="KPlayer_GetExamPrintRemainSpace">GetExamPrintRemainSpace</h4>

Gets remaining exam print space.

 > (`number` nRemain) KPlayer:GetExamPrintRemainSpace()

* <h4 id="KPlayer_GetMapVisitFlag">GetMapVisitFlag</h4>

Gets map visit flag.

 > (`number` nFlag) KPlayer:GetMapVisitFlag(`number` dwMapID)

* <h4 id="KPlayer_SatisfyRequire">SatisfyRequire</h4>

Checks if requirements are satisfied.

 > (`boolean` bSatisfy) KPlayer:SatisfyRequire(`table` tRequire)

* <h4 id="KPlayer_GetMaxVigor">GetMaxVigor</h4>

Gets maximum vigor.

 > (`number` nMaxVigor) KPlayer:GetMaxVigor()

* <h4 id="KPlayer_GetVigorRemainSpace">GetVigorRemainSpace</h4>

Gets remaining vigor space.

 > (`number` nRemain) KPlayer:GetVigorRemainSpace()

---

## Shielded Methods

The following methods are blocked in addon environment and cannot be used:

| Method | Description |
|--------|-------------|
| `TurnTo` | ⚠️ Blocked - Turn to specified direction |
| `FinishQuest` | ⚠️ Blocked - Finish quest |
| `GetBlackListInfo` | ⚠️ Blocked - Get blacklist info |
| `DelBlackList` | ⚠️ Blocked - Delete from blacklist |
| `GetAroundPlayerID` | ⚠️ Blocked - Get nearby player IDs |
| `UpdateFellowshipInfo` | ⚠️ Blocked - Update fellowship info |
| `SetTitle` | ⚠️ Blocked - Set title |
| `ApplyDuel` | ⚠️ Blocked - Apply for duel |
| `AddBlackList` | ⚠️ Blocked - Add to blacklist |
| `AcceptQuest` | ⚠️ Blocked - Accept quest |
