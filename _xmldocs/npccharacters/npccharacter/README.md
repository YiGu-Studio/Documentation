# NPCCharacter（NPC角色）

（译者注：不单单指玩家在酒馆里招的同伴）

## 父节点

* [NPCCharacters](../)

## 子节点

* [equipment](equipment.md)
* [equipmentSet](equipmentset/)
* [face](face/)
* [skills](skills/)
* [Traits](traits/)
* [upgrade\_targets](upgrade_targets/)

## 属性

[id](./#id) \| [name](./#name) \| [default\_group](./#default_group) \| [is\_hero](./#is_hero) \| [civilianTemplate](./#civiliantemplate) \| [occupation](./#occupation) \| [culture](./#culture) \| [skill\_template](./#skill_template) \| [skill\_template](./#skill_template_1) \| [is\_female](./#is_female) \| [level](./#level) \| [is\_basic\_troop](./#is_basic_troop) \| [upgrade\_requires](./#upgrade_requires) \| [formation\_position\_preference](./#formation_position_preference) \| [battleTemplate](./#battletemplate) \| [age](./#age) \| [voice](./#voice)

* **id**

  **数据类型:** `string`  
  **例子:** `npc_wanderer_equipment_template_aserai`  
  _NPC的ID用于游戏引用人物_

* **name**

  **数据类型:** `string`  
  **例子:** `{=wW3iouiU}Hijab`  
  _注意: 在 `{=}`格式中前缀，是在strings.txt中的翻译id。_

* **default\_group**

  **数据类型:** `string`  
  **可选取值:** `Infantry` \| `General` \| `Ranged` \| `HorseArcher` \| `Cavalry`  
  **例子:** `Infantry`  
  _不区分大小写。 命令NPC时所属的默认组。_

* **is\_hero**

  **数据类型:** `boolean`  
  **可接受取值:** `true` \| `false`  
  **例子:** `true`  
  _待办: 去找找它到底有什么作用_

* **civilianTemplate**

  **数据类型:** `reference`  
  **例子:** `NPCCharacter.npc_wanderer_equipment_template_empire`  
  _引用对应着某个市民装备模板._

* **occupation**

  **数据类型:** `string`  
  **可选取值:** `Wanderer` \| `Soldier` \| `Townsfolk` \| `Mercenary` \| `Gangster` \| `PrisonGuard` \| `Judge` \| `Blacksmith` \| `Weaponsmith` \| `NotAssigned` \| `RansomBroker` \| `ShopKeeper` \| `ShopWorker` \| `Tavernkeeper` \| `TavernGameHost` \| `Musician` \| `TavernWench` \| `Armorer` \| `HorseTrader` \| `GoodsTrader` \| `ArenaMaster` \| `Villager` \| `CaravanGuard` \| `BannerBearer`  
  **例如:** `Wanderer`  
  _NPC的职业_

* **culture**

  **数据类型:** `string`  
  **可选取值:** `Culture.empire` \| `Culture.aserai` \| `Culture.sturgia` \| `Culture.khuzait` \| `Culture.battania` \| `Culture.vlandia` \| `Culture.darshi` \| `Culture.nord` \| `Culture.vakken` \| `Culture.neutral_culture`  
  **例子:** `Culture.empire`  
  _NPC所属的派系_

* **skill\_template**

  **数据类型:** `reference`  
  **例子:** `NPCCharacter.infantry_heavyinfantry_level1_template_skills`  
  _引用对应着某个技能加点模板_

* **is\_female**

  **数据类型:** `boolean`  
  **可接受取值:** `true` \| `false`  
  **例子:** `true`  
  _NPC是否为女性_

* **level**

  **数据类型:** `int`  
  **例子:** `5`  
  _NPC的等级_

* **is\_basic\_troop**

  **数据类型:** `boolean`  
  **可接受取值:** `true` \| `false`  
  **例子:** `true`  
  _待办: 搞清楚这个是干嘛的_

* **upgrade\_requires**

  **数据类型:** `ItemCategory reference`  
  **可选取值:** `ItemCategory.horse` \| `ItemCategory.war_horse`  
  **例子:** `ItemCategory.horse`  
  _NPC升级必须的物品_

* **formation\_position\_preference**

  **数据类型:** `Formation reference`  
  **可能取值:** `Back`  
  **例子:** `Back`  
  _阵地位置偏好_

* **battleTemplate**

  **数据类型:** `NPCCharacter reference`  
  **例子:** `NPCCharacter.npc_wanderer_equipment_template_empire`  
  _战役装备模板_

* **age**

  **数据类型:** `int`  
  **例子:** `45`  
  _NPC的年龄_

* **voice**

  **数据类型:** `string`  
  **可选取值:** `curt`  
  **例子:** `curt`  
  _NPC的声线类型_

