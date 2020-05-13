# 防具 Armor

## 父节点 Parent Node

* [ItemComponent](./)

## 子节点 Child Node

* _无 None_

## 属性 Attributes

[头部护甲 head\_armor](armor.md#head_armor) \| [男女不同模型 has\_gender\_variations](armor.md#has_gender_variations) \| [遮盖头发模式 hair\_cover\_type](armor.md#hair_cover_type) \| [修正类型 modifier\_group](armor.md#modifier_group) \| [材质类型 material\_type](armor.md#material_type) \| [遮盖胡子模式 beard\_cover\_type](armor.md#beard_cover_type) \| [躯干护甲 body\_armor](armor.md#body_armor) \| [腿部护甲 leg\_armor](armor.md#leg_armor) \| [手部护甲 arm\_armor](armor.md#arm_armor) \| [覆盖躯干 covers\_body](armor.md#covers_body) \| [\(?\) body\_mesh\_type](armor.md#body_mesh_type) \| [覆盖双腿 covers\_legs](armor.md#covers_legs) \| [覆盖双手 covers\_hands](armor.md#covers_hands) \| [\(?\) mane\_cover\_type](armor.md#mane_cover_type) \| [family\_type](armor.md#family_type) \| [操作性修正 maneuver\_bonus](armor.md#maneuver_bonus) \| [速度修正 speed\_bonus](armor.md#speed_bonus) \| [冲刺修正 charge\_bonus](armor.md#charge_bonus) \| [缰绳模型 reins\_mesh](armor.md#reins_mesh) \| [覆盖头部 covers\_head](armor.md#covers_head)

* **head\_armor**

  **类型:** `int`  
  **范例:** `64`  
  _头部护甲值_

* **has\_gender\_variations**

  **类型:** `boolean`  
  **范例:** `true`  
  _男女是否使用不同模型_

* **hair\_cover\_type**

  **类型:** `string` **接受值:** `'all', 'type1', 'type2', 'type3'`  
  **范例:** `all`  
  _待查明type1，type2，type3分别是啥样的_

* **modifier\_group**

  **类型:** `string`  
  **接受值:** `'cloth_unarmoured', 'leather', 'plate', 'chain', 'cloth'`  
  **范例:** `leather`  
  _可能影响伤害吸收?_

* **material\_type**

  **类型:** `string`  
  **接受值:** `'Cloth', 'Leather', 'Plate', 'Chainmail'`  
  **范例:** `Cloth`  
  _护甲的材质_

* **beard\_cover\_type**

  **类型:** `string`  
  **接受值:** `'type3', 'type2', 'none', 'all', 'type1'`  
  **范例:** `none`  
  _类似遮盖头发模式_

* **body\_armor**

  **类型:** `int`  
  **范例:** `23`  
  _躯干护甲值_

* **leg\_armor**

  **类型:** `int`  
  **范例:** `23`  
  _腿部护甲值_

* **arm\_armor**

  **类型:** `int`  
  **范例:** `23`  
  _手部护甲值_

* **covers\_body**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **范例:** `true`  
  _护甲是否覆盖躯干_

* **body\_mesh\_type**

  **类型:** `string`  
  **接受值:** `'shoulders'`  
  **范例:** `shoulders`  
  _待查明作用_

* **covers\_legs**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **范例:** `true`  
  _是否覆盖双腿_

* **covers\_hands**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **范例:** `true`  
  _是否覆盖双手_

* **mane\_cover\_type**

  **类型:** `string`  
  **接受值:** `'none', 'all'`  
  **范例:** `none`  
  _待查明覆盖部位_

* **family\_type**

  **类型:** `int`  
  **接受值:** `'1', '2'`  
  **范例:** `1`  
  _待查明作用_

* **maneuver\_bonus**

  **类型:** `int`  
  **范例:** `12`  
  _不知道是对人还是对马的操作性修正\(译者认为是马铠对马的操纵性修正\)_

* **speed\_bonus**

  **类型:** `int`  
  **范例:** `11`  
  _不知道是对人还是对马的速度修正\(译者认为是马铠对马的速度修正\)_

* **charge\_bonus**

  **类型:** `int`  
  **范例:** `11`  
  _不知道是对人还是对马的冲刺修正\(译者认为是马铠对马的冲刺修正\)_

* **reins\_mesh**

  **类型:** `string`  
  **范例:** `horse_harness_vlandia_b_rein`  
  _缰绳的模型ID_

* **covers\_head**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **范例:** `true`  
  _是否覆盖头部_

