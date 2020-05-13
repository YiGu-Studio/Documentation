# CraftedItem

## Example Entry

Source: Modules/SandBoxCore/ModuleData/spitems.xml

```markup
  <CraftedItem id="peasant_maul_t1"
               name="{=gYpNILVC}Sledgehammer"
               crafting_template="TwoHandedPolearm"
               culture="Culture.battania">
    <Pieces>
      <Piece id="spear_blade_44"
             Type="Blade"
             scale_factor="102" />
      <Piece id="spear_handle_1"
             Type="Handle" />
    </Pieces>
  </CraftedItem>
```

## Parent node

* [Items](../)

## Child node

* [Pieces](pieces/)

## Attributes

[id](./#id) \| [name](./#name) \| [crafting\_template](./#crafting_template) \| [culture](./#culture) \| [is\_merchandise](./#is_merchandise)

* **id**

  **类型:** `string`  
  **例子:** `sturgia_axe_3_t3`  
  _The ID of the item_

* **name**

  **类型:** `string`  
  **例子:** `{=wW3iouiU}Hijab`  
  _Note: The prefix in the `{=}` format is the translation id found in strings.txt_  
  _TODO: Find out if this is auto generated._

* **crafting\_template**

  **类型:** `string`  
  **possible values:** `'TwoHandedPolearm', 'OneHandedAxe', 'Mace', 'TwoHandedAxe', 'OneHandedSword', 'TwoHandedSword', 'Pike', 'Dagger', 'Javelin', 'ThrowingAxe', 'ThrowingKnife'`  
  **例子:** `TwoHandedPolearm`

* **culture**

  **类型:** `string`  
  **possible values:** `'Culture.aserai', 'Culture.sturgia', 'Culture.battania', 'Culture.looters', 'Culture.khuzait', 'Culture.vlandia', 'Culture.empire', 'Culture.neutral_culture'`  
  **例子:** `Culture.aserai`

* **is\_merchandise**

  **类型:** `boolean`  
  **例子:** `false`  
  _If the item is marketable_

