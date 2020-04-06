# 目录结构

所有的目录都是可选的，除了MOD文件夹本身和可用的[SubModule.xml](../_xmldocs/submodule.md)文件。

游戏自带的Native Module是一个很好的例子，位置：
`Drive:\\InstallLocation\Mount & Blade II Bannerlord\Modules\Native\` 

## 目录说明及文件范例

* `AssetPackages` - 暂时未知，可能需要MOD编辑器正式发布之后才能动这些文件。
  *  `someasset.tpac`
* `Atmospheres` -  [参考[环境 Atmosphere]](../_xmldocs/atmosphere.md)
  * `Interpolated` 
    * `interpolatedatmosphere.xml`
  * `atmosphere.xml`
* `bin` - 存放编译好的二进制文件 - [参考[基础 C\# MOD]](../_tutorials/basic-csharp-mod.md)
  * `Win64_Shipping_Client`
    * `MyModule.dll`
* `GUI` - 存放大部分关于Gauntlet的文件。
  * `Brushes` - 存放Gauntlet Brushes。
  * `Prefabs` - 存放Gauntlet Movies。
* `ModuleData` - 存放所有MOD中XML格式的文件 \(比如物品/文化/文本\).
* `SceneObj` - 存放场景.

```text
- MyModule
	- AssetPackages
		-- assetpackage.tpac
	- Atmospheres
		- Interpolated
			-- interpolatedatmosphere.xml
		-- atmosphere.xml
	- bin
		- Win64_Shipping_Client
			-- MyModule.dll
    - GUI
        - Brushes
        - Prefabs
    - ModuleData
    - SceneObj
    - SubModule.xml
```

