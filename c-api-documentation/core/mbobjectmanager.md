# MBObjectManager(游戏对象管理器)


object manager（对象管理器）是你在制作霸主MOD中将要经常使用的管理器类, 所以熟悉它对你来说非常重要。

MBObjectManager可以用来得到游戏当前已经从XML文件中加载的任何object。 


包括:

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

例如，这是取得一个基础[BasicCharacterObject](basiccharacterobject.md)对象的方法:

```csharp
MBObjectManager.Instance.GetObject<BasicCharacterObject>("example_troop_id");
```

