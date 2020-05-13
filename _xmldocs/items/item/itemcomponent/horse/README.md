# 马匹 Horse

## Parent Node

* [ItemComponent](../)

## Child Node

* [Materials](materials/)

## Attributes

[生物类型 monster](./#monster) \| [操纵性 maneuver](./#maneuver) \| [速度 speed](./#speed) \| [冲撞伤害 charge\_damage](./#charge_damage) \| [体长 body\_length](./#body_length) \| [能不能骑 is\_mountable](./#is_mountable) \| [额外生命值 extra\_health](./#extra_health) \| [骨骼大小 skeleton\_scale](./#skeleton_scale) \| [伤害修正 modifier\_group](./#modifier_group) \| [is\_pack\_animal](./#is_pack_animal) \| [decorator\_key\_min](./#decorator_key_min) \| [decorator\_key\_max](./#decorator_key_max) \| [mane\_mesh](./#mane_mesh)

* **monster**

  **类型:** `string`  
  **接受值:** `'Monster.horse', 'Monster.camel', 'Monster.mule', 'Monster.mule_unmountable', 'Monster.camel_unmountable', 'Monster.horse_2', 'Monster.cat', 'Monster.dog', 'Monster.sheep', 'Monster.cow', 'Monster.hog', 'Monster.goose', 'Monster.chicken'`  
  **例子:** `Monster.horse`  
  _骑乘的类型，比如马啊骆驼啊之类的_

* **maneuver**

  **类型:** `int`  
  **例子:** `73`  
  _操纵性_

* **speed**

  **类型:** `int`  
  **例子:** `73`  
  _速度_

* **charge\_damage**

  **类型:** `int`  
  **例子:** `73`  
  _冲撞伤害_

* **body\_length**

  **类型:** `int`  
  **例子:** `73`  
  _身体长度_

* **is\_mountable**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `false`  
  _能不能骑（骑牛与砍杀）_

* **extra\_health**

  **类型:** `int`  
  **例子:** `81`  
  _额外的生命中？正负皆可_

* **skeleton\_scale**

  **类型:** `string`  
  **接受值:** `'aserai_horse', 'battania_horse', 'empire_horse', 'khuzait_horse', 'sturgia_horse', 'vlandia_horse'`  
  **例子:** `aserai_horse`  
  _预定义的骨骼缩放比例. 待查明数字是否有效以及定义这些常量的位置_

* **modifier\_group**

  **类型:** `string`  
  **接受值:** `'horse'`  
  **例子:** `horse`  
  _不知道干嘛的（译者按：难道和盔甲一样有伤害减免？）_

* **is\_pack\_animal**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `false`  
  _不知道干嘛的s_

* **decorator\_key\_min**

  **类型:** `hex`  
  **例子:** `0F`  
  _不知道干嘛的_

* **decorator\_key\_max**

  **类型:** `hex`  
  **例子:** `0F`  
  _不知道干嘛的_

* **mane\_mesh**

  **类型:** `id`  
  **例子:** `horse_mane`  
  _Mesh ID of the manes_

