# Constants Part 4 - Guild and Social

Game constants for guild (Tong), party, social, and fellowship systems.

---

## TONG_OPERATION_INDEX {#TONG_OPERATION_INDEX}

Guild operation index constants.

| Constant | Description |
|----------|-------------|
| `TONG_OPERATION_INDEX.INVALID` | Invalid |
| `TONG_OPERATION_INDEX.APPLY` | Apply |
| `TONG_OPERATION_INDEX.ACCEPT` | Accept |
| `TONG_OPERATION_INDEX.REFUSE` | Refuse |
| `TONG_OPERATION_INDEX.KICK` | Kick |
| `TONG_OPERATION_INDEX.LEAVE` | Leave |
| `TONG_OPERATION_INDEX.DISMISS` | Dismiss |
| `TONG_OPERATION_INDEX.CHANGE_MASTER` | Change master |
| `TONG_OPERATION_INDEX.CHANGE_GROUP` | Change group |
| `TONG_OPERATION_INDEX.CHANGE_REMARK` | Change remark |
| `TONG_OPERATION_INDEX.INVITE` | Invite |
| `TONG_OPERATION_INDEX.INVITE_RESPOND` | Invite respond |
| `TONG_OPERATION_INDEX.QUERY_TONG_MEMBER_LIST` | Query tong member list |
| `TONG_OPERATION_INDEX.SETTING` | Setting |
| `TONG_OPERATION_INDEX.SPEAK_FLAG` | Speak flag |
| `TONG_OPERATION_INDEX.TONG_RENAME` | Tong rename |
| `TONG_OPERATION_INDEX.REQUEST_BASE_INFO` | Request base info |
| `TONG_OPERATION_INDEX.UPGRADE` | Upgrade |
| `TONG_OPERATION_INDEX.ACTIVE_TECH` | Active tech |
| `TONG_OPERATION_INDEX.REQUEST_TECH_INFO` | Request tech info |
| `TONG_OPERATION_INDEX.ADD_FUND` | Add fund |
| `TONG_OPERATION_INDEX.REQUEST_DEVELOP_INFO` | Request develop info |
| `TONG_OPERATION_INDEX.REQUEST_REPUTE_INFO` | Request repute info |
| `TONG_OPERATION_INDEX.REQUEST_EVENT_LOG` | Request event log |
| `TONG_OPERATION_INDEX.REQUEST_ROSTER_INFO` | Request roster info |
| `TONG_OPERATION_INDEX.REQUEST_GROUP_INFO` | Request group info |
| `TONG_OPERATION_INDEX.EDIT_GROUP_INFO` | Edit group info |
| `TONG_OPERATION_INDEX.EDIT_TITLE` | Edit title |
| `TONG_OPERATION_INDEX.REQUEST_OPERATION_RECORD` | Request operation record |
| `TONG_OPERATION_INDEX.CHANGE_SALARY_LOG` | Change salary log |
| `TONG_OPERATION_INDEX.OPERATION_SALARY` | Operation salary |
| `TONG_OPERATION_INDEX.REQUEST_SALARY_INFO` | Request salary info |
| `TONG_OPERATION_INDEX.TAKE_SALARY_AWARD` | Take salary award |

---

## TONG_EVENT_CODE {#TONG_EVENT_CODE}

Guild event codes.

| Constant | Description |
|----------|-------------|
| `TONG_EVENT_CODE.CREATED` | Created |
| `TONG_EVENT_CODE.DISMISSED` | Dismissed |
| `TONG_EVENT_CODE.ADD_MEMBER` | Add member |
| `TONG_EVENT_CODE.DEL_MEMBER` | Del member |
| `TONG_EVENT_CODE.CHANGE_MASTER` | Change master |
| `TONG_EVENT_CODE.CHANGE_PRESTIGE` | Change prestige |
| `TONG_EVENT_CODE.CHANGE_MAX_MEMBER_COUNT` | Change max member count |
| `TONG_EVENT_CODE.CHANGE_LEVEL` | Change level |
| `TONG_EVENT_CODE.CHANGE_DEVELOP_POINT` | Change develop point |
| `TONG_EVENT_CODE.CHANGE_STATE` | Change state |
| `TONG_EVENT_CODE.CHANGE_MEMBER_GROUP` | Change member group |
| `TONG_EVENT_CODE.CHANGE_GROUP_BASE_INFO` | Change group base info |
| `TONG_EVENT_CODE.CHANGE_GROUP_RIGHT` | Change group right |
| `TONG_EVENT_CODE.CHANGE_MEMBER_REMARK` | Change member remark |
| `TONG_EVENT_CODE.UPDATE_MEMBER` | Update member |
| `TONG_EVENT_CODE.CHANGE_FUND` | Change fund |
| `TONG_EVENT_CODE.CHANGE_TECH` | Change tech |
| `TONG_EVENT_CODE.CHANGE_MEMBER_CASH` | Change member cash |
| `TONG_EVENT_CODE.GUILD_WAR` | Guild war |
| `TONG_EVENT_CODE.GET_ACTIVITY_AWARD` | Get activity award |
| `TONG_EVENT_CODE.CHANGE_ONLINE_COUNT` | Change online count |
| `TONG_EVENT_CODE.FINISH_SCRIPT` | Finish script |
| `TONG_EVENT_CODE.MERGE_APPLY` | Merge apply |
| `TONG_EVENT_CODE.MERGE_DEAL` | Merge deal |
| `TONG_EVENT_CODE.SALARY_AWARD` | Salary award |

---

## TONG_HISTORY_TYPE {#TONG_HISTORY_TYPE}

Guild history type constants.

| Constant | Description |
|----------|-------------|
| `TONG_HISTORY_TYPE.INVALID` | Invalid |
| `TONG_HISTORY_TYPE.MASTER_CHANGE` | Master change |
| `TONG_HISTORY_TYPE.MEMBER_IN` | Member in |
| `TONG_HISTORY_TYPE.MEMBER_OUT` | Member out |
| `TONG_HISTORY_TYPE.FUND_ADD` | Fund add |
| `TONG_HISTORY_TYPE.FUND_COST` | Fund cost |
| `TONG_HISTORY_TYPE.FUND_COST_ALL` | Fund cost all |
| `TONG_HISTORY_TYPE.DEVELOP` | Develop |
| `TONG_HISTORY_TYPE.FUND_ADD_FROM_MEMBER` | Fund add from member |

---

## TONG_STATE {#TONG_STATE}

Guild state constants.

| Constant | Description |
|----------|-------------|
| `TONG_STATE.INVALID` | Invalid |
| `TONG_STATE.NORMAL` | Normal |
| `TONG_STATE.IN_WAR` | In war |

---

## TONG_DIPLOMACY_RELATION {#TONG_DIPLOMACY_RELATION}

Guild diplomacy relation constants.

| Constant | Description |
|----------|-------------|
| `TONG_DIPLOMACY_RELATION.INVALID` | Invalid |
| `TONG_DIPLOMACY_RELATION.ENEMY` | Enemy |
| `TONG_DIPLOMACY_RELATION.NEUTRAL` | Neutral |
| `TONG_DIPLOMACY_RELATION.ALLY` | Ally |

---

## TONG_DIPLOMACY_RESPOND_CODE {#TONG_DIPLOMACY_RESPOND_CODE}

Guild diplomacy respond codes.

| Constant | Description |
|----------|-------------|
| `TONG_DIPLOMACY_RESPOND_CODE.INVALID` | Invalid |
| `TONG_DIPLOMACY_RESPOND_CODE.SUCCESS` | Success |
| `TONG_DIPLOMACY_RESPOND_CODE.FAILED` | Failed |
| `TONG_DIPLOMACY_RESPOND_CODE.REFUSE` | Refuse |
| `TONG_DIPLOMACY_RESPOND_CODE.NO_PERMISSION` | No permission |
| `TONG_DIPLOMACY_RESPOND_CODE.TONG_NOT_EXIST` | Tong not exist |
| `TONG_DIPLOMACY_RESPOND_CODE.ALREADY_ALLY` | Already ally |
| `TONG_DIPLOMACY_RESPOND_CODE.ALLY_LIST_FULL` | Ally list full |
| `TONG_DIPLOMACY_RESPOND_CODE.TARGET_ALLY_LIST_FULL` | Target ally list full |
| `TONG_DIPLOMACY_RESPOND_CODE.ALREADY_ENEMY` | Already enemy |
| `TONG_DIPLOMACY_RESPOND_CODE.ENEMY_LIST_FULL` | Enemy list full |
| `TONG_DIPLOMACY_RESPOND_CODE.NOT_IN_ALLY` | Not in ally |
| `TONG_DIPLOMACY_RESPOND_CODE.NOT_IN_ENEMY` | Not in enemy |
| `TONG_DIPLOMACY_RESPOND_CODE.SELF_TONG` | Self tong |
| `TONG_DIPLOMACY_RESPOND_CODE.SAME_CAMP` | Same camp |

---

## PARTY_NOTIFY_CODE {#PARTY_NOTIFY_CODE}

Party notification codes.

| Constant | Description |
|----------|-------------|
| `PARTY_NOTIFY_CODE.INVALID` | Invalid |
| `PARTY_NOTIFY_CODE.TEAM_CREATED` | Team created |
| `PARTY_NOTIFY_CODE.TEAM_DISBANDED` | Team disbanded |
| `PARTY_NOTIFY_CODE.INVITE_MEMBER` | Invite member |
| `PARTY_NOTIFY_CODE.ACCEPT_MEMBER` | Accept member |
| `PARTY_NOTIFY_CODE.REFUSE_MEMBER` | Refuse member |
| `PARTY_NOTIFY_CODE.MEMBER_ADDED` | Member added |
| `PARTY_NOTIFY_CODE.MEMBER_DELETED` | Member deleted |
| `PARTY_NOTIFY_CODE.MEMBER_NOT_ONLINE` | Member not online |
| `PARTY_NOTIFY_CODE.MEMBER_IN_ANOTHER_PARTY` | Member in another party |
| `PARTY_NOTIFY_CODE.KICK_MEMBER` | Kick member |
| `PARTY_NOTIFY_CODE.LEAVE_PARTY` | Leave party |
| `PARTY_NOTIFY_CODE.YOU_ARE_KICKED` | You are kicked |
| `PARTY_NOTIFY_CODE.DISBANDED` | Disbanded |
| `PARTY_NOTIFY_CODE.CHANGE_LEADER` | Change leader |
| `PARTY_NOTIFY_CODE.YOU_BECOME_LEADER` | You become leader |
| `PARTY_NOTIFY_CODE.APPLY_TO_JOIN` | Apply to join |
| `PARTY_NOTIFY_CODE.APPLY_BY_INVITE` | Apply by invite |
| `PARTY_NOTIFY_CODE.APPLY_TO_JOIN_REFUSED` | Apply to join refused |
| `PARTY_NOTIFY_CODE.APPLY_CANCEL` | Apply cancel |
| `PARTY_NOTIFY_CODE.PARTY_FULL` | Party full |
| `PARTY_NOTIFY_CODE.RAID_FULL` | Raid full |
| `PARTY_NOTIFY_CODE.CHANGE_TEAM_INDEX` | Change team index |
| `PARTY_NOTIFY_CODE.NOT_IN_PARTY` | Not in party |
| `PARTY_NOTIFY_CODE.NO_AUTHORITY` | No authority |
| `PARTY_NOTIFY_CODE.INVALID_LEADER` | Invalid leader |
| `PARTY_NOTIFY_CODE.CANNOT_FORM_TEAM_IN_COPY_MAP` | Cannot form team in copy map |
| `PARTY_NOTIFY_CODE.MEMBER_IN_ANOTHER_CAMP` | Member in another camp |
| `PARTY_NOTIFY_CODE.CAPTAIN_NOT_ACCEPT_RECRUIT` | Captain not accept recruit |
| `PARTY_NOTIFY_CODE.CANCEL_AUTO_ACCEPT` | Cancel auto accept |
| `PARTY_NOTIFY_CODE.DISBAND_FORCE` | Disband force |
| `PARTY_NOTIFY_CODE.MEMBER_ONLINE` | Member online |
| `PARTY_NOTIFY_CODE.MEMBER_OFFLINE` | Member offline |
| `PARTY_NOTIFY_CODE.YOU_CREATE_TEAM` | You create team |
| `PARTY_NOTIFY_CODE.REFUSE_RECRUIT` | Refuse recruit |
| `PARTY_NOTIFY_CODE.UPDATE_MEMBER` | Update member |
| `PARTY_NOTIFY_CODE.MEMBER_CHANGE_MAP` | Member change map |
| `PARTY_NOTIFY_CODE.LOCK_TEAM_PANEL` | Lock team panel |
| `PARTY_NOTIFY_CODE.UNLOCK_TEAM_PANEL` | Unlock team panel |
| `PARTY_NOTIFY_CODE.QUERY_MEMBER_POSITION` | Query member position |
| `PARTY_NOTIFY_CODE.SYNC_MEMBER_POSITION` | Sync member position |
| `PARTY_NOTIFY_CODE.CANNOT_KICK_CD` | Cannot kick cooldown |
| `PARTY_NOTIFY_CODE.CANNOT_LEAVE_RAID` | Cannot leave raid |
| `PARTY_NOTIFY_CODE.TARGET_HAS_FORBID_JOIN` | Target has forbid join |
| `PARTY_NOTIFY_CODE.APPLY_TIMEOUT` | Apply timeout |

---

## TEAM_AUTHORITY_TYPE {#TEAM_AUTHORITY_TYPE}

Team authority type constants.

| Constant | Description |
|----------|-------------|
| `TEAM_AUTHORITY_TYPE.INVALID` | Invalid |
| `TEAM_AUTHORITY_TYPE.LEADER` | Leader |
| `TEAM_AUTHORITY_TYPE.MARK` | Mark |
| `TEAM_AUTHORITY_TYPE.LOOT` | Loot |

---

## FELLOWSHIP_RESPOND_CODE {#FELLOWSHIP_RESPOND_CODE}

Fellowship respond codes.

| Constant | Description |
|----------|-------------|
| `FELLOWSHIP_RESPOND_CODE.INVALID` | Invalid |
| `FELLOWSHIP_RESPOND_CODE.SUCCESS` | Success |
| `FELLOWSHIP_RESPOND_CODE.FAILED` | Failed |
| `FELLOWSHIP_RESPOND_CODE.NOT_ONLINE` | Not online |
| `FELLOWSHIP_RESPOND_CODE.REQUEST_GROUP_NAME` | Request group name |
| `FELLOWSHIP_RESPOND_CODE.GROUP_NOT_EXIST` | Group not exist |
| `FELLOWSHIP_RESPOND_CODE.ALLIANCE_NOT_EXIST` | Alliance not exist |
| `FELLOWSHIP_RESPOND_CODE.GROUP_FULL` | Group full |
| `FELLOWSHIP_RESPOND_CODE.NOT_IN_FELLOWSHIP` | Not in fellowship |
| `FELLOWSHIP_RESPOND_CODE.ALREADY_IN_FELLOWSHIP` | Already in fellowship |
| `FELLOWSHIP_RESPOND_CODE.FELLOWSHIP_LIST_FULL` | Fellowship list full |
| `FELLOWSHIP_RESPOND_CODE.BLACK_LIST_FULL` | Black list full |
| `FELLOWSHIP_RESPOND_CODE.ALREADY_IN_BLACK_LIST` | Already in black list |
| `FELLOWSHIP_RESPOND_CODE.NOT_IN_BLACK_LIST` | Not in black list |
| `FELLOWSHIP_RESPOND_CODE.FOE_FULL` | Foe full |
| `FELLOWSHIP_RESPOND_CODE.ALREADY_IN_FOE` | Already in foe |
| `FELLOWSHIP_RESPOND_CODE.GROUP_NAME_EXIST` | Group name exist |
| `FELLOWSHIP_RESPOND_CODE.GROUP_NAME_INVALID` | Group name invalid |
| `FELLOWSHIP_RESPOND_CODE.TARGET_NAME_INVALID` | Target name invalid |
| `FELLOWSHIP_RESPOND_CODE.GROUP_NAME_TOO_LONG` | Group name too long |
| `FELLOWSHIP_RESPOND_CODE.CANNOT_BE_SELF` | Cannot be self |
| `FELLOWSHIP_RESPOND_CODE.ADD_FOE_IN_WAR` | Add foe in war |

---

## PLAYER_TALK_CHANNEL {#PLAYER_TALK_CHANNEL}

Player talk channel constants.

| Constant | Value | Description |
|----------|-------|-------------|
| `PLAYER_TALK_CHANNEL.LOCAL` | 1 | Local channel (近聊) |
| `PLAYER_TALK_CHANNEL.TEAM` | 2 | Team channel (队伍) |
| `PLAYER_TALK_CHANNEL.RAID` | 3 | Raid channel (团队) |
| `PLAYER_TALK_CHANNEL.TONG` | 4 | Guild channel (帮会) |
| `PLAYER_TALK_CHANNEL.FORCE` | 5 | Force channel (门派) |
| `PLAYER_TALK_CHANNEL.CAMP` | 6 | Camp channel (阵营) |
| `PLAYER_TALK_CHANNEL.WORLD` | 7 | World channel (世界) |
| `PLAYER_TALK_CHANNEL.WHISPER` | 8 | Whisper channel (密聊) |
| `PLAYER_TALK_CHANNEL.SENCE` | 9 | Scene channel (场景) |
| `PLAYER_TALK_CHANNEL.NEARBY` | 10 | Nearby channel (附近) |
| `PLAYER_TALK_CHANNEL.BATTLE_FIELD` | 11 | Battle field channel (战场) |

---

## PLAYER_TALK_ERROR {#PLAYER_TALK_ERROR}

Player talk error codes.

| Constant | Description |
|----------|-------------|
| `PLAYER_TALK_ERROR.SUCCESS` | Success |
| `PLAYER_TALK_ERROR.INVALID_PARAMETER` | Invalid parameter |
| `PLAYER_TALK_ERROR.NOT_IN_TEAM` | Not in team |
| `PLAYER_TALK_ERROR.NOT_IN_RAID` | Not in raid |
| `PLAYER_TALK_ERROR.NOT_IN_TONG` | Not in tong |
| `PLAYER_TALK_ERROR.NOT_IN_BATTLE_FIELD` | Not in battle field |
| `PLAYER_TALK_ERROR.INVALID_CHANNEL` | Invalid channel |
| `PLAYER_TALK_ERROR.EMPTY_RECEIVER` | Empty receiver |
| `PLAYER_TALK_ERROR.RECEIVER_NOT_EXIST` | Receiver not exist |
| `PLAYER_TALK_ERROR.RECEIVER_NOT_ONLINE` | Receiver not online |
| `PLAYER_TALK_ERROR.IN_BLACKLIST` | In blacklist |
| `PLAYER_TALK_ERROR.NOT_ENOUGH_MONEY` | Not enough money |
| `PLAYER_TALK_ERROR.TOO_LONG` | Too long |
| `PLAYER_TALK_ERROR.TOO_FREQUENT` | Too frequent |
| `PLAYER_TALK_ERROR.FORBID_TALK` | Forbid talk |
| `PLAYER_TALK_ERROR.NOT_ENOUGH_LEVEL` | Not enough level |
| `PLAYER_TALK_ERROR.EMPTY_CONTENT` | Empty content |

---

## RELATION_TYPE {#RELATION_TYPE}

Relation type constants.

| Constant | Description |
|----------|-------------|
| `RELATION_TYPE.INVALID` | Invalid |
| `RELATION_TYPE.ALL` | All |
| `RELATION_TYPE.PARTY` | Party |
| `RELATION_TYPE.TONG` | Tong |
| `RELATION_TYPE.ALLY` | Ally |
| `RELATION_TYPE.ENEMY` | Enemy |
| `RELATION_TYPE.NEUTRALITY` | Neutrality |
| `RELATION_TYPE.SELF` | Self |

---

## CAMP {#CAMP}

Camp constants.

| Constant | Description |
|----------|-------------|
| `CAMP.INVALID` | Invalid |
| `CAMP.GOOD` | Good (浩气盟) |
| `CAMP.EVIL` | Evil (恶人谷) |
| `CAMP.NEUTRAL` | Neutral (中立) |

---

## MENTOR_RECORD_STATE {#MENTOR_RECORD_STATE}

Mentor record state constants.

| Constant | Description |
|----------|-------------|
| `MENTOR_RECORD_STATE.INVALID` | Invalid |
| `MENTOR_RECORD_STATE.UNDER_MENTOR_SHIP` | Under mentorship |
| `MENTOR_RECORD_STATE.WAITING_FOR_GRADUATE` | Waiting for graduate |
| `MENTOR_RECORD_STATE.GRADUATED` | Graduated |

---

## CHARACTER_GENDER {#CHARACTER_GENDER}

Character gender constants.

| Constant | Description |
|----------|-------------|
| `CHARACTER_GENDER.MALE` | Male |
| `CHARACTER_GENDER.FEMALE` | Female |

---

## FORCE_TYPE {#FORCE_TYPE}

Force (sect/school) type constants.

| Constant | Value | Description |
|----------|-------|-------------|
| `FORCE_TYPE.INVALID` | 0 | Invalid |
| `FORCE_TYPE.SHAOLIN` | 1 | Shaolin (少林) |
| `FORCE_TYPE.WANHUA` | 2 | Wanhua (万花) |
| `FORCE_TYPE.TIANCE` | 3 | Tiance (天策) |
| `FORCE_TYPE.CHUNYANG` | 4 | Chunyang (纯阳) |
| `FORCE_TYPE.QIXIU` | 5 | Qixiu (七秀) |
| `FORCE_TYPE.WUDU` | 6 | Wudu (五毒) |
| `FORCE_TYPE.TANGJIA` | 7 | Tangjia (唐家堡) |
| `FORCE_TYPE.CANGJIAN` | 8 | Cangjian (藏剑) |
| `FORCE_TYPE.GAIBANG` | 9 | Gaibang (丐帮) |
| `FORCE_TYPE.MINGJIAO` | 10 | Mingjiao (明教) |
| `FORCE_TYPE.DINGJING` | 21 | Dingjing (丁敬) |
| `FORCE_TYPE.CHANGGEI` | 22 | Changgei (长歌) |
| `FORCE_TYPE.DOMINATOR` | 23 | Dominator (霸刀) |
| `FORCE_TYPE.PENGLAIGE` | 24 | Penglaige (蓬莱) |
| `FORCE_TYPE.LINGXUEGE` | 25 | Lingxuege (凌雪阁) |
| `FORCE_TYPE.YANJUN` | 26 | Yanjun (衍天宗) |
| `FORCE_TYPE.BEIJUN` | 27 | Beijun (北天药宗) |
| `FORCE_TYPE.DUAN` | 28 | Duan (段氏) |
| `FORCE_TYPE.TOTAL` | 99 | Total |

---

## PK_STATE {#PK_STATE}

PK state constants.

| Constant | Description |
|----------|-------------|
| `PK_STATE.CLOSE` | Close (PK关闭) |
| `PK_STATE.OPEN` | Open (PK开启) |

---

## ASSIST_NEWBIE_CODE {#ASSIST_NEWBIE_CODE}

Assist newbie response codes.

| Constant | Description |
|----------|-------------|
| `ASSIST_NEWBIE_CODE.SUCCESS` | Success |
| `ASSIST_NEWBIE_CODE.ERROR` | Error |
| `ASSIST_NEWBIE_CODE.SELF_NOT_EXIST` | Self not exist |
| `ASSIST_NEWBIE_CODE.TARGET_NOT_EXIST` | Target not exist |
| `ASSIST_NEWBIE_CODE.NOT_QUALIFIED` | Not qualified |
| `ASSIST_NEWBIE_CODE.TOO_FAR` | Too far |
| `ASSIST_NEWBIE_CODE.NOT_SAME_CAMP` | Not same camp |
| `ASSIST_NEWBIE_CODE.NEWBIE_LEFT` | Newbie left |
| `ASSIST_NEWBIE_CODE.SENIOR_LEFT` | Senior left |
| `ASSIST_NEWBIE_CODE.ALREADY_ASSISTING` | Already assisting |
| `ASSIST_NEWBIE_CODE.SENIOR_ASSISTING_COUNT_LIMIT` | Senior assisting count limit |

---

## See Also

- [Constants Part 3 - Items](./Constants3.md)
- [Constants Part 5 - Auction and Mail](./Constants5.md)
