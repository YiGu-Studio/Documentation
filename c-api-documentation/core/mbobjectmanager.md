# MBObjectManager


object manager是在霸主中你将经常使用的东西, 所以熟悉它对你来说非常重要。

MBObjectManager可以用来得到游戏当前已经从XML加载的任何object。 


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

例如取得：[BasicCharacterObject](basiccharacterobject.md):

```csharp
MBObjectManager.Instance.GetObject<BasicCharacterObject>("example_troop_id");
```

