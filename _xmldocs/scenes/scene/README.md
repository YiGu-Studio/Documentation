# Scene

## Parent node

* [Scenes](../)

## Child nodes

* [TerrainTypes](terraintypes/)

## Attributes

[name](./#name) \| [terrain](./#terrain) \| [forest\_density](./#forest_density) \| [is\_siege\_map](./#is_siege_map) \| [is\_village\_map](./#is_village_map)

* **name**

  **类型:** `string`  
  **例子:** `{=!}battle_terrain_a (Plain)`  
  _The name of the scene_

* **terrain**

  **类型:** `string`  
  **possible values:** `Plain` \| `Desert` \| `Steppe` \| `Swamp` \| `Forest` **例子:** `Plain`  
  _The terrain of the scene_

* **forest\_density**

  **类型:** `string`  
  **possible values:** `Low` \| `High` **例子:** `Low`  
  _The forest density on the scene_  
  _Note: the value seems to be case insensitive_

* **is\_siege\_map**

  **类型:** `boolean`  
  **接受值:** `true` \| `false`  
  **default value:** `false`  
  **例子:** `true`  
  _If the scene is a Siege scene_

* **is\_village\_map**

  **类型:** `boolean`  
  **接受值:** `true` \| `false`  
  **default value:** `false`  
  **例子:** `true`  
  _If the scene is a Village scene_

