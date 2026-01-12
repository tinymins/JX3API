# Constants Part 2 - Skills and Combat

Game constants for skills, combat, and character attributes.

---

## ATTRIBUTE_TYPE {#ATTRIBUTE_TYPE}

Character attribute type constants. Used for buff effects and attribute modifications.

### Movement Attributes

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.RUN_SPEED_BASE` | Base run speed |
| `ATTRIBUTE_TYPE.MOVE_SPEED_PERCENT` | Movement speed percent |
| `ATTRIBUTE_TYPE.MIN_RUN_SPEED` | Minimum run speed |
| `ATTRIBUTE_TYPE.MAX_RUN_SPEED` | Maximum run speed |
| `ATTRIBUTE_TYPE.MAX_JUMP_COUNT` | Maximum jump count |
| `ATTRIBUTE_TYPE.SET_JUMP_COUNT` | Set jump count |
| `ATTRIBUTE_TYPE.FLY_FLAG` | Flying flag |
| `ATTRIBUTE_TYPE.ON_TOWER_FLAG` | On tower flag |
| `ATTRIBUTE_TYPE.ON_PARACHUTE_FLAG` | On parachute flag |
| `ATTRIBUTE_TYPE.HORSE_ATTRIBUTE` | Horse attribute |
| `ATTRIBUTE_TYPE.HORSE_RUN_TYPE` | Horse run type |
| `ATTRIBUTE_TYPE.HEIGHT` | Height |
| `ATTRIBUTE_TYPE.TRANSFORM` | Transform |
| `ATTRIBUTE_TYPE.GRAVITY_BASE` | Base gravity |
| `ATTRIBUTE_TYPE.GRAVITY_PERCENT` | Gravity percent |
| `ATTRIBUTE_TYPE.JUMP_SPEED_BASE` | Base jump speed |
| `ATTRIBUTE_TYPE.JUMP_SPEED_PERCENT` | Jump speed percent |
| `ATTRIBUTE_TYPE.HORSE_JUMP_SPEED_ADDITIONAL` | Horse jump speed additional |
| `ATTRIBUTE_TYPE.DROP_DEFENCE` | Drop defence |
| `ATTRIBUTE_TYPE.DIVING_FRAME_BASE` | Base diving frame |
| `ATTRIBUTE_TYPE.DIVING_FRAME_PERCENT` | Diving frame percent |
| `ATTRIBUTE_TYPE.MODIFY_DIVING_COUNT` | Modify diving count |
| `ATTRIBUTE_TYPE.WATER_FLY_ABILITY` | Water fly ability |
| `ATTRIBUTE_TYPE.CAN_NOT_JUMP` | Cannot jump |

### Primary Attributes

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.STRENGTH_BASE` | Base strength |
| `ATTRIBUTE_TYPE.STRENGTH_BASE_PERCENT_ADD` | Strength base percent add |
| `ATTRIBUTE_TYPE.AGILITY_BASE` | Base agility |
| `ATTRIBUTE_TYPE.AGILITY_BASE_PERCENT_ADD` | Agility base percent add |
| `ATTRIBUTE_TYPE.VITALITY_BASE` | Base vitality |
| `ATTRIBUTE_TYPE.VITALITY_BASE_PERCENT_ADD` | Vitality base percent add |
| `ATTRIBUTE_TYPE.SPIRIT_BASE` | Base spirit |
| `ATTRIBUTE_TYPE.SPIRIT_BASE_PERCENT_ADD` | Spirit base percent add |
| `ATTRIBUTE_TYPE.SPUNK_BASE` | Base spunk |
| `ATTRIBUTE_TYPE.SPUNK_BASE_PERCENT_ADD` | Spunk base percent add |
| `ATTRIBUTE_TYPE.HASTE_BASE` | Base haste |
| `ATTRIBUTE_TYPE.HASTE_BASE_PERCENT_ADD` | Haste base percent add |
| `ATTRIBUTE_TYPE.UNLIMIT_HASTE_BASE_PERCENT_ADD` | Unlimited haste base percent add |
| `ATTRIBUTE_TYPE.TRANSMIT_TRAIN` | Transmit train |
| `ATTRIBUTE_TYPE.MAX_TRAIN_VALUE` | Maximum train value |

### Life Attributes

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.CURRENT_LIFE` | Current life |
| `ATTRIBUTE_TYPE.MAX_LIFE_BASE` | Base maximum life |
| `ATTRIBUTE_TYPE.MAX_LIFE_PERCENT_ADD` | Maximum life percent add |
| `ATTRIBUTE_TYPE.MAX_LIFE_ADDITIONAL` | Additional maximum life |
| `ATTRIBUTE_TYPE.FINAL_MAX_LIFE_ADD_PERCENT` | Final maximum life add percent |
| `ATTRIBUTE_TYPE.LIFE_REPLENISH` | Life replenish |
| `ATTRIBUTE_TYPE.LIFE_REPLENISH_PERCENT` | Life replenish percent |
| `ATTRIBUTE_TYPE.LIFE_REPLENISH_COEFFICIENT` | Life replenish coefficient |
| `ATTRIBUTE_TYPE.LIFE_REPLENISH_EXT` | Life replenish extended |

### Mana Attributes

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.CURRENT_MANA` | Current mana |
| `ATTRIBUTE_TYPE.MAX_MANA_BASE` | Base maximum mana |
| `ATTRIBUTE_TYPE.MAX_MANA_PERCENT_ADD` | Maximum mana percent add |
| `ATTRIBUTE_TYPE.MAX_MANA_ADDITIONAL` | Additional maximum mana |
| `ATTRIBUTE_TYPE.MANA_PERCENT_ADD` | Mana percent add |
| `ATTRIBUTE_TYPE.MANA_REPLENISH` | Mana replenish |
| `ATTRIBUTE_TYPE.MANA_REPLENISH_PERCENT` | Mana replenish percent |
| `ATTRIBUTE_TYPE.MANA_REPLENISH_COEFFICIENT` | Mana replenish coefficient |
| `ATTRIBUTE_TYPE.MANA_REPLENISH_EXT` | Mana replenish extended |

### Rage/Energy Attributes

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.CURRENT_RAGE` | Current rage |
| `ATTRIBUTE_TYPE.MAX_RAGE` | Maximum rage |
| `ATTRIBUTE_TYPE.RAGE_REPLENISH` | Rage replenish |
| `ATTRIBUTE_TYPE.CURRENT_ENERGY` | Current energy |
| `ATTRIBUTE_TYPE.MAX_ENERGY` | Maximum energy |
| `ATTRIBUTE_TYPE.ENERGY_REPLENISH` | Energy replenish |

### Sun/Moon Energy (Ming Jiao)

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.SUN_POWER_VALUE` | Sun power value |
| `ATTRIBUTE_TYPE.MOON_POWER_VALUE` | Moon power value |
| `ATTRIBUTE_TYPE.CURRENT_SUN_ENERGY` | Current sun energy |
| `ATTRIBUTE_TYPE.MAX_SUN_ENERGY` | Maximum sun energy |
| `ATTRIBUTE_TYPE.SUN_ENERGY_ADD_PERCENT` | Sun energy add percent |
| `ATTRIBUTE_TYPE.SUN_ENERGY_REPLENISH` | Sun energy replenish |
| `ATTRIBUTE_TYPE.SUN_ENERGY_FALL_OFF` | Sun energy fall off |
| `ATTRIBUTE_TYPE.STOP_MAKE_SUN_POWER` | Stop make sun power |
| `ATTRIBUTE_TYPE.CURRENT_MOON_ENERGY` | Current moon energy |
| `ATTRIBUTE_TYPE.MAX_MOON_ENERGY` | Maximum moon energy |
| `ATTRIBUTE_TYPE.MOON_ENERGY_ADD_PERCENT` | Moon energy add percent |
| `ATTRIBUTE_TYPE.MOON_ENERGY_REPLENISH` | Moon energy replenish |
| `ATTRIBUTE_TYPE.MOON_ENERGY_FALL_OFF` | Moon energy fall off |

### Stamina/Thew

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.CURRENT_STAMINA` | Current stamina |
| `ATTRIBUTE_TYPE.MAX_STAMINA` | Maximum stamina |
| `ATTRIBUTE_TYPE.CURRENT_THEW` | Current thew |
| `ATTRIBUTE_TYPE.MAX_THEW` | Maximum thew |

### Threat

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.ACTIVE_THREAT_COEFFICIENT` | Active threat coefficient |
| `ATTRIBUTE_TYPE.PASSIVE_THREAT_COEFFICIENT` | Passive threat coefficient |

### Combat Stats

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.DODGE` | Dodge |
| `ATTRIBUTE_TYPE.DODGE_BASE_RATE` | Dodge base rate |
| `ATTRIBUTE_TYPE.PARRY_BASE_RATE` | Parry base rate |
| `ATTRIBUTE_TYPE.PARRY_BASE` | Base parry |
| `ATTRIBUTE_TYPE.PARRY_PERCENT` | Parry percent |
| `ATTRIBUTE_TYPE.PARRYVALUE_BASE` | Base parry value |
| `ATTRIBUTE_TYPE.PARRYVALUE_PERCENT` | Parry value percent |
| `ATTRIBUTE_TYPE.SENSE` | Sense |
| `ATTRIBUTE_TYPE.STRAIN_BASE` | Base strain |
| `ATTRIBUTE_TYPE.STRAIN_PERCENT` | Strain percent |
| `ATTRIBUTE_TYPE.TOUGHNESS_BASE_RATE` | Toughness base rate |
| `ATTRIBUTE_TYPE.TOUGHNESS_BASE` | Base toughness |
| `ATTRIBUTE_TYPE.TOUGHNESS_PERCENT` | Toughness percent |
| `ATTRIBUTE_TYPE.IMMORTAL` | Immortal |

### Physics Attack

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.SKILL_PHYSICS_DAMAGE` | Skill physics damage |
| `ATTRIBUTE_TYPE.SKILL_PHYSICS_DAMAGE_RAND` | Skill physics damage random |
| `ATTRIBUTE_TYPE.SKILL_PHYSICS_DAMAGE_PERCENT` | Skill physics damage percent |
| `ATTRIBUTE_TYPE.PHYSICS_DAMAGE_COEFFICIENT` | Physics damage coefficient |
| `ATTRIBUTE_TYPE.PHYSICS_ATTACK_POWER_BASE` | Base physics attack power |
| `ATTRIBUTE_TYPE.PHYSICS_ATTACK_POWER_PERCENT` | Physics attack power percent |
| `ATTRIBUTE_TYPE.PHYSICS_HIT_BASE_RATE` | Physics hit base rate |
| `ATTRIBUTE_TYPE.PHYSICS_HIT_VALUE` | Physics hit value |
| `ATTRIBUTE_TYPE.PHYSICS_CRITICAL_STRIKE_BASE_RATE` | Physics critical strike base rate |
| `ATTRIBUTE_TYPE.PHYSICS_CRITICAL_STRIKE` | Physics critical strike |
| `ATTRIBUTE_TYPE.PHYSICS_CRITICAL_DAMAGE_POWER_BASE` | Physics critical damage power base |
| `ATTRIBUTE_TYPE.PHYSICS_CRITICAL_DAMAGE_POWER_PERCENT` | Physics critical damage power percent |
| `ATTRIBUTE_TYPE.PHYSICS_OVERCOME_BASE` | Base physics overcome |
| `ATTRIBUTE_TYPE.PHYSICS_OVERCOME_PERCENT` | Physics overcome percent |
| `ATTRIBUTE_TYPE.PHYSICS_SHIELD_BASE` | Base physics shield |
| `ATTRIBUTE_TYPE.PHYSICS_SHIELD_PERCENT` | Physics shield percent |
| `ATTRIBUTE_TYPE.PHYSICS_SHIELD_ADDITIONAL` | Additional physics shield |

### Magic Attack (All Types)

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.SKILL_MAGIC_DAMAGE` | Skill magic damage |
| `ATTRIBUTE_TYPE.MAGIC_ATTACK_POWER_BASE` | Base magic attack power |
| `ATTRIBUTE_TYPE.MAGIC_ATTACK_POWER_PERCENT` | Magic attack power percent |
| `ATTRIBUTE_TYPE.MAGIC_CRITICAL_STRIKE` | Magic critical strike |
| `ATTRIBUTE_TYPE.MAGIC_SHIELD` | Magic shield |
| `ATTRIBUTE_TYPE.MAGIC_CRITICAL_DAMAGE_POWER_BASE` | Magic critical damage power base |
| `ATTRIBUTE_TYPE.MAGIC_CRITICAL_DAMAGE_POWER_PERCENT` | Magic critical damage power percent |
| `ATTRIBUTE_TYPE.MAGIC_OVERCOME` | Magic overcome |
| `ATTRIBUTE_TYPE.MAGIC_HIT_BASE_RATE` | Magic hit base rate |
| `ATTRIBUTE_TYPE.MAGIC_HIT_VALUE` | Magic hit value |

### Solar Magic (Yang)

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.SKILL_SOLAR_DAMAGE` | Skill solar damage |
| `ATTRIBUTE_TYPE.SOLAR_ATTACK_POWER_BASE` | Base solar attack power |
| `ATTRIBUTE_TYPE.SOLAR_ATTACK_POWER_PERCENT` | Solar attack power percent |
| `ATTRIBUTE_TYPE.SOLAR_CRITICAL_STRIKE` | Solar critical strike |
| `ATTRIBUTE_TYPE.SOLAR_OVERCOME_BASE` | Base solar overcome |
| `ATTRIBUTE_TYPE.SOLAR_OVERCOME_PERCENT` | Solar overcome percent |
| `ATTRIBUTE_TYPE.SOLAR_MAGIC_SHIELD_BASE` | Base solar magic shield |
| `ATTRIBUTE_TYPE.SOLAR_MAGIC_SHIELD_PERCENT` | Solar magic shield percent |

### Neutral Magic

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.SKILL_NEUTRAL_DAMAGE` | Skill neutral damage |
| `ATTRIBUTE_TYPE.NEUTRAL_ATTACK_POWER_BASE` | Base neutral attack power |
| `ATTRIBUTE_TYPE.NEUTRAL_ATTACK_POWER_PERCNET` | Neutral attack power percent |
| `ATTRIBUTE_TYPE.NEUTRAL_CRITICAL_STRIKE` | Neutral critical strike |
| `ATTRIBUTE_TYPE.NEUTRAL_OVERCOME_BASE` | Base neutral overcome |
| `ATTRIBUTE_TYPE.NEUTRAL_OVERCOME_PERCENT` | Neutral overcome percent |
| `ATTRIBUTE_TYPE.NEUTRAL_MAGIC_SHIELD_BASE` | Base neutral magic shield |
| `ATTRIBUTE_TYPE.NEUTRAL_MAGIC_SHIELD_PERCENT` | Neutral magic shield percent |

### Lunar Magic (Yin)

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.SKILL_LUNAR_DAMAGE` | Skill lunar damage |
| `ATTRIBUTE_TYPE.LUNAR_ATTACK_POWER_BASE` | Base lunar attack power |
| `ATTRIBUTE_TYPE.LUNAR_ATTACK_POWER_PERCENT` | Lunar attack power percent |
| `ATTRIBUTE_TYPE.LUNAR_CRITICAL_STRIKE` | Lunar critical strike |
| `ATTRIBUTE_TYPE.LUNAR_OVERCOME_BASE` | Base lunar overcome |
| `ATTRIBUTE_TYPE.LUNAR_OVERCOME_PERCENT` | Lunar overcome percent |
| `ATTRIBUTE_TYPE.LUNAR_MAGIC_SHIELD_BASE` | Base lunar magic shield |
| `ATTRIBUTE_TYPE.LUNAR_MAGIC_SHIELD_PERCENT` | Lunar magic shield percent |

### Poison

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.SKILL_POISON_DAMAGE` | Skill poison damage |
| `ATTRIBUTE_TYPE.POISON_ATTACK_POWER_BASE` | Base poison attack power |
| `ATTRIBUTE_TYPE.POISON_ATTACK_POWER_PERCENT` | Poison attack power percent |
| `ATTRIBUTE_TYPE.POISON_CRITICAL_STRIKE` | Poison critical strike |
| `ATTRIBUTE_TYPE.POISON_OVERCOME_BASE` | Base poison overcome |
| `ATTRIBUTE_TYPE.POISON_OVERCOME_PERCENT` | Poison overcome percent |
| `ATTRIBUTE_TYPE.POISON_MAGIC_SHIELD_BASE` | Base poison magic shield |
| `ATTRIBUTE_TYPE.POISON_MAGIC_SHIELD_PERCENT` | Poison magic shield percent |

### Therapy

| Constant | Description |
|----------|-------------|
| `ATTRIBUTE_TYPE.THERAPY_POWER_BASE` | Base therapy power |
| `ATTRIBUTE_TYPE.THERAPY_POWER_PERCENT` | Therapy power percent |
| `ATTRIBUTE_TYPE.SKILL_THERAPY` | Skill therapy |
| `ATTRIBUTE_TYPE.SKILL_THERAPY_RAND` | Skill therapy random |
| `ATTRIBUTE_TYPE.SKILL_THERAPY_PERCENT` | Skill therapy percent |
| `ATTRIBUTE_TYPE.THERAPY_COEFFICIENT` | Therapy coefficient |
| `ATTRIBUTE_TYPE.BE_THERAPY_COEFFICIENT` | Be therapy coefficient |

---

## SKILL_RESULT_CODE {#SKILL_RESULT_CODE}

Skill cast result codes.

| Constant | Description |
|----------|-------------|
| `SKILL_RESULT_CODE.SUCCESS` | Success |
| `SKILL_RESULT_CODE.FAILED` | Failed |
| `SKILL_RESULT_CODE.INVALID_CAST_MODE` | Invalid cast mode |
| `SKILL_RESULT_CODE.NOT_ENOUGH_LIFE` | Not enough life |
| `SKILL_RESULT_CODE.NOT_ENOUGH_MANA` | Not enough mana |
| `SKILL_RESULT_CODE.NOT_ENOUGH_RAGE` | Not enough rage |
| `SKILL_RESULT_CODE.NOT_ENOUGH_ENERGY` | Not enough energy |
| `SKILL_RESULT_CODE.NOT_ENOUGH_TRAIN` | Not enough train |
| `SKILL_RESULT_CODE.NOT_ENOUGH_STAMINA` | Not enough stamina |
| `SKILL_RESULT_CODE.NOT_ENOUGH_ITEM` | Not enough item |
| `SKILL_RESULT_CODE.NOT_ENOUGH_AMMO` | Not enough ammo |
| `SKILL_RESULT_CODE.SKILL_NOT_READY` | Skill not ready (cooldown) |
| `SKILL_RESULT_CODE.INVALID_SKILL` | Invalid skill |
| `SKILL_RESULT_CODE.INVALID_TARGET` | Invalid target |
| `SKILL_RESULT_CODE.NO_TARGET` | No target |
| `SKILL_RESULT_CODE.NEED_TARGET` | Need target |
| `SKILL_RESULT_CODE.TOO_CLOSE_TARGET` | Target too close |
| `SKILL_RESULT_CODE.TOO_FAR_TARGET` | Target too far |
| `SKILL_RESULT_CODE.OUT_OF_ANGLE` | Out of angle |
| `SKILL_RESULT_CODE.TARGET_INVISIBLE` | Target invisible |
| `SKILL_RESULT_CODE.WEAPON_ERROR` | Weapon error |
| `SKILL_RESULT_CODE.WEAPON_DESTROY` | Weapon destroyed |
| `SKILL_RESULT_CODE.AMMO_ERROR` | Ammo error |
| `SKILL_RESULT_CODE.NOT_EQUIT_AMMO` | Ammo not equipped |
| `SKILL_RESULT_CODE.MOUNT_ERROR` | Mount error |
| `SKILL_RESULT_CODE.IN_OTACTION` | In OT action |
| `SKILL_RESULT_CODE.ON_SILENCE` | Silenced |
| `SKILL_RESULT_CODE.NOT_FORMATION_LEADER` | Not formation leader |
| `SKILL_RESULT_CODE.NOT_ENOUGH_MEMBER` | Not enough members |
| `SKILL_RESULT_CODE.NOT_START_ACCUMULATE` | Not started accumulate |
| `SKILL_RESULT_CODE.NOT_SUN_MOON_POWER` | Not enough sun/moon power |
| `SKILL_RESULT_CODE.SKILL_ERROR` | Skill error |
| `SKILL_RESULT_CODE.BUFF_ERROR` | Buff error |
| `SKILL_RESULT_CODE.NOT_IN_FIGHT` | Not in fight |
| `SKILL_RESULT_CODE.MOVE_STATE_ERROR` | Move state error |
| `SKILL_RESULT_CODE.ERROR_BY_HORSE` | Error by horse |
| `SKILL_RESULT_CODE.BUFF_INVALID` | Buff invalid |
| `SKILL_RESULT_CODE.FORCE_EFFECT` | Force effect |
| `SKILL_RESULT_CODE.BUFF_IMMUNITY` | Buff immunity |
| `SKILL_RESULT_CODE.TARGET_LIFE_ERROR` | Target life error |
| `SKILL_RESULT_CODE.SELF_LIFE_ERROR` | Self life error |
| `SKILL_RESULT_CODE.DST_MOVE_STATE_ERROR` | Destination move state error |
| `SKILL_RESULT_CODE.NOT_PARTY` | Not in party |
| `SKILL_RESULT_CODE.MAP_BAN` | Map ban |
| `SKILL_RESULT_CODE.TARGET_STEALTH` | Target in stealth |
| `SKILL_RESULT_CODE.ERROR_BY_SPRINT` | Error by sprint |
| `SKILL_RESULT_CODE.DYNAMIC_GROUP_MISMATCH` | Dynamic group mismatch |
| `SKILL_RESULT_CODE.POSE_INVALID` | Pose invalid |
| `SKILL_RESULT_CODE.IMMUNITY_CAST_ID_MISMATCH` | Immunity cast ID mismatch |
| `SKILL_RESULT_CODE.IDENTITY_ATTACK_ID_MISMATCH` | Identity attack ID mismatch |
| `SKILL_RESULT_CODE.NOT_ENOUGH_SUN_ENERGY` | Not enough sun energy |
| `SKILL_RESULT_CODE.NOT_ENOUGH_MOON_ENERGY` | Not enough moon energy |
| `SKILL_RESULT_CODE.ALTITUDE_TOO_HIGH` | Altitude too high |
| `SKILL_RESULT_CODE.ALTITUDE_TOO_LOW` | Altitude too low |
| `SKILL_RESULT_CODE.NOT_ENOUGH_SPRINT_POWER` | Not enough sprint power |
| `SKILL_RESULT_CODE.ERROR_BY_HOLD_HORSE` | Error by hold horse |

---

## SKILL_CAST_MODE {#SKILL_CAST_MODE}

Skill cast mode/area types.

| Constant | Description |
|----------|-------------|
| `SKILL_CAST_MODE.SECTOR` | Sector area |
| `SKILL_CAST_MODE.SECTOR_OF_DEPTH` | Sector with depth |
| `SKILL_CAST_MODE.TARGET_ANGLE_SECTOR` | Target angle sector |
| `SKILL_CAST_MODE.RECTANGLE` | Rectangle area |
| `SKILL_CAST_MODE.RECTANGLE_OF_DEPTH` | Rectangle with depth |
| `SKILL_CAST_MODE.TARGET_ANGLE_RECTANGLE` | Target angle rectangle |
| `SKILL_CAST_MODE.CASTER_AREA` | Caster area |
| `SKILL_CAST_MODE.CASTER_AREA_OF_DEPTH` | Caster area with depth |
| `SKILL_CAST_MODE.TARGET_AREA` | Target area |
| `SKILL_CAST_MODE.POINT_AREA` | Point area |
| `SKILL_CAST_MODE.POINT_AREA_OF_CASTER_TEAM` | Point area of caster team |
| `SKILL_CAST_MODE.POINT_RECTANGLE` | Point rectangle |
| `SKILL_CAST_MODE.CASTER_SINGLE` | Caster single |
| `SKILL_CAST_MODE.TARGET_SINGLE` | Target single |
| `SKILL_CAST_MODE.TARGET_CHAIN` | Target chain |
| `SKILL_CAST_MODE.POINT` | Point |
| `SKILL_CAST_MODE.ITEM` | Item |
| `SKILL_CAST_MODE.TARGET_LEADER` | Target leader |
| `SKILL_CAST_MODE.PARTY_AREA` | Party area |
| `SKILL_CAST_MODE.TARGET_TEAM_AREA` | Target team area |
| `SKILL_CAST_MODE.TARGET_HOODLE` | Target hoodle |
| `SKILL_CAST_MODE.CASTER_SPREAD_CIRCLE` | Caster spread circle |
| `SKILL_CAST_MODE.TARGET_RAY` | Target ray |
| `SKILL_CAST_MODE.CASTER_CONVEX_HULL_AREA` | Caster convex hull area |
| `SKILL_CAST_MODE.POINT_AREA_FIND_FIRST` | Point area find first |

---

## SKILL_KIND_TYPE {#SKILL_KIND_TYPE}

Skill kind/damage type.

| Constant | Description |
|----------|-------------|
| `SKILL_KIND_TYPE.PHYSICS` | Physics damage |
| `SKILL_KIND_TYPE.SOLAR_MAGIC` | Solar magic damage (Yang) |
| `SKILL_KIND_TYPE.NEUTRAL_MAGIC` | Neutral magic damage |
| `SKILL_KIND_TYPE.LUNAR_MAGIC` | Lunar magic damage (Yin) |
| `SKILL_KIND_TYPE.POISON` | Poison damage |
| `SKILL_KIND_TYPE.LEAP` | Leap |
| `SKILL_KIND_TYPE.NONE` | None |

---

## SKILL_FUNCTION_TYPE {#SKILL_FUNCTION_TYPE}

Skill function type for buff effects.

| Constant | Description |
|----------|-------------|
| `SKILL_FUNCTION_TYPE.NORMAL` | Normal |
| `SKILL_FUNCTION_TYPE.SLOW` | Slow |
| `SKILL_FUNCTION_TYPE.FEAR` | Fear |
| `SKILL_FUNCTION_TYPE.HALT` | Halt |
| `SKILL_FUNCTION_TYPE.SILENCE` | Silence |
| `SKILL_FUNCTION_TYPE.CHAOS` | Chaos |
| `SKILL_FUNCTION_TYPE.CHARM` | Charm |
| `SKILL_FUNCTION_TYPE.STUN` | Stun |
| `SKILL_FUNCTION_TYPE.ENMITY` | Enmity |
| `SKILL_FUNCTION_TYPE.BLOODING` | Bleeding |
| `SKILL_FUNCTION_TYPE.DAZE` | Daze |
| `SKILL_FUNCTION_TYPE.DAMAGE` | Damage |
| `SKILL_FUNCTION_TYPE.Fly` | Fly |
| `SKILL_FUNCTION_TYPE.Disarm` | Disarm |

---

## SKILL_RESULT_TYPE {#SKILL_RESULT_TYPE}

Skill result type for damage/healing.

| Constant | Description |
|----------|-------------|
| `SKILL_RESULT_TYPE.PHYSICS_DAMAGE` | Physics damage |
| `SKILL_RESULT_TYPE.SOLAR_MAGIC_DAMAGE` | Solar magic damage |
| `SKILL_RESULT_TYPE.NEUTRAL_MAGIC_DAMAGE` | Neutral magic damage |
| `SKILL_RESULT_TYPE.LUNAR_MAGIC_DAMAGE` | Lunar magic damage |
| `SKILL_RESULT_TYPE.POISON_DAMAGE` | Poison damage |
| `SKILL_RESULT_TYPE.REFLECTIED_DAMAGE` | Reflected damage |
| `SKILL_RESULT_TYPE.THERAPY` | Therapy/Healing |
| `SKILL_RESULT_TYPE.STEAL_LIFE` | Steal life |
| `SKILL_RESULT_TYPE.ABSORB_THERAPY` | Absorb therapy |
| `SKILL_RESULT_TYPE.ABSORB_DAMAGE` | Absorb damage |
| `SKILL_RESULT_TYPE.SHIELD_DAMAGE` | Shield damage |
| `SKILL_RESULT_TYPE.PARRY_DAMAGE` | Parry damage |
| `SKILL_RESULT_TYPE.INSIGHT_DAMAGE` | Insight damage |
| `SKILL_RESULT_TYPE.EFFECTIVE_DAMAGE` | Effective damage |
| `SKILL_RESULT_TYPE.EFFECTIVE_THERAPY` | Effective therapy |
| `SKILL_RESULT_TYPE.TRANSFER_LIFE` | Transfer life |
| `SKILL_RESULT_TYPE.TRANSFER_MANA` | Transfer mana |

---

## SKILL_EFFECT_TYPE {#SKILL_EFFECT_TYPE}

Skill effect type.

| Constant | Description |
|----------|-------------|
| `SKILL_EFFECT_TYPE.INVALID` | Invalid |
| `SKILL_EFFECT_TYPE.SKILL` | Skill effect |
| `SKILL_EFFECT_TYPE.BUFF` | Buff effect |
| `SKILL_EFFECT_TYPE.TOTAL` | Total |

---

## SKILL_CAST_EFFECT_TYPE {#SKILL_CAST_EFFECT_TYPE}

Skill cast effect type.

| Constant | Description |
|----------|-------------|
| `SKILL_CAST_EFFECT_TYPE.INVALID` | Invalid |
| `SKILL_CAST_EFFECT_TYPE.HARMFUL` | Harmful |
| `SKILL_CAST_EFFECT_TYPE.NERTUAL` | Neutral |
| `SKILL_CAST_EFFECT_TYPE.BENEFICIAL` | Beneficial |

---

## SKILL_COMPARE_FLAG {#SKILL_COMPARE_FLAG}

Skill compare flag.

| Constant | Description |
|----------|-------------|
| `SKILL_COMPARE_FLAG.EQUAL` | Equal |
| `SKILL_COMPARE_FLAG.GREATER_EQUAL` | Greater than or equal |

---

## BUFF_COMPARE_FLAG {#BUFF_COMPARE_FLAG}

Buff compare flag.

| Constant | Description |
|----------|-------------|
| `BUFF_COMPARE_FLAG.EQUAL` | Equal |
| `BUFF_COMPARE_FLAG.GREATER_EQUAL` | Greater than or equal |
| `BUFF_COMPARE_FLAG.LESS` | Less than |

---

## See Also

- [Constants Part 1](./Constants.md)
- [Constants Part 3 - Items](./Constants3.md)
