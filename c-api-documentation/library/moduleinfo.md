# ModuleInfo

ModuleInfo类包含了所有模组的信息。

你可以通过类似下面这种方法，获取所有 **已经加载的** 模组列表，和关于它们的细节信息(它们的ModuleInfo) ：

```csharp
var loadedMods = new List<ModuleInfo>();
foreach(var moduleName in Utilities.GetModulesNames())
{
    var moduleInfo = new ModuleInfo();
    moduleInfo.Load(moduleName);
    loadedMods.Add(moduleInfo);
}
```

这可以用来判断一个模组是否已经被加载，对于使用依赖模组的Mod十分有用。
