[English](./KPlayer.md) | 中文

# KPlayer（玩家对象）

玩家对象，代表游戏中的玩家角色。

说明：

- 通过 `GetClientPlayer()`、`GetControlPlayer()`、`GetPlayer()` 获取
- 客户端玩家是本地玩家，控制玩家在某些场景下可能不同

## 属性

| 属性 | 类型 | 说明 |
|------|------|------|
| `dwID` | `number` | 玩家唯一 ID |
| `nX` | `number` | X 坐标 |
| `nY` | `number` | Y 坐标 |
| `nZ` | `number` | Z 坐标 |
| `nFaceDirection` | `number` | 面向方向 |
| `szName` | `string` | 玩家名称 |
| `szTitle` | `string` | 玩家称号 |
| `dwForceID` | `number` | 势力 ID |
| `nLevel` | `number` | 玩家等级 |
| `nExperience` | `number` | 当前经验值 |
| `nOnPracticeRoom` | `number` | 修炼房状态 |
| `nCurrentStamina` | `number` | 当前体力 |
| `nCurrentThew` | `number` | 当前精力 |
| `nMaxStamina` | `number` | 最大体力 |
| `nMaxThew` | `number` | 最大精力 |
| `nCurrentVigor` | `number` | 当前活力（制造用） |
| `nBattleFieldSide` | `number` | 战场阵营 |
| `dwSchoolID` | `number` | 门派 ID |
| `nGender` | `number` | 性别 |
| `dwTongID` | `number` | 帮会 ID |
| `nMoveState` | `number` | 移动状态（参见 `MOVE_STATE`） |
| `bOnHorse` | `boolean` | 是否骑乘坐骑 |
| `bFightState` | `boolean` | 是否处于战斗状态 |
| `nCurrentTrainValue` | `number` | 当前修为值 |
| `nMaxTrainValue` | `number` | 最大修为值 |
| `nUsedTrainValue` | `number` | 已使用修为值 |
| `nDirectionXY` | `number` | XY 方向 |
| `nCurrentLife` | `number` | 当前生命值 |
| `nMaxLife` | `number` | 最大生命值 |
| `nMaxLifeBase` | `number` | 基础最大生命值 |
| `nCurrentMana` | `number` | 当前内力值 |
| `nMaxMana` | `number` | 最大内力值 |
| `nMaxManaBase` | `number` | 基础最大内力值 |
| `nCurrentEnergy` | `number` | 当前能量值 |
| `nMaxEnergy` | `number` | 最大能量值 |
| `nEnergyReplenish` | `number` | 能量恢复速率 |
| `nAccumulateValue` | `number` | 累积值 |
| `nCurrentSunEnergy` | `number` | 当前日灵（特定门派） |
| `nSunPowerValue` | `number` | 日灵力量值 |
| `nMaxSunEnergy` | `number` | 最大日灵 |
| `nCurrentMoonEnergy` | `number` | 当前月魂 |
| `nMoonPowerValue` | `number` | 月魂力量值 |
| `nMaxMoonEnergy` | `number` | 最大月魂 |
| `nCamp` | `number` | 阵营类型 |
| `bCampFlag` | `boolean` | 阵营标志 |
| `nCurrentPrestige` | `number` | 当前威望 |
| `nPoseState` | `number` | 姿态状态（参见 `POSE_TYPE`） |
| `nCurrentRage` | `number` | 当前怒气 |
| `nMaxRage` | `number` | 最大怒气 |
| `nRunSpeed` | `number` | 移动速度 |
| `nRunSpeedBase` | `number` | 基础移动速度 |
| `dwTeamID` | `number` | 队伍 ID |
| `nRoleType` | `number` | 角色类型（参见 `ROLE_TYPE`） |
| `nContribution` | `number` | 贡献点数 |
| `nCoin` | `number` | 金币数量 |
| `nJustice` | `number` | 侠义值 |
| `nExamPrint` | `number` | 试炼印记 |
| `nArenaAward` | `number` | 竞技场奖励点数 |
| `nActivityAward` | `number` | 活动奖励点数 |
| `bHideHat` | `boolean` | 是否隐藏头盔 |
| `bRedName` | `boolean` | 是否红名（PK 标记） |
| `dwKillCount` | `number` | 击杀数 |
| `nRankPoint` | `number` | 排名积分 |
| `nTitle` | `number` | 当前称号 ID |
| `nTitlePoint` | `number` | 称号点数 |
| `dwPetID` | `number` | 宠物 ID |
| `bCanUseBigSword` | `boolean` | 是否可使用重剑 |
| `dwMiniAvatarID` | `number` | 小头像 ID |
| `nSprintPower` | `number` | 冲刺能量 |
| `nSprintPowerMax` | `number` | 最大冲刺能量 |
| `nSprintPowerRevive` | `number` | 冲刺能量恢复速率 |
| `nHorseSprintPower` | `number` | 坐骑冲刺能量 |
| `nHorseSprintPowerMax` | `number` | 最大坐骑冲刺能量 |
| `nHorseSprintPowerRevive` | `number` | 坐骑冲刺能量恢复速率 |
| `bSprintFlag` | `boolean` | 冲刺标志 |

## 方法

### 对象获取方法

[`GetItem`](#KPlayer_GetItem)
[`GetKungfuMount`](#KPlayer_GetKungfuMount)
[`GetTalkLinkItem`](#KPlayer_GetTalkLinkItem)
[`GetPet`](#KPlayer_GetPet)
[`GetScene`](#KPlayer_GetScene)

### 状态方法

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

### 技能方法

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

### 物品方法

[`GetItemAmount`](#KPlayer_GetItemAmount)
[`GetItemAmountInAllPackages`](#KPlayer_GetItemAmountInAllPackages)
[`GetBoxFreeRoomSize`](#KPlayer_GetBoxFreeRoomSize)
[`GetItemCDProgress`](#KPlayer_GetItemCDProgress)
[`GetItemPos`](#KPlayer_GetItemPos)
[`GetEquipPos`](#KPlayer_GetEquipPos)
[`ExchangeItem`](#KPlayer_ExchangeItem)
[`GetBankPackageCount`](#KPlayer_GetBankPackageCount)

### 任务方法

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

### 生活技能方法

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

### 书籍方法

[`IsBookMemorized`](#KPlayer_IsBookMemorized)
[`GetBookList`](#KPlayer_GetBookList)
[`GetBookSegmentList`](#KPlayer_GetBookSegmentList)

### 好友方法

[`GetFellowshipGroupInfo`](#KPlayer_GetFellowshipGroupInfo)
[`GetFellowshipInfo`](#KPlayer_GetFellowshipInfo)
[`GetFoeInfo`](#KPlayer_GetFoeInfo)
[`SetFellowshipRemark`](#KPlayer_SetFellowshipRemark)

### 装备方法

[`GetRepresentID`](#KPlayer_GetRepresentID)
[`GetEquipIDArray`](#KPlayer_GetEquipIDArray)
[`GetTotalEquipScore`](#KPlayer_GetTotalEquipScore)
[`GetBaseEquipScore`](#KPlayer_GetBaseEquipScore)
[`GetStrengthEquipScore`](#KPlayer_GetStrengthEquipScore)
[`GetMountsEquipScore`](#KPlayer_GetMountsEquipScore)
[`CanBreakEquip`](#KPlayer_CanBreakEquip)

### 声望方法

[`GetReputation`](#KPlayer_GetReputation)
[`GetReputeLevel`](#KPlayer_GetReputeLevel)

### 成就方法

[`IsAchievementAcquired`](#KPlayer_IsAchievementAcquired)
[`GetAchievementRecord`](#KPlayer_GetAchievementRecord)
[`IsDesignationPrefixAcquired`](#KPlayer_IsDesignationPrefixAcquired)
[`IsDesignationPostfixAcquired`](#KPlayer_IsDesignationPostfixAcquired)

### 天赋方法

[`OpenTalent`](#KPlayer_OpenTalent)
[`GetTalentInfo`](#KPlayer_GetTalentInfo)
[`OpenVenation`](#KPlayer_OpenVenation)

### 动作方法

[`Talk`](#KPlayer_Talk)
[`GetTalkData`](#KPlayer_GetTalkData)
[`Jump`](#KPlayer_Jump)
[`StopCurrentAction`](#KPlayer_StopCurrentAction)
[`CancelBuff`](#KPlayer_CancelBuff)
[`WindowSelect`](#KPlayer_WindowSelect)
[`CanDialog`](#KPlayer_CanDialog)
[`CanApplyDuel`](#KPlayer_CanApplyDuel)
[`CanAddFoe`](#KPlayer_CanAddFoe)

### 其他方法

[`GetMaxExamPrint`](#KPlayer_GetMaxExamPrint)
[`GetExamPrintRemainSpace`](#KPlayer_GetExamPrintRemainSpace)
[`GetMapVisitFlag`](#KPlayer_GetMapVisitFlag)
[`SatisfyRequire`](#KPlayer_SatisfyRequire)
[`GetMaxVigor`](#KPlayer_GetMaxVigor)
[`GetVigorRemainSpace`](#KPlayer_GetVigorRemainSpace)

---

* <h4 id="KPlayer_GetItem">GetItem</h4>

从玩家背包获取物品。

 > ([`KGItem`](./KGItem.zh-CN.md) item) KPlayer:GetItem(`number` nPackage, `number` nIndex)

* <h4 id="KPlayer_GetKungfuMount">GetKungfuMount</h4>

获取当前挂载的心法。

 > ([`KSkill`](./KSkill.zh-CN.md) skill) KPlayer:GetKungfuMount()

* <h4 id="KPlayer_GetTalkLinkItem">GetTalkLinkItem</h4>

从聊天链接获取物品。

 > ([`KGItem`](./KGItem.zh-CN.md) item) KPlayer:GetTalkLinkItem(`number` nIndex)

* <h4 id="KPlayer_GetPet">GetPet</h4>

获取玩家的宠物 NPC。

 > ([`KNpc`](./KNpc.zh-CN.md) pet) KPlayer:GetPet()

* <h4 id="KPlayer_GetScene">GetScene</h4>

获取玩家所在的场景。

 > ([`KScene`](./KScene.zh-CN.md) scene) KPlayer:GetScene()

* <h4 id="KPlayer_GetTarget">GetTarget</h4>

获取玩家当前的目标。

 > (`number` dwTargetType, `number` dwTargetID) KPlayer:GetTarget()

* <h4 id="KPlayer_GetGlobalID">GetGlobalID</h4>

获取玩家的全局 ID。

 > (`number` dwGlobalID) KPlayer:GetGlobalID()

* <h4 id="KPlayer_GetBoxSize">GetBoxSize</h4>

获取指定背包的大小。

 > (`number` nSize) KPlayer:GetBoxSize(`number` nBox)

* <h4 id="KPlayer_GetBuffCount">GetBuffCount</h4>

获取玩家身上的 Buff 数量。

 > (`number` nCount) KPlayer:GetBuffCount()

* <h4 id="KPlayer_GetBuff">GetBuff</h4>

根据索引获取 Buff 信息。

 > (`table` tBuff) KPlayer:GetBuff(`number` nIndex)

* <h4 id="KPlayer_IsInParty">IsInParty</h4>

检查玩家是否在队伍中。

 > (`boolean` bInParty) KPlayer:IsInParty()

* <h4 id="KPlayer_IsInRaid">IsInRaid</h4>

检查玩家是否在团队中。

 > (`boolean` bInRaid) KPlayer:IsInRaid()

* <h4 id="KPlayer_IsPlayerInMyParty">IsPlayerInMyParty</h4>

检查指定玩家是否在同一队伍。

 > (`boolean` bInParty) KPlayer:IsPlayerInMyParty(`number` dwPlayerID)

* <h4 id="KPlayer_IsPartyMemberInSameScene">IsPartyMemberInSameScene</h4>

检查队友是否在同一场景。

 > (`boolean` bSameScene) KPlayer:IsPartyMemberInSameScene(`number` dwPlayerID)

* <h4 id="KPlayer_IsPartyLeader">IsPartyLeader</h4>

检查玩家是否为队长。

 > (`boolean` bLeader) KPlayer:IsPartyLeader()

* <h4 id="KPlayer_IsPartyFull">IsPartyFull</h4>

检查队伍是否已满。

 > (`boolean` bFull) KPlayer:IsPartyFull()

* <h4 id="KPlayer_GetMapID">GetMapID</h4>

获取玩家所在的地图 ID。

 > (`number` dwMapID) KPlayer:GetMapID()

* <h4 id="KPlayer_GetAbsoluteCoordinate">GetAbsoluteCoordinate</h4>

获取玩家的绝对世界坐标。

 > (`number` nX, `number` nY, `number` nZ) KPlayer:GetAbsoluteCoordinate()

* <h4 id="KPlayer_GetOTActionState">GetOTActionState</h4>

获取玩家的 OT 动作状态。

 > (`table` tState) KPlayer:GetOTActionState()

* <h4 id="KPlayer_GetSkillOTActionState">GetSkillOTActionState</h4>

获取玩家的技能 OT 动作状态。

说明：
- 对于敌方玩家返回 nil

 > (`table` tState) KPlayer:GetSkillOTActionState()

* <h4 id="KPlayer_GetSkillPrepareState">GetSkillPrepareState</h4>

获取玩家的技能准备状态（旧接口）。

 > (`table` tState) KPlayer:GetSkillPrepareState()

* <h4 id="KPlayer_GetMoney">GetMoney</h4>

获取玩家的金钱数量。

 > (`number` nMoney) KPlayer:GetMoney()

* <h4 id="KPlayer_GetAllSkillList">GetAllSkillList</h4>

获取玩家的所有技能。

 > (`table` tSkillList) KPlayer:GetAllSkillList()

* <h4 id="KPlayer_GetSkillList">GetSkillList</h4>

获取指定心法的技能列表。

 > (`table` tSkillList) KPlayer:GetSkillList(`number` dwKungfuID)

* <h4 id="KPlayer_GetKungfuList">GetKungfuList</h4>

获取心法列表。

 > (`table` tKungfuList) KPlayer:GetKungfuList()

* <h4 id="KPlayer_GetSkillLevel">GetSkillLevel</h4>

获取指定技能的等级。

 > (`number` nLevel) KPlayer:GetSkillLevel(`number` dwSkillID)

* <h4 id="KPlayer_GetSkillCDProgress">GetSkillCDProgress</h4>

获取技能冷却进度。

 > (`number` nLeft, `number` nTotal) KPlayer:GetSkillCDProgress(`number` dwSkillID)

* <h4 id="KPlayer_GetSkillRecipeKey">GetSkillRecipeKey</h4>

获取技能秘籍 Key。

 > (`number` nKey) KPlayer:GetSkillRecipeKey(`number` dwSkillID, `number` dwSkillLevel)

* <h4 id="KPlayer_GetSkillRecipeList">GetSkillRecipeList</h4>

获取技能秘籍列表。

 > (`table` tRecipeList) KPlayer:GetSkillRecipeList(`number` dwSkillID)

* <h4 id="KPlayer_GetCDLeft">GetCDLeft</h4>

获取剩余冷却时间。

 > (`number` nLeft) KPlayer:GetCDLeft(`number` dwCDID)

* <h4 id="KPlayer_GetCDInterval">GetCDInterval</h4>

获取冷却间隔。

 > (`number` nInterval) KPlayer:GetCDInterval(`number` dwCDID)

* <h4 id="KPlayer_GetCDMaxCount">GetCDMaxCount</h4>

获取最大 CD 充能数。

 > (`number` nMaxCount) KPlayer:GetCDMaxCount(`number` dwCDID)

* <h4 id="KPlayer_GetCDMaxOverDraftCount">GetCDMaxOverDraftCount</h4>

获取最大 CD 透支数。

 > (`number` nMaxOverDraft) KPlayer:GetCDMaxOverDraftCount(`number` dwCDID)

* <h4 id="KPlayer_ActiveSkillRecipe">ActiveSkillRecipe</h4>

激活技能秘籍。

 > (`void`) KPlayer:ActiveSkillRecipe(`number` dwRecipeID)

* <h4 id="KPlayer_DeactiveSKillRecipe">DeactiveSKillRecipe</h4>

取消激活技能秘籍。

 > (`void`) KPlayer:DeactiveSKillRecipe(`number` dwRecipeID)

* <h4 id="KPlayer_GetKungfuMountID">GetKungfuMountID</h4>

获取挂载的心法 ID。

 > (`number` dwKungfuID) KPlayer:GetKungfuMountID()

* <h4 id="KPlayer_GetItemAmount">GetItemAmount</h4>

获取背包中指定物品的数量。

 > (`number` nAmount) KPlayer:GetItemAmount(`number` dwTabType, `number` dwIndex)

* <h4 id="KPlayer_GetItemAmountInAllPackages">GetItemAmountInAllPackages</h4>

获取所有背包中物品的数量。

 > (`number` nAmount) KPlayer:GetItemAmountInAllPackages(`number` dwTabType, `number` dwIndex)

* <h4 id="KPlayer_GetBoxFreeRoomSize">GetBoxFreeRoomSize</h4>

获取指定背包的空闲格子数。

 > (`number` nFreeRoom) KPlayer:GetBoxFreeRoomSize(`number` nBox)

* <h4 id="KPlayer_GetItemCDProgress">GetItemCDProgress</h4>

获取物品冷却进度。

 > (`number` nLeft, `number` nTotal) KPlayer:GetItemCDProgress(`number` dwTabType, `number` dwIndex)

* <h4 id="KPlayer_GetItemPos">GetItemPos</h4>

获取物品在背包中的位置。

 > (`number` nPackage, `number` nIndex) KPlayer:GetItemPos(`number` dwTabType, `number` dwIndex)

* <h4 id="KPlayer_GetEquipPos">GetEquipPos</h4>

获取装备位置。

 > (`number` nPos) KPlayer:GetEquipPos(`number` nEquipSlot)

* <h4 id="KPlayer_ExchangeItem">ExchangeItem</h4>

交换背包格子中的物品。

 > (`void`) KPlayer:ExchangeItem(`number` nFromPackage, `number` nFromIndex, `number` nToPackage, `number` nToIndex)

* <h4 id="KPlayer_GetBankPackageCount">GetBankPackageCount</h4>

获取银行背包数量。

 > (`number` nCount) KPlayer:GetBankPackageCount()

* <h4 id="KPlayer_GetQuestPhase">GetQuestPhase</h4>

获取任务当前阶段。

 > (`number` nPhase) KPlayer:GetQuestPhase(`number` dwQuestID)

* <h4 id="KPlayer_GetQuestTree">GetQuestTree</h4>

获取任务树结构。

 > (`table` tQuestTree) KPlayer:GetQuestTree()

* <h4 id="KPlayer_GetQuestID">GetQuestID</h4>

根据索引获取任务 ID。

 > (`number` dwQuestID) KPlayer:GetQuestID(`number` nIndex)

* <h4 id="KPlayer_GetQuestTraceInfo">GetQuestTraceInfo</h4>

获取任务追踪信息。

 > (`table` tTraceInfo) KPlayer:GetQuestTraceInfo(`number` dwQuestID)

* <h4 id="KPlayer_GetQuestState">GetQuestState</h4>

获取任务状态。

 > (`number` nState) KPlayer:GetQuestState(`number` dwQuestID)

* <h4 id="KPlayer_GetQuestDiffcultyLevel">GetQuestDiffcultyLevel</h4>

获取任务难度等级。

 > (`number` nDifficulty) KPlayer:GetQuestDiffcultyLevel(`number` dwQuestID)

* <h4 id="KPlayer_GetQuestExpAttenuation">GetQuestExpAttenuation</h4>

获取任务经验衰减。

 > (`number` fAttenuation) KPlayer:GetQuestExpAttenuation(`number` dwQuestID)

* <h4 id="KPlayer_GetQuestAssistDailyCount">GetQuestAssistDailyCount</h4>

获取每日协助任务次数。

 > (`number` nCount) KPlayer:GetQuestAssistDailyCount()

* <h4 id="KPlayer_GetFinishedDailyQuestCount">GetFinishedDailyQuestCount</h4>

获取已完成的日常任务数量。

 > (`number` nCount) KPlayer:GetFinishedDailyQuestCount()

* <h4 id="KPlayer_GetMaxAcceptDailyQuestCount">GetMaxAcceptDailyQuestCount</h4>

获取最大可接日常任务数量。

 > (`number` nMax) KPlayer:GetMaxAcceptDailyQuestCount()

* <h4 id="KPlayer_CanAcceptQuest">CanAcceptQuest</h4>

检查是否可以接受任务。

 > (`boolean` bCanAccept) KPlayer:CanAcceptQuest(`number` dwQuestID)

* <h4 id="KPlayer_GetProfession">GetProfession</h4>

获取生活技能信息。

 > (`table` tProfession) KPlayer:GetProfession(`number` nProfessionID)

* <h4 id="KPlayer_GetProfessionLevel">GetProfessionLevel</h4>

获取生活技能等级。

 > (`number` nLevel) KPlayer:GetProfessionLevel(`number` nProfessionID)

* <h4 id="KPlayer_GetProfessionMaxLevel">GetProfessionMaxLevel</h4>

获取生活技能最大等级。

 > (`number` nMaxLevel) KPlayer:GetProfessionMaxLevel(`number` nProfessionID)

* <h4 id="KPlayer_GetProfessionProficiency">GetProfessionProficiency</h4>

获取生活技能熟练度。

 > (`number` nProficiency) KPlayer:GetProfessionProficiency(`number` nProfessionID)

* <h4 id="KPlayer_GetProfessionBranch">GetProfessionBranch</h4>

获取生活技能分支。

 > (`number` nBranch) KPlayer:GetProfessionBranch(`number` nProfessionID)

* <h4 id="KPlayer_GetProfessionAdjustLevel">GetProfessionAdjustLevel</h4>

获取生活技能调整等级。

 > (`number` nAdjustLevel) KPlayer:GetProfessionAdjustLevel(`number` nProfessionID)

* <h4 id="KPlayer_IsProfessionLearnedByCraftID">IsProfessionLearnedByCraftID</h4>

通过制造 ID 检查是否学习了生活技能。

 > (`boolean` bLearned) KPlayer:IsProfessionLearnedByCraftID(`number` dwCraftID)

* <h4 id="KPlayer_CastProfessionSkill">CastProfessionSkill</h4>

施放生活技能。

 > (`void`) KPlayer:CastProfessionSkill(`number` dwRecipeID)

* <h4 id="KPlayer_IsRecipeLearned">IsRecipeLearned</h4>

检查是否学习了配方。

 > (`boolean` bLearned) KPlayer:IsRecipeLearned(`number` dwRecipeID)

* <h4 id="KPlayer_GetRecipe">GetRecipe</h4>

获取配方信息。

 > (`table` tRecipe) KPlayer:GetRecipe(`number` dwRecipeID)

* <h4 id="KPlayer_IsBookMemorized">IsBookMemorized</h4>

检查是否已阅读书籍。

 > (`boolean` bMemorized) KPlayer:IsBookMemorized(`number` dwBookID)

* <h4 id="KPlayer_GetBookList">GetBookList</h4>

获取已阅读的书籍列表。

 > (`table` tBookList) KPlayer:GetBookList()

* <h4 id="KPlayer_GetBookSegmentList">GetBookSegmentList</h4>

获取书籍章节列表。

 > (`table` tSegmentList) KPlayer:GetBookSegmentList(`number` dwBookID)

* <h4 id="KPlayer_GetFellowshipGroupInfo">GetFellowshipGroupInfo</h4>

获取好友分组信息。

 > (`table` tGroupInfo) KPlayer:GetFellowshipGroupInfo()

* <h4 id="KPlayer_GetFellowshipInfo">GetFellowshipInfo</h4>

获取好友信息。

 > (`table` tFellowship) KPlayer:GetFellowshipInfo(`number` dwPlayerID)

* <h4 id="KPlayer_GetFoeInfo">GetFoeInfo</h4>

获取仇人信息。

 > (`table` tFoeInfo) KPlayer:GetFoeInfo(`number` dwPlayerID)

* <h4 id="KPlayer_SetFellowshipRemark">SetFellowshipRemark</h4>

设置好友备注。

 > (`void`) KPlayer:SetFellowshipRemark(`number` dwPlayerID, `string` szRemark)

* <h4 id="KPlayer_GetRepresentID">GetRepresentID</h4>

获取外观 ID。

 > (`number` dwRepresentID) KPlayer:GetRepresentID(`number` nSlot)

* <h4 id="KPlayer_GetEquipIDArray">GetEquipIDArray</h4>

获取装备 ID 数组。

 > (`table` tEquipIDs) KPlayer:GetEquipIDArray()

* <h4 id="KPlayer_GetTotalEquipScore">GetTotalEquipScore</h4>

获取总装备分数。

 > (`number` nScore) KPlayer:GetTotalEquipScore()

* <h4 id="KPlayer_GetBaseEquipScore">GetBaseEquipScore</h4>

获取基础装备分数。

 > (`number` nScore) KPlayer:GetBaseEquipScore()

* <h4 id="KPlayer_GetStrengthEquipScore">GetStrengthEquipScore</h4>

获取精炼装备分数。

 > (`number` nScore) KPlayer:GetStrengthEquipScore()

* <h4 id="KPlayer_GetMountsEquipScore">GetMountsEquipScore</h4>

获取镶嵌（宝石）装备分数。

 > (`number` nScore) KPlayer:GetMountsEquipScore()

* <h4 id="KPlayer_CanBreakEquip">CanBreakEquip</h4>

检查装备是否可以分解。

 > (`boolean` bCanBreak) KPlayer:CanBreakEquip(`number` nPackage, `number` nIndex)

* <h4 id="KPlayer_GetReputation">GetReputation</h4>

获取与势力的声望值。

 > (`number` nReputation) KPlayer:GetReputation(`number` dwFactionID)

* <h4 id="KPlayer_GetReputeLevel">GetReputeLevel</h4>

获取与势力的声望等级。

 > (`number` nLevel) KPlayer:GetReputeLevel(`number` dwFactionID)

* <h4 id="KPlayer_IsAchievementAcquired">IsAchievementAcquired</h4>

检查是否获得成就。

 > (`boolean` bAcquired) KPlayer:IsAchievementAcquired(`number` dwAchievementID)

* <h4 id="KPlayer_GetAchievementRecord">GetAchievementRecord</h4>

获取成就记录。

 > (`table` tRecord) KPlayer:GetAchievementRecord(`number` dwAchievementID)

* <h4 id="KPlayer_IsDesignationPrefixAcquired">IsDesignationPrefixAcquired</h4>

检查是否获得称号前缀。

 > (`boolean` bAcquired) KPlayer:IsDesignationPrefixAcquired(`number` dwDesignationID)

* <h4 id="KPlayer_IsDesignationPostfixAcquired">IsDesignationPostfixAcquired</h4>

检查是否获得称号后缀。

 > (`boolean` bAcquired) KPlayer:IsDesignationPostfixAcquired(`number` dwDesignationID)

* <h4 id="KPlayer_OpenTalent">OpenTalent</h4>

打开天赋面板。

 > (`void`) KPlayer:OpenTalent()

* <h4 id="KPlayer_GetTalentInfo">GetTalentInfo</h4>

获取天赋信息。

 > (`table` tTalentInfo) KPlayer:GetTalentInfo()

* <h4 id="KPlayer_OpenVenation">OpenVenation</h4>

打开经脉面板。

 > (`void`) KPlayer:OpenVenation()

* <h4 id="KPlayer_Talk">Talk</h4>

发送聊天消息。

说明：
- 根据插件权限有频道限制
- 某些频道需要用户操作

 > (`void`) KPlayer:Talk(`number` nChannel, `string` szReceiver, `table` tContent)

* <h4 id="KPlayer_GetTalkData">GetTalkData</h4>

获取聊天数据。

 > (`table` tTalkData) KPlayer:GetTalkData()

* <h4 id="KPlayer_Jump">Jump</h4>

使玩家跳跃。

 > (`void`) KPlayer:Jump()

* <h4 id="KPlayer_StopCurrentAction">StopCurrentAction</h4>

停止当前动作。

 > (`void`) KPlayer:StopCurrentAction()

* <h4 id="KPlayer_CancelBuff">CancelBuff</h4>

取消 Buff。

 > (`void`) KPlayer:CancelBuff(`number` dwBuffID, `number` nLevel)

* <h4 id="KPlayer_WindowSelect">WindowSelect</h4>

执行窗口选择。

 > (`void`) KPlayer:WindowSelect(`number` nOption)

* <h4 id="KPlayer_CanDialog">CanDialog</h4>

检查是否可以对话。

 > (`boolean` bCanDialog) KPlayer:CanDialog()

* <h4 id="KPlayer_CanApplyDuel">CanApplyDuel</h4>

检查是否可以申请切磋。

 > (`boolean` bCanApply) KPlayer:CanApplyDuel(`number` dwTargetID)

* <h4 id="KPlayer_CanAddFoe">CanAddFoe</h4>

检查是否可以添加为仇人。

 > (`boolean` bCanAdd) KPlayer:CanAddFoe(`number` dwTargetID)

* <h4 id="KPlayer_GetMaxExamPrint">GetMaxExamPrint</h4>

获取最大试炼印记数。

 > (`number` nMax) KPlayer:GetMaxExamPrint()

* <h4 id="KPlayer_GetExamPrintRemainSpace">GetExamPrintRemainSpace</h4>

获取试炼印记剩余空间。

 > (`number` nRemain) KPlayer:GetExamPrintRemainSpace()

* <h4 id="KPlayer_GetMapVisitFlag">GetMapVisitFlag</h4>

获取地图访问标记。

 > (`number` nFlag) KPlayer:GetMapVisitFlag(`number` dwMapID)

* <h4 id="KPlayer_SatisfyRequire">SatisfyRequire</h4>

检查是否满足需求。

 > (`boolean` bSatisfy) KPlayer:SatisfyRequire(`table` tRequire)

* <h4 id="KPlayer_GetMaxVigor">GetMaxVigor</h4>

获取最大活力值。

 > (`number` nMaxVigor) KPlayer:GetMaxVigor()

* <h4 id="KPlayer_GetVigorRemainSpace">GetVigorRemainSpace</h4>

获取活力剩余空间。

 > (`number` nRemain) KPlayer:GetVigorRemainSpace()

---

## 被屏蔽的方法

以下方法在 addon 环境中被屏蔽，无法使用：

| 方法 | 说明 |
|------|------|
| `TurnTo` | ⚠️ 被屏蔽 - 转向指定方向 |
| `FinishQuest` | ⚠️ 被屏蔽 - 完成任务 |
| `GetBlackListInfo` | ⚠️ 被屏蔽 - 获取黑名单信息 |
| `DelBlackList` | ⚠️ 被屏蔽 - 从黑名单删除 |
| `GetAroundPlayerID` | ⚠️ 被屏蔽 - 获取周围玩家 ID |
| `UpdateFellowshipInfo` | ⚠️ 被屏蔽 - 更新好友信息 |
| `SetTitle` | ⚠️ 被屏蔽 - 设置称号 |
| `ApplyDuel` | ⚠️ 被屏蔽 - 申请切磋 |
| `AddBlackList` | ⚠️ 被屏蔽 - 添加到黑名单 |
| `AcceptQuest` | ⚠️ 被屏蔽 - 接受任务 |
