# Weapon

## Parent Node

* [ItemComponent](../)

## Child Node

* [WeaponFlags](weaponflags.md)

## Attributes

[武器类别 weapon\_class](./#weapon_class) \| [平衡 weapon\_balance](./#weapon_balance) \| [thrust\_speed](./#thrust_speed) \| [速度 speed\_rating](./#speed_rating) \| [投射物速度 missile\_speed](./#missile_speed) \| [长度 weapon\_length](./#weapon_length) \| [挥砍伤害 swing\_damage](./#swing_damage) \| [挥砍伤害的类型 swing\_damage\_type](./#swing_damage_type) \| [武器使用 item\_usage](./#item_usage) \| [材质 physics\_material](./#physics_material) \| [弹药类型 ammo\_class](./#ammo_class) \| [弹药限制 ammo\_limit](./#ammo_limit) \| [准确度 accuracy](./#accuracy) \| [戳刺伤害 thrust\_damage](./#thrust_damage) \| [戳刺伤害类型 thrust\_damage\_type](./#thrust_damage_type) \| [重心 center\_of\_mass](./#center_of_mass) \| [弹药量 stack\_amount](./#stack_amount) \| [旋转角度 rotation](./#rotation) \| [掠过的声音 passby\_sound\_code](./#passby_sound_code) \| [旋转速度 rotation\_speed](./#rotation_speed) \| [飞行的声音 flying\_sound\_code](./#flying_sound_code) \| [击中后的角度 sticking\_rotation](./#sticking_rotation) \| [击中后的位置 sticking\_position](./#sticking_position) \| [轨迹粒子效果 trail\_particle\_name](./#trail_particle_name) \| [位置 position](./#position) \| [躯干护甲 body\_armor](./#body_armor) \| [耐久度 hit\_points](./#hit_points)

* **weapon\_class**

  **类型:** `string`  
  **接受值:** `'OneHandedAxe', 'Bow', 'OneHandedSword', 'TwoHandedPolearm', 'Crossbow', 'Stone', 'Arrow', 'Boulder', 'Bolt', 'LargeShield', 'Banner'`  
  **例子:** `OneHandedAxe`  
  _武器的类别_

* **weapon\_balance**

  **类型:** `int`  
  **例子:** `100`  
  _武器的平衡_

* **thrust\_speed**

  **类型:** `int`  
  **例子:** `12`  
  _Thrust speed of the weapon_

* **speed\_rating**

  **类型:** `int`  
  **例子:** `60`  
  _武器速度_

* **missile\_speed**

  **类型:** `int`  
  **例子:** `60`  
  _射出的投射物速度_

* **weapon\_length**

  **类型:** `int`  
  **例子:** `60`  
  _武器长度_

* **swing\_damage**

  **类型:** `int`  
  **例子:** `60`  
  _挥砍伤害值_

* **swing\_damage\_type**

  **类型:** `string`  
  **接受值:** `'Pierce', 'Blunt', 'Cut'`  
  **例子:** `Pierce`  
  _挥砍伤害的类型_

* **item\_usage**

  **类型:** `string`  
  **接受值:** `'torch', 'bow', 'long_bow', 'onehanded_block_shield_swing', 'polearm_block_thrust', 'crossbow_fast', 'crossbow', 'stone', '', 'heavy_stone', 'arrow_top', 'arrow_right', 'hand_shield', 'shield', 'banner'`  
  **例子:** `heavy_stone`  
  _武器是咋用的_

* **physics\_material**

  **类型:** `string`  
  **接受值:** `'metal_weapon', 'wood_weapon', 'missile', 'ballista_missile', 'burning_ballista', 'boulder_stone', 'burning_jar', 'wood_shield', 'metal_shield'`  
  **例子:** `metal_shield`  
  _武器的材质（诸如铁制盾，铁制武器，木制武器）_

* **ammo\_class**

  **类型:** `string`  
  **接受值:** `'Arrow', 'Bolt', 'Stone', 'Boulder'`  
  **例子:** `Arrow`  
  _弹药类型（箭矢、弩矢等）_

* **ammo\_limit**

  **类型:** `int`  
  **例子:** `1`  
  _弹药限制，不知道是'一个弹匣'还是'一次射出'。_

* **accuracy**

  **类型:** `int`  
  **例子:** `21`  
  _远程武器的准确度_

* **thrust\_damage**

  **类型:** `int`  
  **例子:** `21`  
  _戳刺伤害_

* **thrust\_damage\_type**

  **类型:** `string`  
  **接受值:** `'Pierce', 'Blunt', 'Cut'`  
  **例子:** `Pierce`  
  _戳刺伤害类型_

* **center\_of\_mass**

  **类型:** `vector3d`  
  **例子:** `0.15,0,0`  
  _武器中心位置，不知道干嘛用的_

* **stack\_amount**

  **类型:** `int`  
  **例子:** `23`  
  _应该是一袋箭有多少支这种_

* **rotation**

  **类型:** `vector3d`  
  **例子:** `100,30,20`  
  _不知道干嘛用的（译者按：可能是飞斧之类扔出后模型的旋转角度向量）_

* **passby\_sound\_code**

  **类型:** `string`  
  **例子:** `event:/mission/combat/missile/passby`  
  _投射物掠过人物发出的声音_

* **rotation\_speed**

  **类型:** `double`  
  **例子:** `0.5`  
  _不知道干嘛用的（译者按：可能是飞斧之类扔出后模型的旋转速度）_

* **flying\_sound\_code**

  **类型:** `string`  
  **例子:** `event:/mission/combat/missile/foley/passby`  
  _投射物飞行发出的声音_

* **sticking\_rotation**

  **类型:** `vector3d`  
  **例子:** `90,0,0`  
  _不知道干嘛用的（译者按：与之前的旋转角度类似，结合下一个属性，可能是击中后模型的旋转角度，飞斧击中盾牌后全都是同一个角度）_

* **sticking\_position**

  **类型:** `vector3d`  
  **例子:** `90,0,0`  
  _不知道干嘛用的（译者按：似乎是旋转中心？结合上一个属性，可能是击中后模型的相对位置）_

* **trail\_particle\_name**

  **类型:** `string`  
  **例子:** `psys_game_missile_flame`  
  _弹药飞行轨迹的粒子效果_

* **position**

  **类型:** `vector3d`  
  **例子:** `-0.04, -0.05, 0.01`  
  _位置，暂时不知道是啥位置_

* **body\_armor**

  **类型:** `int`  
  **例子:** `82`  
  _武器提供的躯干护甲值，不知道对于其他部位是否有效_

* **hit\_points**

  **类型:** `int`  
  **例子:** `820`  
  _盾的耐久度_

