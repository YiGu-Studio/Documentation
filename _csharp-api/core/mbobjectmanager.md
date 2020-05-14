# MBObjectManager 类

在给`霸主`做模组中你会频繁使用对象管理器,所以你需要熟练运用它.

MBObjectManager可以用于一切从XML中加载进游戏的对象.

内容包括:

* [BasicCharacterObjects](basiccharacterobject.md)
* CharacterAttributes
* CraftingPieces
* CraftingTemplates
* Cultures
* ItemModifierGroups
* ItemCategories
* ItemComponents
* [ItemObjects](itemobject.md)
* SkillObjects
* SiegeEngineTypes

获取基本角色对象的例子[BasicCharacterObject](basiccharacterobject.md):
```csharp
MBObjectManager.Instance.GetObject<BasicCharacterObject>("example_troop_id");
```
