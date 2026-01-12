# Constants

Game constants and enumerations exported for Addon API.

---

## PLAYER_TALK_CHANNEL {#PLAYER_TALK_CHANNEL}

Chat channel type constants.

| Constant | Description |
|----------|-------------|
| `PLAYER_TALK_CHANNEL.INVALID` | Invalid channel |
| `PLAYER_TALK_CHANNEL.NEARBY` | Nearby/Local chat |
| `PLAYER_TALK_CHANNEL.TEAM` | Team chat |
| `PLAYER_TALK_CHANNEL.RAID` | Raid chat |
| `PLAYER_TALK_CHANNEL.BATTLE_FIELD` | Battlefield chat |
| `PLAYER_TALK_CHANNEL.SENCE` | Scene/Map chat |
| `PLAYER_TALK_CHANNEL.WHISPER` | Whisper/Private message |
| `PLAYER_TALK_CHANNEL.FACE` | Face-to-face chat |
| `PLAYER_TALK_CHANNEL.GM_MESSAGE` | GM message |
| `PLAYER_TALK_CHANNEL.LOCAL_SYS` | Local system message |
| `PLAYER_TALK_CHANNEL.GLOBAL_SYS` | Global system message |
| `PLAYER_TALK_CHANNEL.GM_ANNOUNCE` | GM announcement |
| `PLAYER_TALK_CHANNEL.TO_TONG_GM_ANNOUNCE` | GM announcement to guild |
| `PLAYER_TALK_CHANNEL.TO_PLAYER_GM_ANNOUNCE` | GM announcement to player |
| `PLAYER_TALK_CHANNEL.NPC_NEARBY` | NPC nearby chat |
| `PLAYER_TALK_CHANNEL.NPC_PARTY` | NPC party chat |
| `PLAYER_TALK_CHANNEL.NPC_SENCE` | NPC scene chat |
| `PLAYER_TALK_CHANNEL.NPC_WHISPER` | NPC whisper |
| `PLAYER_TALK_CHANNEL.NPC_SAY_TO` | NPC say to target |
| `PLAYER_TALK_CHANNEL.NPC_YELL_TO` | NPC yell to target |
| `PLAYER_TALK_CHANNEL.NPC_FACE` | NPC face chat |
| `PLAYER_TALK_CHANNEL.NPC_SAY_TO_ID` | NPC say to target by sentence ID |
| `PLAYER_TALK_CHANNEL.NPC_SAY_TO_CAMP` | NPC say to camp |
| `PLAYER_TALK_CHANNEL.TONG` | Guild chat |
| `PLAYER_TALK_CHANNEL.TONG_ALLIANCE` | Guild alliance chat |
| `PLAYER_TALK_CHANNEL.TONG_SYS` | Guild system message |
| `PLAYER_TALK_CHANNEL.WORLD` | World chat |
| `PLAYER_TALK_CHANNEL.FORCE` | Force/Faction chat |
| `PLAYER_TALK_CHANNEL.CAMP` | Camp chat |
| `PLAYER_TALK_CHANNEL.MENTOR` | Mentor chat |
| `PLAYER_TALK_CHANNEL.FRIENDS` | Friends chat |
| `PLAYER_TALK_CHANNEL.DEBUG_THREAT` | Debug threat |
| `PLAYER_TALK_CHANNEL.IDENTITY` | Identity chat |
| `PLAYER_TALK_CHANNEL.BULLET_SCREEN` | Bullet screen |
| `PLAYER_TALK_CHANNEL.JJC_BULLET_SCREEN` | Arena bullet screen |
| `PLAYER_TALK_CHANNEL.CAMP_FIGHT_BULLET_SCREEN` | Camp fight bullet screen |
| `PLAYER_TALK_CHANNEL.BATTLE_FIELD_SIDE` | Battlefield side chat |
| `PLAYER_TALK_CHANNEL.SYSTEM_NOTICE` | System notice |

---

## GLOBAL {#GLOBAL}

Global game constants.

| Constant | Description |
|----------|-------------|
| `GLOBAL.GAME_FPS` | Game frames per second |
| `GLOBAL.DIRECTION_COUNT` | Number of directions |
| `GLOBAL.CELL_LENGTH` | Cell length |
| `GLOBAL.LOGICAL_CELL_CM_LENGTH` | Logical cell length in cm |
| `GLOBAL.INVALID_PARTY_ID` | Invalid party ID |
| `GLOBAL.INVALID_SKILL_ID` | Invalid skill ID |
| `GLOBAL.MOVE_DEST_RANGE` | Movement destination range |
| `GLOBAL.CURRENT_ITEM_VERSION` | Current item version |
| `GLOBAL.MAX_BANK_PACKAGE_COUNT` | Maximum bank package count |
| `GLOBAL.START_QUEST_DELAY` | Quest start delay |
| `GLOBAL.AI_USER_EVENT` | AI user event |
| `GLOBAL.AI_USER_ACTION` | AI user action |
| `GLOBAL.COIN_PRICE_DISCOUNT_BASE` | Coin shop price discount base |
| `GLOBAL.HORSE_PACKAGE_SIZE` | Horse package size |
| `GLOBAL.MAX_RARE_HORSE_COUNT` | Maximum rare horse count |

---

## ITEM_GENRE {#ITEM_GENRE}

Item genre/category constants.

| Constant | Description |
|----------|-------------|
| `ITEM_GENRE.EQUIPMENT` | Equipment |
| `ITEM_GENRE.POTION` | Potion |
| `ITEM_GENRE.TASK_ITEM` | Task/Quest item |
| `ITEM_GENRE.MATERIAL` | Material |
| `ITEM_GENRE.BOOK` | Book |
| `ITEM_GENRE.DESIGNATION` | Designation item |
| `ITEM_GENRE.MOUNT_ITEM` | Mount item |
| `ITEM_GENRE.ENCHANT_ITEM` | Enchant item |
| `ITEM_GENRE.BOX` | Box |
| `ITEM_GENRE.BOX_KEY` | Box key |
| `ITEM_GENRE.DIAMOND` | Diamond (five-element stone) |
| `ITEM_GENRE.COLOR_DIAMOND` | Color diamond |
| `ITEM_GENRE.CUB` | Cub (tameable) |
| `ITEM_GENRE.FODDER` | Fodder |
| `ITEM_GENRE.FOOD` | Food |
| `ITEM_GENRE.EMOTION` | Emotion item |
| `ITEM_GENRE.EXTERIOR_COLLECTION_PIECE` | Exterior collection piece |
| `ITEM_GENRE.COIN_SHOP_QUANTITY_LIMIT_ITEM` | Coin shop quantity limited item |
| `ITEM_GENRE.ACTION` | Action item |
| `ITEM_GENRE.HOMELAND` | Homeland item |
| `ITEM_GENRE.TOTAL` | Total count |

---

## EQUIPMENT_SUB {#EQUIPMENT_SUB}

Equipment sub-type constants.

| Constant | Description |
|----------|-------------|
| `EQUIPMENT_SUB.MELEE_WEAPON` | Melee weapon |
| `EQUIPMENT_SUB.RANGE_WEAPON` | Range weapon |
| `EQUIPMENT_SUB.CHEST` | Chest armor |
| `EQUIPMENT_SUB.HELM` | Helm |
| `EQUIPMENT_SUB.AMULET` | Amulet/Necklace |
| `EQUIPMENT_SUB.RING` | Ring |
| `EQUIPMENT_SUB.WAIST` | Waist/Belt |
| `EQUIPMENT_SUB.PENDANT` | Pendant |
| `EQUIPMENT_SUB.PANTS` | Pants |
| `EQUIPMENT_SUB.BOOTS` | Boots |
| `EQUIPMENT_SUB.BANGLE` | Bangle/Bracers |
| `EQUIPMENT_SUB.WAIST_EXTEND` | Waist extend (e.g., wine gourd) |
| `EQUIPMENT_SUB.PACKAGE` | Package/Bag |
| `EQUIPMENT_SUB.ARROW` | Arrow/Throwing weapon |
| `EQUIPMENT_SUB.BACK_EXTEND` | Back extend |
| `EQUIPMENT_SUB.HORSE` | Horse/Mount |
| `EQUIPMENT_SUB.BULLET` | Bullet/Trap |
| `EQUIPMENT_SUB.FACE_EXTEND` | Face extend |
| `EQUIPMENT_SUB.MINI_AVATAR` | Mini avatar |
| `EQUIPMENT_SUB.PET` | Pet |
| `EQUIPMENT_SUB.L_SHOULDER_EXTEND` | Left shoulder extend |
| `EQUIPMENT_SUB.R_SHOULDER_EXTEND` | Right shoulder extend |
| `EQUIPMENT_SUB.BACK_CLOAK_EXTEND` | Cloak |
| `EQUIPMENT_SUB.HORSE_EQUIP` | Horse equipment |
| `EQUIPMENT_SUB.BAG_EXTEND` | Bag extend |
| `EQUIPMENT_SUB.PENDENT_PET` | Pendant pet |
| `EQUIPMENT_SUB.TOTAL` | Total count |

---

## WEAPON_DETAIL {#WEAPON_DETAIL}

Weapon detail type constants.

| Constant | Description |
|----------|-------------|
| `WEAPON_DETAIL.WAND` | Wand |
| `WEAPON_DETAIL.SPEAR` | Spear |
| `WEAPON_DETAIL.SWORD` | Sword |
| `WEAPON_DETAIL.FIST` | Fist weapon |
| `WEAPON_DETAIL.DOUBLE_WEAPON` | Double weapon |
| `WEAPON_DETAIL.PEN` | Pen |
| `WEAPON_DETAIL.SLING_SHOT` | Sling shot |
| `WEAPON_DETAIL.DART` | Dart |
| `WEAPON_DETAIL.MACH_DART` | Mach dart |
| `WEAPON_DETAIL.BIG_SWORD` | Big sword |
| `WEAPON_DETAIL.FLUTE` | Flute |
| `WEAPON_DETAIL.BOW` | Bow |
| `WEAPON_DETAIL.KNIFE` | Knife |
| `WEAPON_DETAIL.STICK` | Stick |
| `WEAPON_DETAIL.BLADE_SHIELD` | Blade shield |
| `WEAPON_DETAIL.HEPTA_CHORD` | Hepta chord (七弦琴) |
| `WEAPON_DETAIL.BROAD_SWORD` | Broad sword |
| `WEAPON_DETAIL.UMBRELLA` | Umbrella |
| `WEAPON_DETAIL.CHAIN_BLADE` | Chain blade |
| `WEAPON_DETAIL.TOTAL` | Total count |

---

## INVENTORY_INDEX {#INVENTORY_INDEX}

Inventory index constants.

| Constant | Description |
|----------|-------------|
| `INVENTORY_INDEX.MELEE_WEAPON` | Melee weapon slot |
| `INVENTORY_INDEX.BIG_SWORD` | Big sword slot |
| `INVENTORY_INDEX.RANGE_WEAPON` | Range weapon slot |
| `INVENTORY_INDEX.CHEST` | Chest slot |
| `INVENTORY_INDEX.HELM` | Helm slot |
| `INVENTORY_INDEX.AMULET` | Amulet slot |
| `INVENTORY_INDEX.LEFT_RING` | Left ring slot |
| `INVENTORY_INDEX.RIGHT_RING` | Right ring slot |
| `INVENTORY_INDEX.WAIST` | Waist slot |
| `INVENTORY_INDEX.PENDANT` | Pendant slot |
| `INVENTORY_INDEX.PANTS` | Pants slot |
| `INVENTORY_INDEX.BOOTS` | Boots slot |
| `INVENTORY_INDEX.BANGLE` | Bangle slot |
| `INVENTORY_INDEX.PACKAGE1` | Package 1 slot |
| `INVENTORY_INDEX.PACKAGE2` | Package 2 slot |
| `INVENTORY_INDEX.PACKAGE3` | Package 3 slot |
| `INVENTORY_INDEX.PACKAGE4` | Package 4 slot |
| `INVENTORY_INDEX.PACKAGE_MIBAO` | Mibao package slot |
| `INVENTORY_INDEX.BANK_PACKAGE1` | Bank package 1 slot |
| `INVENTORY_INDEX.BANK_PACKAGE2` | Bank package 2 slot |
| `INVENTORY_INDEX.BANK_PACKAGE3` | Bank package 3 slot |
| `INVENTORY_INDEX.BANK_PACKAGE4` | Bank package 4 slot |
| `INVENTORY_INDEX.BANK_PACKAGE5` | Bank package 5 slot |
| `INVENTORY_INDEX.ARROW` | Arrow slot |
| `INVENTORY_INDEX.HEAD_HORSE_EQUIP` | Head horse equipment slot |
| `INVENTORY_INDEX.CHEST_HORSE_EQUIP` | Chest horse equipment slot |
| `INVENTORY_INDEX.FOOT_HORSE_EQUIP` | Foot horse equipment slot |
| `INVENTORY_INDEX.HANG_ITEM_HORSE_EQUIP` | Hang item horse equipment slot |
| `INVENTORY_INDEX.TOTAL` | Total count |

---

## CAMP {#CAMP}

Camp/Faction constants.

| Constant | Description |
|----------|-------------|
| `CAMP.NEUTRAL` | Neutral |
| `CAMP.GOOD` | Good (浩气盟) |
| `CAMP.EVIL` | Evil (恶人谷) |

---

## TARGET {#TARGET}

Target type constants.

| Constant | Description |
|----------|-------------|
| `TARGET.NO_TARGET` | No target |
| `TARGET.NPC` | NPC target |
| `TARGET.PLAYER` | Player target |
| `TARGET.DOODAD` | Doodad target |
| `TARGET.ITEM` | Item target |
| `TARGET.COORDINATES` | Coordinates target |

---

## ROLE_TYPE {#ROLE_TYPE}

Role type constants.

| Constant | Description |
|----------|-------------|
| `ROLE_TYPE.INVALID` | Invalid |
| `ROLE_TYPE.STANDARD_NPC` | Standard NPC |
| `ROLE_TYPE.STANDARD_MALE` | Standard male player |
| `ROLE_TYPE.STANDARD_FEMALE` | Standard female player |
| `ROLE_TYPE.LITTLE_BOY` | Little boy |
| `ROLE_TYPE.LITTLE_GIRL` | Little girl |
| `ROLE_TYPE.MONSTER` | Monster |
| `ROLE_TYPE.TOTAL` | Total count |

---

## PK_STATE {#PK_STATE}

PK state constants.

| Constant | Description |
|----------|-------------|
| `PK_STATE.CLOSE` | PK closed |
| `PK_STATE.OPEN` | PK open |
| `PK_STATE.CAMP` | Camp PK |
| `PK_STATE.TONG` | Guild PK |

---

## MOVE_STATE {#MOVE_STATE}

Movement state constants.

| Constant | Description |
|----------|-------------|
| `MOVE_STATE.ON_STAND` | Standing |
| `MOVE_STATE.ON_WALK` | Walking |
| `MOVE_STATE.ON_RUN` | Running |
| `MOVE_STATE.ON_JUMP` | Jumping |
| `MOVE_STATE.ON_SWIM` | Swimming |
| `MOVE_STATE.ON_KNOCK_DOWN` | Knocked down |
| `MOVE_STATE.ON_KNOCK_BACK` | Knocked back |
| `MOVE_STATE.ON_KNOCK_OFF` | Knocked off |
| `MOVE_STATE.ON_HALT` | Halted |
| `MOVE_STATE.ON_FREEZE` | Frozen |
| `MOVE_STATE.ON_ENTRAP` | Entrapped |
| `MOVE_STATE.ON_SIT` | Sitting |
| `MOVE_STATE.ON_DEATH` | Dead |
| `MOVE_STATE.ON_DASH` | Dashing |
| `MOVE_STATE.ON_PULL` | Being pulled |
| `MOVE_STATE.ON_REPULSED` | Repulsed |
| `MOVE_STATE.ON_RISE` | Rising |
| `MOVE_STATE.ON_AUTO_FLY` | Auto flying |

---

## INVENTORY_TYPE {#INVENTORY_TYPE}

Inventory type constants.

| Constant | Description |
|----------|-------------|
| `INVENTORY_TYPE.EQUIPMENT` | Equipment inventory |
| `INVENTORY_TYPE.PACKAGE` | Package inventory |
| `INVENTORY_TYPE.BANK` | Bank inventory |
| `INVENTORY_TYPE.SLOT` | Slot inventory |
| `INVENTORY_TYPE.SOLD_LIST` | Sold list |
| `INVENTORY_TYPE.SYSTEM_PACKAGE` | System package |
| `INVENTORY_TYPE.BULLET_PACKAGE` | Bullet package |
| `INVENTORY_TYPE.TIME_LIMIT_SOLD_LIST` | Time-limited sold list |
| `INVENTORY_TYPE.CUB_PACKAGE` | Cub package |
| `INVENTORY_TYPE.HORSE_PACKAGE` | Horse package |
| `INVENTORY_TYPE.TOTAL` | Total count |

---

## ITEM_BIND {#ITEM_BIND}

Item bind type constants.

| Constant | Description |
|----------|-------------|
| `ITEM_BIND.INVALID` | Invalid |
| `ITEM_BIND.NEVER_BIND` | Never bind |
| `ITEM_BIND.BIND_ON_EQUIPPED` | Bind on equipped |
| `ITEM_BIND.BIND_ON_PICKED` | Bind on picked |
| `ITEM_BIND.BIND_ON_TIME_LIMITATION` | Bind on time limitation |

---

## ANNOUNCE_SHOW_TYPE {#ANNOUNCE_SHOW_TYPE}

Announcement show type constants.

| Constant | Description |
|----------|-------------|
| `ANNOUNCE_SHOW_TYPE.INVALID` | Invalid |
| `ANNOUNCE_SHOW_TYPE.CHAT_BOX` | Show in chat box |
| `ANNOUNCE_SHOW_TYPE.SCROLL_BOX` | Show in scroll box |
| `ANNOUNCE_SHOW_TYPE.BOSS_TIP` | Show as boss tip |
| `ANNOUNCE_SHOW_TYPE.COUNT_DOWN` | Show with countdown |
| `ANNOUNCE_SHOW_TYPE.SCROLL_BOX_GM` | GM scroll box |
| `ANNOUNCE_SHOW_TYPE.SCROLL_BOX_FIREWORKS` | Fireworks scroll box |
| `ANNOUNCE_SHOW_TYPE.CALENDAR_BOX` | Calendar box |

---

## MAP_TYPE {#MAP_TYPE}

Map type constants.

| Constant | Description |
|----------|-------------|
| `MAP_TYPE.INVALID` | Invalid |
| `MAP_TYPE.NORMAL` | Normal map |
| `MAP_TYPE.DUNGEON` | Dungeon |
| `MAP_TYPE.BATTLE_FIELD` | Battlefield |
| `MAP_TYPE.ARENA` | Arena |

---

## FORCE_TYPE {#FORCE_TYPE}

Force/School type constants.

| Constant | Description |
|----------|-------------|
| `FORCE_TYPE.INVALID` | Invalid |
| `FORCE_TYPE.SHAO_LIN` | Shaolin (少林) |
| `FORCE_TYPE.WAN_HUA` | Wanhua (万花) |
| `FORCE_TYPE.TIAN_CE` | Tiance (天策) |
| `FORCE_TYPE.CHUN_YANG` | Chunyang (纯阳) |
| `FORCE_TYPE.QI_XIU` | Qixiu (七秀) |
| `FORCE_TYPE.WU_DU` | Wudu (五毒) |
| `FORCE_TYPE.TANG_MEN` | Tangmen (唐门) |
| `FORCE_TYPE.CANG_JIAN` | Cangjian (藏剑) |
| `FORCE_TYPE.GAI_BANG` | Gaibang (丐帮) |
| `FORCE_TYPE.MING_JIAO` | Mingjiao (明教) |
| `FORCE_TYPE.CANG_YUN` | Cangyun (苍云) |
| `FORCE_TYPE.CHANG_GE` | Changge (长歌) |
| `FORCE_TYPE.BA_DAO` | Badao (霸刀) |
| `FORCE_TYPE.PENG_LAI` | Penglai (蓬莱) |
| `FORCE_TYPE.LING_XUE` | Lingxue (凌雪) |
| `FORCE_TYPE.YAN_TIAN` | Yantian (衍天) |
| `FORCE_TYPE.YAO_ZONG` | Yaozong (药宗) |
| `FORCE_TYPE.DAO_ZONG` | Daozong (刀宗) |
| `FORCE_TYPE.WAN_LING` | Wanling (万灵) |

---

## VIP_TYPE {#VIP_TYPE}

VIP type constants.

| Constant | Description |
|----------|-------------|
| `VIP_TYPE.NONE` | No VIP |
| `VIP_TYPE.VIP` | VIP |
| `VIP_TYPE.SUPER_VIP` | Super VIP |

---

## SERVER_TYPE {#SERVER_TYPE}

Server type constants.

| Constant | Description |
|----------|-------------|
| `SERVER_TYPE.NORMAL` | Normal server |
| `SERVER_TYPE.PVP` | PVP server |

---

## PARTY_LOOT_MODE {#PARTY_LOOT_MODE}

Party loot mode constants.

| Constant | Description |
|----------|-------------|
| `PARTY_LOOT_MODE.FREE_FOR_ALL` | Free for all |
| `PARTY_LOOT_MODE.DISTRIBUTE` | Distribute |
| `PARTY_LOOT_MODE.GROUP_LOOT` | Group loot |
| `PARTY_LOOT_MODE.BIDDING` | Bidding |

---

## DOODAD_KIND {#DOODAD_KIND}

Doodad kind constants.

| Constant | Description |
|----------|-------------|
| `DOODAD_KIND.INVALID` | Invalid |
| `DOODAD_KIND.NORMAL` | Normal doodad |
| `DOODAD_KIND.CORPSE` | Corpse |
| `DOODAD_KIND.CRAFT_TARGET` | Craft target |
| `DOODAD_KIND.QUEST` | Quest doodad |
| `DOODAD_KIND.READ` | Readable doodad |
| `DOODAD_KIND.GUIDE` | Guide doodad |
| `DOODAD_KIND.DOOR` | Door |
| `DOODAD_KIND.TRAP` | Trap |
| `DOODAD_KIND.TREASURE` | Treasure |
| `DOODAD_KIND.CLIENT_ONLY` | Client only |

---

## RELATION_TYPE {#RELATION_TYPE}

Relation type constants.

| Constant | Description |
|----------|-------------|
| `RELATION_TYPE.SELF` | Self |
| `RELATION_TYPE.ALLY` | Ally |
| `RELATION_TYPE.ENEMY` | Enemy |
| `RELATION_TYPE.NEUTRALITY` | Neutrality |
| `RELATION_TYPE.PARTY` | Party member |
| `RELATION_TYPE.RAID` | Raid member |

---

## QUEST_STATE {#QUEST_STATE}

Quest state constants.

| Constant | Description |
|----------|-------------|
| `QUEST_STATE.NOT_ACCEPT` | Not accepted |
| `QUEST_STATE.ACCEPTED` | Accepted |
| `QUEST_STATE.FINISHED` | Finished |

---

## MAIL_TYPE {#MAIL_TYPE}

Mail type constants.

| Constant | Description |
|----------|-------------|
| `MAIL_TYPE.INVALID` | Invalid |
| `MAIL_TYPE.PLAYER` | Player mail |
| `MAIL_TYPE.SYSTEM` | System mail |
| `MAIL_TYPE.TEXT_ONLY` | Text only mail |

---

## CHARACTER_GENDER {#CHARACTER_GENDER}

Character gender constants.

| Constant | Description |
|----------|-------------|
| `CHARACTER_GENDER.INVALID` | Invalid |
| `CHARACTER_GENDER.MALE` | Male |
| `CHARACTER_GENDER.FEMALE` | Female |

---

## PLAYER_TALK_ERROR {#PLAYER_TALK_ERROR}

Chat error code constants.

| Constant | Description |
|----------|-------------|
| `PLAYER_TALK_ERROR.PLAYER_NOT_FOUND` | Player not found |
| `PLAYER_TALK_ERROR.NOT_IN_PARTY` | Not in party |
| `PLAYER_TALK_ERROR.NOT_IN_SENCE` | Not in scene |
| `PLAYER_TALK_ERROR.PLAYER_OFFLINE` | Player offline |
| `PLAYER_TALK_ERROR.YOU_BLACKLIST_TARGET` | Target is in your blacklist |
| `PLAYER_TALK_ERROR.TARGET_BLACKLIST_YOU` | You are in target's blacklist |
| `PLAYER_TALK_ERROR.BAN` | Banned |
| `PLAYER_TALK_ERROR.SCENE_CD` | Scene cooldown |
| `PLAYER_TALK_ERROR.NOT_IN_TONG` | Not in guild |
| `PLAYER_TALK_ERROR.TONG_CAN_NOT_SPEAK` | Cannot speak in guild |
| `PLAYER_TALK_ERROR.DAILY_LIMIT` | Daily limit reached |
| `PLAYER_TALK_ERROR.NOT_IN_FORCE` | Not in force |
| `PLAYER_TALK_ERROR.CHARGE_LIMIT` | Charge limit |
| `PLAYER_TALK_ERROR.REMOTE_PLAYER_LIMIT` | Remote player limit |
| `PLAYER_TALK_ERROR.DISABLE_TALK` | Talk disabled |
| `PLAYER_TALK_ERROR.NO_IDENTITY` | No identity |
| `PLAYER_TALK_ERROR.BREAK_RULE` | Rule broken |
| `PLAYER_TALK_ERROR.BULLET_SCREEN_DISABLE` | Bullet screen disabled |
| `PLAYER_TALK_ERROR.BULLET_SCREEN_TEXT_LEN_LIMIT` | Bullet screen text length limit |
| `PLAYER_TALK_ERROR.MUTE_ALL` | All muted |
| `PLAYER_TALK_ERROR.TARGET_APP_BLACKLIST_YOU` | Target app blacklisted you |

---

## See Also

- [UI Object Constants](./UIObject.md)
- [More Constants](./Constants2.md)
