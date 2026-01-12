# Constants Part 6 - Battlefield, Arena and PvP

Game constants for battlefield, arena, PvP, and combat systems.

---

## BATTLE_FIELD_NOTIFY_TYPE {#BATTLE_FIELD_NOTIFY_TYPE}

Battlefield notification type constants.

| Constant | Description |
|----------|-------------|
| `BATTLE_FIELD_NOTIFY_TYPE.INVALID` | Invalid |
| `BATTLE_FIELD_NOTIFY_TYPE.ENTER_QUEUE` | Enter queue |
| `BATTLE_FIELD_NOTIFY_TYPE.LEAVE_QUEUE` | Leave queue |
| `BATTLE_FIELD_NOTIFY_TYPE.MATCH_SUCCESS` | Match success |
| `BATTLE_FIELD_NOTIFY_TYPE.CANCEL_MATCH` | Cancel match |
| `BATTLE_FIELD_NOTIFY_TYPE.ENTER_BF` | Enter battlefield |
| `BATTLE_FIELD_NOTIFY_TYPE.LEAVE_BF` | Leave battlefield |
| `BATTLE_FIELD_NOTIFY_TYPE.BF_END` | Battlefield end |
| `BATTLE_FIELD_NOTIFY_TYPE.UPDATE_SCORE` | Update score |
| `BATTLE_FIELD_NOTIFY_TYPE.UPDATE_KILL` | Update kill |
| `BATTLE_FIELD_NOTIFY_TYPE.UPDATE_DEATH` | Update death |
| `BATTLE_FIELD_NOTIFY_TYPE.UPDATE_DAMAGE` | Update damage |
| `BATTLE_FIELD_NOTIFY_TYPE.UPDATE_HEAL` | Update heal |
| `BATTLE_FIELD_NOTIFY_TYPE.UPDATE_ASSIST` | Update assist |
| `BATTLE_FIELD_NOTIFY_TYPE.WIN` | Win |
| `BATTLE_FIELD_NOTIFY_TYPE.LOSE` | Lose |
| `BATTLE_FIELD_NOTIFY_TYPE.DRAW` | Draw |
| `BATTLE_FIELD_NOTIFY_TYPE.QUEUE_TIMEOUT` | Queue timeout |
| `BATTLE_FIELD_NOTIFY_TYPE.KICKED` | Kicked |
| `BATTLE_FIELD_NOTIFY_TYPE.DESERTER` | Deserter |
| `BATTLE_FIELD_NOTIFY_TYPE.PREPARE_END` | Prepare end |

---

## BATTLE_FIELD_RESPOND_CODE {#BATTLE_FIELD_RESPOND_CODE}

Battlefield respond codes.

| Constant | Description |
|----------|-------------|
| `BATTLE_FIELD_RESPOND_CODE.INVALID` | Invalid |
| `BATTLE_FIELD_RESPOND_CODE.SUCCESS` | Success |
| `BATTLE_FIELD_RESPOND_CODE.FAILED` | Failed |
| `BATTLE_FIELD_RESPOND_CODE.IN_QUEUE` | In queue |
| `BATTLE_FIELD_RESPOND_CODE.NOT_IN_QUEUE` | Not in queue |
| `BATTLE_FIELD_RESPOND_CODE.IN_BATTLEFIELD` | In battlefield |
| `BATTLE_FIELD_RESPOND_CODE.NOT_IN_BATTLEFIELD` | Not in battlefield |
| `BATTLE_FIELD_RESPOND_CODE.LEVEL_TOO_LOW` | Level too low |
| `BATTLE_FIELD_RESPOND_CODE.LEVEL_TOO_HIGH` | Level too high |
| `BATTLE_FIELD_RESPOND_CODE.NOT_ENOUGH_PLAYER` | Not enough player |
| `BATTLE_FIELD_RESPOND_CODE.MAP_FULL` | Map full |
| `BATTLE_FIELD_RESPOND_CODE.CAMP_FULL` | Camp full |
| `BATTLE_FIELD_RESPOND_CODE.IN_COPY` | In copy map |
| `BATTLE_FIELD_RESPOND_CODE.IN_TRANSPORT` | In transport |
| `BATTLE_FIELD_RESPOND_CODE.DEAD` | Dead |
| `BATTLE_FIELD_RESPOND_CODE.IN_COMBAT` | In combat |
| `BATTLE_FIELD_RESPOND_CODE.CD_NOT_READY` | Cooldown not ready |
| `BATTLE_FIELD_RESPOND_CODE.NOT_TEAM_LEADER` | Not team leader |
| `BATTLE_FIELD_RESPOND_CODE.TEAM_MEMBER_NOT_IN_SAME_MAP` | Team member not in same map |
| `BATTLE_FIELD_RESPOND_CODE.TEAM_MEMBER_LEVEL_ERROR` | Team member level error |
| `BATTLE_FIELD_RESPOND_CODE.TEAM_MEMBER_IN_QUEUE` | Team member in queue |
| `BATTLE_FIELD_RESPOND_CODE.TEAM_MEMBER_IN_BF` | Team member in battlefield |
| `BATTLE_FIELD_RESPOND_CODE.DESERTER_DEBUFF` | Deserter debuff |
| `BATTLE_FIELD_RESPOND_CODE.NOT_SAME_CAMP` | Not same camp |
| `BATTLE_FIELD_RESPOND_CODE.NOT_ENOUGH_REPUTATION` | Not enough reputation |

---

## ARENA_RESPOND_CODE {#ARENA_RESPOND_CODE}

Arena respond codes.

| Constant | Description |
|----------|-------------|
| `ARENA_RESPOND_CODE.INVALID` | Invalid |
| `ARENA_RESPOND_CODE.SUCCESS` | Success |
| `ARENA_RESPOND_CODE.FAILED` | Failed |
| `ARENA_RESPOND_CODE.IN_QUEUE` | In queue |
| `ARENA_RESPOND_CODE.NOT_IN_QUEUE` | Not in queue |
| `ARENA_RESPOND_CODE.IN_ARENA` | In arena |
| `ARENA_RESPOND_CODE.NOT_IN_ARENA` | Not in arena |
| `ARENA_RESPOND_CODE.LEVEL_TOO_LOW` | Level too low |
| `ARENA_RESPOND_CODE.NOT_IN_TEAM` | Not in team |
| `ARENA_RESPOND_CODE.NOT_TEAM_LEADER` | Not team leader |
| `ARENA_RESPOND_CODE.TEAM_SIZE_ERROR` | Team size error |
| `ARENA_RESPOND_CODE.TEAM_MEMBER_NOT_READY` | Team member not ready |
| `ARENA_RESPOND_CODE.TEAM_MEMBER_IN_QUEUE` | Team member in queue |
| `ARENA_RESPOND_CODE.TEAM_MEMBER_IN_ARENA` | Team member in arena |
| `ARENA_RESPOND_CODE.TEAM_MEMBER_LEVEL_ERROR` | Team member level error |
| `ARENA_RESPOND_CODE.CD_NOT_READY` | Cooldown not ready |
| `ARENA_RESPOND_CODE.IN_COPY` | In copy map |
| `ARENA_RESPOND_CODE.DEAD` | Dead |
| `ARENA_RESPOND_CODE.TEAM_FULL` | Team full |
| `ARENA_RESPOND_CODE.ALREADY_IN_TEAM` | Already in team |
| `ARENA_RESPOND_CODE.NOT_FIND_TEAM` | Not find team |
| `ARENA_RESPOND_CODE.TEAM_NOT_IN_QUEUE` | Team not in queue |
| `ARENA_RESPOND_CODE.SCORE_TOO_HIGH` | Score too high |
| `ARENA_RESPOND_CODE.SCORE_TOO_LOW` | Score too low |
| `ARENA_RESPOND_CODE.TODAY_LIMIT` | Today limit |

---

## ARENA_TYPE {#ARENA_TYPE}

Arena type constants.

| Constant | Description |
|----------|-------------|
| `ARENA_TYPE.INVALID` | Invalid |
| `ARENA_TYPE.ARENA_2V2` | 2v2 Arena |
| `ARENA_TYPE.ARENA_3V3` | 3v3 Arena |
| `ARENA_TYPE.ARENA_5V5` | 5v5 Arena |

---

## PLAYER_ARENA_TYPE {#PLAYER_ARENA_TYPE}

Player arena type constants.

| Constant | Description |
|----------|-------------|
| `PLAYER_ARENA_TYPE.INVALID` | Invalid |
| `PLAYER_ARENA_TYPE.LADDER_2V2` | Ladder 2v2 |
| `PLAYER_ARENA_TYPE.LADDER_3V3` | Ladder 3v3 |
| `PLAYER_ARENA_TYPE.LADDER_5V5` | Ladder 5v5 |
| `PLAYER_ARENA_TYPE.PVP_MATCH` | PvP match |

---

## PK_STATE {#PK_STATE}

PK state constants.

| Constant | Description |
|----------|-------------|
| `PK_STATE.CLOSE` | Close (PK disabled) |
| `PK_STATE.OPEN` | Open (PK enabled) |

---

## PK_RESPOND {#PK_RESPOND}

PK respond codes.

| Constant | Description |
|----------|-------------|
| `PK_RESPOND.INVALID` | Invalid |
| `PK_RESPOND.SUCCESS` | Success |
| `PK_RESPOND.FAILED` | Failed |
| `PK_RESPOND.IN_SAFE_ZONE` | In safe zone |
| `PK_RESPOND.IN_PVE_MAP` | In PvE map |
| `PK_RESPOND.CAMP_NOT_ALLOW` | Camp not allow |

---

## CAMP_RESULT_CODE {#CAMP_RESULT_CODE}

Camp result codes.

| Constant | Description |
|----------|-------------|
| `CAMP_RESULT_CODE.INVALID` | Invalid |
| `CAMP_RESULT_CODE.SUCCESS` | Success |
| `CAMP_RESULT_CODE.FAILED` | Failed |
| `CAMP_RESULT_CODE.IN_TONG` | In guild |
| `CAMP_RESULT_CODE.LEVEL_TOO_LOW` | Level too low |
| `CAMP_RESULT_CODE.PRESTIGE_TOO_LOW` | Prestige too low |
| `CAMP_RESULT_CODE.ALREADY_IN_CAMP` | Already in camp |
| `CAMP_RESULT_CODE.CD_NOT_READY` | Cooldown not ready |
| `CAMP_RESULT_CODE.NOT_ENOUGH_MONEY` | Not enough money |
| `CAMP_RESULT_CODE.NOT_IN_CAMP` | Not in camp |

---

## CORPS_RESPOND_CODE {#CORPS_RESPOND_CODE}

Corps respond codes.

| Constant | Description |
|----------|-------------|
| `CORPS_RESPOND_CODE.INVALID` | Invalid |
| `CORPS_RESPOND_CODE.SUCCESS` | Success |
| `CORPS_RESPOND_CODE.FAILED` | Failed |
| `CORPS_RESPOND_CODE.NOT_IN_CAMP` | Not in camp |
| `CORPS_RESPOND_CODE.NOT_IN_CORPS` | Not in corps |
| `CORPS_RESPOND_CODE.ALREADY_IN_CORPS` | Already in corps |
| `CORPS_RESPOND_CODE.CORPS_FULL` | Corps full |
| `CORPS_RESPOND_CODE.NOT_LEADER` | Not leader |
| `CORPS_RESPOND_CODE.LEVEL_TOO_LOW` | Level too low |
| `CORPS_RESPOND_CODE.CD_NOT_READY` | Cooldown not ready |
| `CORPS_RESPOND_CODE.NOT_ENOUGH_MONEY` | Not enough money |
| `CORPS_RESPOND_CODE.NOT_ENOUGH_PRESTIGE` | Not enough prestige |

---

## REVIVE_TYPE {#REVIVE_TYPE}

Revive type constants.

| Constant | Description |
|----------|-------------|
| `REVIVE_TYPE.INVALID` | Invalid |
| `REVIVE_TYPE.NORMAL` | Normal revive |
| `REVIVE_TYPE.IN_SITU` | In situ revive |
| `REVIVE_TYPE.BY_PLAYER` | By player revive |
| `REVIVE_TYPE.BY_BUFF` | By buff revive |
| `REVIVE_TYPE.BY_ITEM` | By item revive |

---

## TARGET_TYPE {#TARGET_TYPE}

Target type constants.

| Constant | Description |
|----------|-------------|
| `TARGET_TYPE.INVALID` | Invalid |
| `TARGET_TYPE.NPC` | NPC |
| `TARGET_TYPE.PLAYER` | Player |
| `TARGET_TYPE.DOODAD` | Doodad |
| `TARGET_TYPE.ITEM` | Item |
| `TARGET_TYPE.COORDS` | Coords |
| `TARGET_TYPE.SELF` | Self |
| `TARGET_TYPE.NPC_CORPSE` | NPC corpse |
| `TARGET_TYPE.PLAYER_CORPSE` | Player corpse |

---

## CHARACTER_KIND {#CHARACTER_KIND}

Character kind constants.

| Constant | Description |
|----------|-------------|
| `CHARACTER_KIND.INVALID` | Invalid |
| `CHARACTER_KIND.NPC` | NPC |
| `CHARACTER_KIND.PLAYER` | Player |

---

## NPC_SPECIES_TYPE {#NPC_SPECIES_TYPE}

NPC species type constants.

| Constant | Description |
|----------|-------------|
| `NPC_SPECIES_TYPE.INVALID` | Invalid |
| `NPC_SPECIES_TYPE.HUMAN` | Human |
| `NPC_SPECIES_TYPE.ANIMAL` | Animal |
| `NPC_SPECIES_TYPE.MECHANISM` | Mechanism |
| `NPC_SPECIES_TYPE.UNDEAD` | Undead |
| `NPC_SPECIES_TYPE.EVIL` | Evil |
| `NPC_SPECIES_TYPE.SPIRIT` | Spirit |
| `NPC_SPECIES_TYPE.PLANT` | Plant |

---

## ROLE_TYPE {#ROLE_TYPE}

Role type constants.

| Constant | Description |
|----------|-------------|
| `ROLE_TYPE.INVALID` | Invalid |
| `ROLE_TYPE.DAMAGE_DEALER` | Damage dealer |
| `ROLE_TYPE.TANK` | Tank |
| `ROLE_TYPE.HEALER` | Healer |

---

## DOODAD_KIND {#DOODAD_KIND}

Doodad kind constants.

| Constant | Description |
|----------|-------------|
| `DOODAD_KIND.INVALID` | Invalid |
| `DOODAD_KIND.NORMAL` | Normal |
| `DOODAD_KIND.CORPSE` | Corpse |
| `DOODAD_KIND.CRAFT_TARGET` | Craft target |
| `DOODAD_KIND.QUEST` | Quest |
| `DOODAD_KIND.TRAP` | Trap |
| `DOODAD_KIND.READ` | Read |
| `DOODAD_KIND.GUIDE` | Guide |
| `DOODAD_KIND.DOOR` | Door |
| `DOODAD_KIND.SWITCH` | Switch |
| `DOODAD_KIND.CLIENT_ONLY` | Client only |

---

## MOVE_STATE {#MOVE_STATE}

Move state constants.

| Constant | Description |
|----------|-------------|
| `MOVE_STATE.INVALID` | Invalid |
| `MOVE_STATE.ON_STAND` | On stand |
| `MOVE_STATE.ON_WALK` | On walk |
| `MOVE_STATE.ON_RUN` | On run |
| `MOVE_STATE.ON_JUMP` | On jump |
| `MOVE_STATE.ON_SWIM` | On swim |
| `MOVE_STATE.ON_SWIM_JUMP` | On swim jump |
| `MOVE_STATE.ON_FLOAT` | On float |
| `MOVE_STATE.ON_SIT` | On sit |
| `MOVE_STATE.ON_KNOCKED_DOWN` | On knocked down |
| `MOVE_STATE.ON_KNOCKED_BACK` | On knocked back |
| `MOVE_STATE.ON_KNOCKED_OFF` | On knocked off |
| `MOVE_STATE.ON_HALT` | On halt |
| `MOVE_STATE.ON_FREEZE` | On freeze |
| `MOVE_STATE.ON_ENTRAP` | On entrap |
| `MOVE_STATE.ON_DEATH` | On death |
| `MOVE_STATE.ON_DASH` | On dash |
| `MOVE_STATE.ON_PULL` | On pull |
| `MOVE_STATE.ON_REPULSED` | On repulsed |
| `MOVE_STATE.ON_AUTO_FLY` | On auto fly |
| `MOVE_STATE.ON_SKATE` | On skate |
| `MOVE_STATE.ON_RUSH` | On rush |

---

## AI_ACTION_TYPE {#AI_ACTION_TYPE}

AI action type constants.

| Constant | Description |
|----------|-------------|
| `AI_ACTION_TYPE.INVALID` | Invalid |
| `AI_ACTION_TYPE.IDLE` | Idle |
| `AI_ACTION_TYPE.WANDER` | Wander |
| `AI_ACTION_TYPE.PATROL` | Patrol |
| `AI_ACTION_TYPE.PURSUE` | Pursue |
| `AI_ACTION_TYPE.ESCAPE` | Escape |
| `AI_ACTION_TYPE.RETURN` | Return |
| `AI_ACTION_TYPE.FOLLOW` | Follow |

---

## AI_THREAT_TYPE {#AI_THREAT_TYPE}

AI threat type constants.

| Constant | Description |
|----------|-------------|
| `AI_THREAT_TYPE.INVALID` | Invalid |
| `AI_THREAT_TYPE.DAMAGE` | Damage |
| `AI_THREAT_TYPE.HEAL` | Heal |
| `AI_THREAT_TYPE.BASE` | Base |

---

## See Also

- [Constants Part 5 - Auction](./Constants5.md)
- [Constants Part 7 - Homeland](./Constants7.md)
