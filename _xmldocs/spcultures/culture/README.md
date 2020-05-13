# Culture

## Parent node

* [SPCultures](../)

## Child node

* [female\_names](female_names/)
* [male\_names](male_names/)
* [clan\_names](clan_names/)

## Attributes

[id](./#id) \| [name](./#name) \| [is\_main\_culture](./#is_main_culture) \| [color](./#color) \| [color2](./#color2) \| [elite\_basic\_troop](./#elite_basic_troop) \| [basic\_troop](./#basic_troop) \| [melee\_militia\_troop](./#melee_militia_troop) \| [ranged\_militia\_troop](./#ranged_militia_troop) \| [melee\_elite\_militia\_troop](./#melee_elite_militia_troop) \| [ranged\_elite\_militia\_troop](./#ranged_elite_militia_troop) \| [can\_have\_settlement](./#can_have_settlement) \| [town\_edge\_number](./#town_edge_number) \| [villager\_party\_template](./#villager_party_template) \| [default\_party\_template](./#default_party_template) \| [caravan\_party\_template](./#caravan_party_template) \| [elite\_caravan\_party\_template](./#elite_caravan_party_template) \| [militia\_party\_template](./#militia_party_template) \| [rebels\_party\_template](./#rebels_party_template) \| [prosperity\_bonus](./#prosperity_bonus) \| [encounter\_background\_mesh](./#encounter_background_mesh) \| [default\_face\_key](./#default_face_key) \| [text](./#text) \| [tournament\_master](./#tournament_master) \| [villager](./#villager) \| [caravan\_master](./#caravan_master) \| [armed\_trader](./#armed_trader) \| [caravan\_guard](./#caravan_guard) \| [veteran\_caravan\_guard](./#veteran_caravan_guard) \| [duel\_preset](./#duel_preset) \| [prison\_guard](./#prison_guard) \| [guard](./#guard) \| [steward](./#steward) \| [blacksmith](./#blacksmith) \| [weaponsmith](./#weaponsmith) \| [townswoman](./#townswoman) \| [townswoman\_infant](./#townswoman_infant) \| [townswoman\_child](./#townswoman_child) \| [townswoman\_teenager](./#townswoman_teenager) \| [townsman](./#townsman) \| [townsman\_infant](./#townsman_infant) \| [townsman\_child](./#townsman_child) \| [townsman\_teenager](./#townsman_teenager) \| [ransom\_broker](./#ransom_broker) \| [gangleader\_bodyguard](./#gangleader_bodyguard) \| [merchant\_notary](./#merchant_notary) \| [artisan\_notary](./#artisan_notary) \| [preacher\_notary](./#preacher_notary) \| [rural\_notable\_notary](./#rural_notable_notary) \| [shop\_worker](./#shop_worker) \| [tavernkeeper](./#tavernkeeper) \| [taverngamehost](./#taverngamehost) \| [musician](./#musician) \| [tavern\_wench](./#tavern_wench) \| [armorer](./#armorer) \| [horseMerchant](./#horsemerchant) \| [merchant](./#merchant) \| [beggar](./#beggar) \| [female\_beggar](./#female_beggar) \| [female\_dancer](./#female_dancer) \| [gear\_practice\_dummy](./#gear_practice_dummy) \| [weapon\_practice\_stage\_1](./#weapon_practice_stage_1) \| [weapon\_practice\_stage\_2](./#weapon_practice_stage_2) \| [weapon\_practice\_stage\_3](./#weapon_practice_stage_3) \| [gear\_dummy](./#gear_dummy) \| [militia\_bonus](./#militia_bonus) \| [is\_bandit](./#is_bandit) \| [bandit\_chief](./#bandit_chief) \| [bandit\_raider](./#bandit_raider) \| [bandit\_bandit](./#bandit_bandit) \| [bandit\_boss](./#bandit_boss) \| [bandit\_boss\_party\_template](./#bandit_boss_party_template)

* **id**

  **类型:** `string`  
  **例子:** `empire`  
  _The ID of the culture \(faction\)_

* **name**

  **类型:** `string`  
  **例子:** `{=FjwRsf1C}Vlandia`  
  _Note: The prefix in the `{=}` format is the translation id found in strings.txt_  
  _TODO: Find out if this is auto generated._

* **is\_main\_culture**

  **类型:** `boolean`  
  **接受值:** `true` \| `false` **例子:** `false`  
  _If the culture is a major \(true\) or a minor \(false\) faction_

* **color**

  **类型:** `hex`  
  **例子:** `FF4E3A55`  
  _The color of the faction. TODO: figure out where the colour is displayed_

* **color2**

  **类型:** `hex`  
  **例子:** `FF4E3A55`  
  _The secondary color of the faction. TODO: figure out where the colour is displayed_

* **elite\_basic\_troop**

  **类型:** `reference`  
  **例子:** `NPCCharacter.imperial_vigla_recruit`  
  _Reference to the NPCCharacter XML node. The Elite Recruit troop of the faction._

* **basic\_troop**

  **类型:** `reference`  
  **例子:** `NPCCharacter.imperial_recruit`  
  _Reference to the NPCCharacter XML node. The Recruit troop of the faction._

* **melee\_militia\_troop**

  **类型:** `reference`  
  **例子:** `NPCCharacter.imperial_recruit`  
  _Reference to the NPCCharacter XML node._

* **ranged\_militia\_troop**

  **类型:** `reference`  
  **例子:** `NPCCharacter.imperial_recruit`  
  _Reference to the NPCCharacter XML node._

* **melee\_elite\_militia\_troop**

  **类型:** `reference`  
  **例子:** `NPCCharacter.imperial_recruit`  
  _Reference to the NPCCharacter XML node._

* **ranged\_elite\_militia\_troop**

  **类型:** `reference`  
  **例子:** `NPCCharacter.imperial_recruit`  
  _Reference to the NPCCharacter XML node._

* **can\_have\_settlement**

  **类型:** `reference`  
  **接受值:** `true` \| `false`  
  **例子:** `true`  
  _If the faction can have settlements on the map._

* **town\_edge\_number**

  **类型:** `int`  
  **例子:** `16`  
  _TODO: figure out what this does._

* **villager\_party\_template**

  **类型:** `reference`  
  **例子:** `PartyTemplate.villager_empire_template`  
  _Villagers template reference to PartyTemplate XML node_

* **default\_party\_template**

  **类型:** `reference`  
  **例子:** `PartyTemplate.villager_empire_template`  
  _Default template reference to PartyTemplate XML node_

* **caravan\_party\_template**

  **类型:** `reference`  
  **例子:** `PartyTemplate.villager_empire_template`  
  _Caravan template reference to PartyTemplate XML node_

* **elite\_caravan\_party\_template**

  **类型:** `reference`  
  **例子:** `PartyTemplate.villager_empire_template`  
  _Elite Caravan template reference to PartyTemplate XML node_

* **militia\_party\_template**

  **类型:** `reference`  
  **例子:** `PartyTemplate.villager_empire_template`  
  _Militia template reference to PartyTemplate XML node_

* **rebels\_party\_template**

  **类型:** `reference`  
  **例子:** `PartyTemplate.villager_empire_template`  
  _Rebels template reference to PartyTemplate XML node_

* **prosperity\_bonus**

  **类型:** `int`  
  **例子:** `1`  
  _Bonus to the prosperity of a faction_

* **encounter\_background\_mesh**

  **类型:** `reference`  
  **例子:** `encounter_empire`  
  _Encounter background_

* **default\_face\_key**

  **类型:** `face_code`  
  **例子:** `000fa92e90004202aced5d976886573d5d679585a376fdd605877a7764b8987c00000000000007520000037f0000000f00000037049140010000000000000000`  
  _Default face keys for faction_

* **text**

  **类型:** `string`  
  **例子:** `{=X0kKBzsW}Lorem Ipsum Dol Amor`  
  _Description of the faction_

* **tournament\_master**

  **类型:** `reference`  
  **例子:** `NPCCharacter.tournament_master_empire`  
  _Reference to the tournament master NPCCharacter XML node._

* **villager**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **caravan\_master**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **armed\_trader**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **caravan\_guard**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **veteran\_caravan\_guard**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **duel\_preset**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **prison\_guard**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **guard**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **steward**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **blacksmith**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **weaponsmith**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **townswoman**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **townswoman\_infant**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **townswoman\_child**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **townswoman\_teenager**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **townsman**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **townsman\_infant**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **townsman\_child**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **townsman\_teenager**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **ransom\_broker**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **gangleader\_bodyguard**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **merchant\_notary**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **artisan\_notary**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **preacher\_notary**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **rural\_notable\_notary**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **shop\_worker**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **tavernkeeper**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **taverngamehost**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **musician**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **tavern\_wench**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **armorer**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **horseMerchant**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **merchant**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **beggar**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **female\_beggar**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **female\_dancer**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **gear\_practice\_dummy**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **weapon\_practice\_stage\_1**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **weapon\_practice\_stage\_2**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **weapon\_practice\_stage\_3**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **gear\_dummy**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **militia\_bonus**

  **类型:** `int`  
  **例子:** `1`  
  _TODO: figure out what exactly this bonus does._

* **is\_bandit**

  **类型:** `int`  
  **接受值:** `true` \| `false`  
  **default:** `false`  
  **例子:** `1`  
  _TODO: figure out what exactly this bonus does._

* **bandit\_chief**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **bandit\_raider**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **bandit\_bandit**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **bandit\_boss**

  **类型:** `reference`  
  **例子:** `NPCCharacter.villager_empire`  
  _Reference to the NPCCharacter XML node._

* **bandit\_boss\_party\_template**

  **类型:** `reference`  
  **例子:** `PartyTemplate.sea_raiders_boss_party_template`  
  _Bandit boss party template reference to PartyTemplate XML node_

