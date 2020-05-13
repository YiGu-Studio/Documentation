# 物品 Item

## 例子

Source: Modules/SandBoxCore/ModuleData/spitems.xml

```markup
  <Item id="headscarf_d"
        name="{=wW3iouiU}Hijab"
        mesh="headscarf_d"
        culture="Culture.aserai"
        weight="0.5"
        appearance="0.5"
        Type="HeadArmor">
    <ItemComponent>
      <Armor head_armor="3"
             has_gender_variations="false"
             hair_cover_type="all"
             modifier_group="cloth_unarmoured"
             material_type="Cloth"
             beard_cover_type="type3" />
    </ItemComponent>
    <Flags Civilian="true"
           UseTeamColor="true" />
  </Item>
```

## Parent node

* [物品\(类别\) Items](../)

## Child nodes

* [物品组件 ItemComponent](itemcomponent/)
* [旗帜 Flags](flags.md)

## Attributes

[名称 name](./#name) \| [网格 mesh](./#mesh) \| [文化 culture](./#culture) \| [重量 weight](./#weight) \| [外观 appearance](./#appearance) \| [类型 Type](./#type) \| [多人模式物品 multiplayer\_item](./#multiplayer_item) \| [子类型 subtype](./#subtype) \| [难度 difficulty](./#difficulty) \| [\(?\) lod\_atlas\_index](./#lod_atlas_index) \| [是否商品 is\_merchandise](./#is_merchandise) \| [模型名 body\_name](./#body_name) \| [\(?\) recalculate\_body](./#recalculate_body) \| [\(?\) prefab](./#prefab) \| [价值 value](./#value) \| [收起位置 item\_holsters](./#item_holsters) \| [弹药位置偏移 AmmoOffset](./#ammooffset) \| [\(?\) holster\_position\_shift](./#holster_position_shift) \| [\(?\) holster\_body\_name](./#holster_body_name) \| [容器模型 holster\_mesh](./#holster_mesh) \| [容器\(带武器\)模型 holster\_mesh\_with\_weapon](./#holster_mesh_with_weapon) \| [投射物模型 flying\_mesh](./#flying_mesh) \| [盾牌碰撞模型 shield\_body\_name](./#shield_body_name) \| [\(?\) using\_tableau](./#using_tableau) \| [\(?\) has\_lower\_holster\_priority](./#has_lower_holster_priority) \| [物品类别 item\_category](./#item_category) \| [是否食物 IsFood](./#isfood)

* **name**

  **类型:** `string`  
  **范例:** `{=wW3iouiU}Hijab`  
  _注意: 例子中的前缀 `{=}` 是string.txt中定义的翻译文本ID_  
  _尚不知晓翻译文本ID是否为自动生成的_

* **mesh**

  **类型:** `string`  
  **范例:** `headscarf_d`  
  _字符串为模型的ID_  
  _尚未找出模型的存储位置_

* **culture**

  **类型:** `string`  
  **可能的值:** `'Culture.aserai', 'Culture.sturgia', 'Culture.battania', 'Culture.looters', 'Culture.khuzait', 'Culture.vlandia', 'Culture.empire', 'Culture.neutral_culture'`  
  **范例:** `Culture.aserai`

* **weight**

  **类型:** `double`  
  **范例:** `0.5`

* **appearance**

  **类型:** `double`  
  **范例:** `0.5`  
  _待办: 找出这个属性的具体作用_

* **Type**

  **类型:** `ArmourType`  
  **可能的值:** `'HeadArmor', 'headArmor', 'Cape', 'BodyArmor', 'HandArmor', 'LegArmor', 'OneHandedWeapon', 'Bow', 'Polearm', 'Crossbow', 'Thrown', 'Arrows', 'Bolts', 'Shield', 'Horse', 'HorseHarness', 'Goods', 'Banner', 'Animal'`  
  **范例:** `HeadArmor`

* **multiplayer\_item**

  **类型:** `boolean`  
  **可能的值:** `'true', 'false'`  
  **范例:** `false`

* **subtype**

  **类型:** `string`  
  **可能的值:** `'head_armor', 'body_armor', 'bow', 'two_handed_wpn', 'arrows', 'horse'`  
  **范例:** `head_armor`  
  _待办: 查明作用_

* **difficulty**

  **类型:** `int`  
  **可能的值:** `0-100`  
  **范例:** `80`

* **lod\_atlas\_index**

  **类型:** `int`  
  **范例:** `2`  
  _待办: 查明作用_

* **is\_merchandise**

  **类型:** `boolean`  
  **范例:** `false`  
  _定义这件物品是否是商品（是否买得到）_

* **body\_name**

  **类型:** `id`  
  **范例:** `bo_mace_a`  
  _可能是武器的碰撞模型？ 待办: 查明作用_

* **recalculate\_body**

  **类型:** `boolean`  
  **可能的值:** `'true', 'false'`  
  **范例:** `false`  
  _待办: 查明作用_

* **prefab**

  **类型:** `id`  
  **范例:** `torch_a_wm_only_flame`  
  _待办: 查明作用 可能是粒子效果？_

* **value**

  **类型:** `int`  
  **范例:** `150`  
  _市场均价_

* **item\_holsters**

  **类型:** `string`  
  **可能的值:** `'abdomen_left', 'bow_back_2:bow_hip:bow_hip_2:bow_back', 'bow_back:bow_back_2:bow_hip:bow_hip_2', 'sword_left_hip', 'polearm_back:polearm_back_2', 'bow_hip:bow_hip_2:bow_back:bow_back_2', 'crossbow_back:bow_hip:mace_right_hip:bow_hip_2', 'throwing_stone:throwing_stone_2', '', 'quiver_back_top:quiver_back_top_2', 'quiver_back_middle:quiver_bolts_2:quiver_bolts', 'quiver_back_lower:quiver_back_lower_2', 'quiver_back_middle:quiver_bolts:quiver_bolts_2', 'quiver_bolts:quiver_bolts_2:quiver_back_middle:quiver_back_top', 'quiver_back_middle:quiver_back_top:quiver_bolts:quiver_bolts_2', 'shield_round:shield_4', 'shield_oval:shield_4:shield_3:shield_2', 'shield:shield_2:shield_3:shield_4', 'shield_kite:shield_2:shield_3:shield_4'`  
  **范例:** `abdomen_left`  
  _收起状态下的携带位置_

* **AmmoOffset**

  **类型:** `vector3d`  
  **范例:** `0.0, 0.02131, 0.24675`  
  _投射物的起始位置？_

* **holster\_position\_shift**

  **类型:** `vector3d`  
  **范例:** `0.0,0.0,-0.0`  
  _待办: 查明作用（某种位置偏移）_

* **holster\_body\_name**

  **类型:** `string`  
  **范例:** `bo_axe_short`  
  _待办: 查明作用（模型）_

* **holster\_mesh**

  **类型:** `string`  
  **范例:** `stone_holster`  
  _比如箭袋的模型_

* **holster\_mesh\_with\_weapon**

  **类型:** `string`  
  **范例:** `stone_holster`  
  _比如插着剑的剑鞘的模型_

* **flying\_mesh**

  **类型:** `string`  
  **范例:** `arrow_bl_flying`  
  _投射物模型_

* **shield\_body\_name**

  **类型:** `string`  
  **范例:** `bo_sturgia_shield_a`  
  _盾牌的碰撞模型_

* **using\_tableau**

  **类型:** `boolean`  
  **范例:** `true`  
  _Whether the item has a tableau（不确定Tableau是什么）_

* **has\_lower\_holster\_priority**

  **类型:** `boolean`  
  **范例:** `true`  
  _待办: 查明作用_

* **item\_category**

  **类型:** `id`  
  **可能的值:** `'horse', 'sumpter_horse', 'war_horse', 'wool', 'silver', 'jewelry', 'salt', 'cotton', 'flax', 'clay', 'pottery', 'linen', 'leather', 'velvet', 'cheese', 'butter', 'fish', 'grape', 'date_fruit', 'olives', 'beer', 'wine', 'oil', 'fur', 'animal', 'sheep', 'cow', 'hog'`  
  **范例:** `horse`  
  _交易界面的类型_

* **IsFood**

  **类型:** `boolean`  
  **范例:** `true`  
  _能不能吃_

