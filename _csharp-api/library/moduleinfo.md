# ModuleInfo

`ModuleInfor`类里放的是各个Mod的相关信息。

你也可以获取一个列表，里面放着所有**已加载**的Mod，以及它们各自的详细信息\(它们自己的`ModuleInfor`\)，比如：

```csharp
var loadedMods = new List<ModuleInfo>();
foreach(var moduleName in Utilities.GetModulesNames())
{
    var moduleInfo = new ModuleInfo();
    moduleInfo.Load(moduleName);
    loadedMods.Add(moduleInfo);
}
```

以上代码可以用来判定某个Mod加载了没有。当Mod之间存在某些依赖关系，但又不是必须依赖的时候，这种判断会很有用。

